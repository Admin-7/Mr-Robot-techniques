> [[Wiki|Home]] ▸ **Cryptography**

One fundamental component of digital safety is an understanding of applied cryptography ("crypto," for short). While most introductions to cryptography focus extensively on mathematics, this article attempts a far more practical introduction to the concepts. Although it is infeasible to completely avoid maths, a full understanding of the mathematical details is not required for the proper or safe use of crypto features because it is the concepts, not the details, that are most important for people new to the world of digital safety to internalize.

# Contents

1. [Introduction](#introduction)
1. [Best friends](#best-friends)
1. [Basic concepts](#basic-concepts)
    1. [Messages (contents)](#messages-contents)
    1. [Adversaries (eavesdroppers)](#adversaries-eavesdroppers)
    1. [Channels (mediums)](#channels-mediums)
    1. [Secrets (keys)](#secrets-keys)
    1. [Schemes (algorithms)](#schemes-algorithms)
1. Forget the computer: Understanding decoder rings
1. Theory vs. Practice: Truly unbreakable encryption that won't work in practice

# Introduction

Cryptography seems magical, but it isn't. A basic understanding of most modern provably secure digital systems is within your reach. All you need to understand most security protocols, at least well enough to use them safely and fluently, is a solid understanding of the nature of what computers are, familiarity with a few terms of art such as "key," "cipher," and "plaintext," and the willingness to think through a couple of simple problem scenarios.

This article is a work-in-progress of an attempt to distill a massive collection of alternate resources about mathematical and applied cryptography into an accessible explanation for complete beginners. Where necessary, it sacrifices brevity in favor of verbose clarity, although over time the hope is that it will become shorter (not longer) as better explanations or metaphors make themselves apparent to the authors. For a list of cited sources, see [§ Additional references](#additional-references), below.

# Best friends

You're 10 years old. Your best friend sits next to you in class at school. Every day, despite your teacher's insistence that your attention be on the textbook, you still need to exchange thoughts, observations, secrets, gossip, jokes, and dreams. No one can blame you. After all, the impulse to communicate is one of the most human of traits.

You have become quite adept at passing notes between yourselves while your teacher's back is turned. Unfortunately, each attempt has become increasingly risky. At first, your teacher simply chided you for not paying attention. But as your disobedience saw no sign of decreasing, the school's attempts to deter your behavior have become ever fiercer.

There are numerous issues associated with communicating with your best friend in an openly hostile environment like this:

* First of all, as you have already learned, you might be caught red-handed in the act. Ideally, you would have some way of passing notes without fear of ever being caught; the mere fact of your communication would be hidden from any observer.
* Even if you are not caught red-handed, the teacher might find notes you wrote that day when he searches your desks after class. Ideally, you would have some way of protecting the content of your messages such that the teacher cannot understand what you wrote even if they obtained the note and read the symbols on it. This is particularly important, since many of the notes are about him, which are surely going to raise his ire if he can read them.

How to communicate privately? Using hand signals, perhaps? This would solve the problem of leaving notes behind, but it is even more conspicuous than passing notes. You will be found out for sure.

After some discussion at the playground, the two of you decide that, no, the act of passing notes has proven to be effective enough, largely because the two of you are not the only ones who do it. The bigger problem is that when you are caught or when a note is found, the teacher can track the note back down to you.

If only there were some way of writing notes such that you could not be identified as their source….

Surely you are not the first young kids who have faced this problem. What you need is a secret code. A private language that only you and your friend know, small enough to fit on the notes you write, yet expressive enough to portray your dislike of classtime. By increasing your operational skill of passing notes back and forth, and using a secret language that you have yet to develop, you are confident that you can communicate privately, without ever fearing detention again.

# Basic concepts

The above simple scenario is a commonplace, physical-world example that has many of the most important elements of modern cryptographic systems.

## Messages (contents)

Every cryptographic system operates on some message. In the example above, the messages are the hastily written notes that you are passing to your best friend during class. When you write, "Mr. Hastings smells a lot like tuna fish today," you are composing a message that, you hope, will remain a secret. In cryptography, we call this the *plaintext*, because it is the text of the message in its plainly readable form. If this message is read by anyone other than your best friend, it will compromise your conversation's *confidentiality* and intrude upon your *privacy*.

Maintaining the confidentiality of your message is related to, but not the same thing as, ensuring that your conversation itself remain *secret*. For example, if your teacher turns around and catches you with your hand across your desk, he will surely force you to hand over the note. Your message has been *intercepted* while it was being sent.

When the teacher unfolds the note to reveal what you wrote, he will be able to understand what you said because you did not *encrypt* the message; it was sent *unencrypted*, which is to say that it was never translated away from plaintext.

## Adversaries (eavesdroppers)

In a perfect world, one without authoritarian and boring school systems, there would be no need for you and your best friend to use or care about cryptography because there would be no context in which your communication would be restricted or risk your safety. The teacher would not be a threat to you. However, because we do not live in that perfect world, you have *adversaries* like Mr. Hastings, who are all too eager to *eavesdrop* on the notes you want to pass to your best friend.

The purpose of cryptography is to thwart the efforts of these adversaries. Perhaps counterintuitively, it is precisely because of the presence of your enemies that you have need for such powerful tools like cryptography in the first place.

## Channels (mediums)

A channel is a medium of communication: *how* the information is shared, rather than *what* information is being shared. Earlier, when briefly considered using hand signals to keep your notes from falling into your teacher's hands, what you were considering was an *alternate channel* over which to send your messages. While having multiple channels is useful, they do not necessarily change the nature of the problem.

Any given channel may be at risk of being eavesdropped on, and so simply using a different or multiple channels increases the logistical cost for an eavesdropper, but not necessarily the kind of action they must take to intercept your communications.

## Secrets (keys)

In order to produce a secret language immune from being eavesdropped, both you and your best friend must know this alternate, more private "langugage." For example, let's presume that your secret language just replaces one word with another. Your original plaintext message…

```
Mr. Hastings smells a lot like tuna fish today
```

…is too risky to send unencrypted, so you come up with a secret code that maps one word to another:

| Mr. | Hastings | smells   | a    | lot    | like | tuna    | fish  | today |
| --- | -------- | -------- | ---- | ------ | ---- | ------- | ----- | ----- |
| Egg | floss    | vertical | cake | hooked | cat  | vulture | black | omen  |

Now, when you want to tell your friend about dissatisfaction with the olfactory situation in class today, you write a note like this:

```
Egg floss vertical cake hooked cat vulture black omen
```

By substituting one word for another, we have transformed our plaintext into *ciphertext*. That is to say, we have encrypted it by processing through a *cipher*, which in this case is simply changing one word to a second equivalent word that only has meaning if you know what word it should be mapped back into.

One good thing about this new note is that it's far less risky to send, because Mr. Hastings will not have any idea that it is about him! Unfortuantely, if you do not also tell your friend about your choice of mapping one word to a specific other word, your friend will also have no idea what you're talking about. In other words, if you do not share the *key* with your friend, only you can decrypt the message (retrieve the plaintext from the ciphertext).

In this simple example, the table that maps one word to the other is the secret knowledge that must be shared between the two of you to be useful, so it is called a *shared key*. This is similar to the way both (or all) of your parents can open the front door to your home: they share two copies of the same key to the same lock.

Moreover, since the same key is used both to encrypt the plaintext and also to decrypt the ciphertext, we call this a *symmetric* key.

## Schemes (algorithms)

> :construction: TK-TODO

# Forget the computer: Understanding decoder rings

> :construction: TK-TODO
>
> Decoder ring (aka Ceasar cipher, transposition cipher, etc)
>
> https://www.exploratorium.edu/ronh/secret/secret.html

![Animated GIF of a decover ring](https://web.archive.org/web/20200507231338if_/https://d18l82el6cdm1i.cloudfront.net/uploads/mJjzGTfhA5-121448.gif)

# One-time pad
# Pseudo-random number generator (PRNG) such as RC4

# Additional references

* [Code: The Hidden Language of Computer Hardware and Software](https://en.wikipedia.org/wiki/Code:_The_Hidden_Language_of_Computer_Hardware_and_Software)