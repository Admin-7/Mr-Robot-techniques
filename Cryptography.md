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
    1. [Ciphers (algorithms)](#ciphers-algorithms)
1. [Naive encryption schemes](#naive-encryption-schemes)
1. [Why we need randomness](#why-we-need-randomness)
1. [Pseudo-random number generators](#pseudo-random-number-generators)
1. [Exclusive OR](#exclusive-or)
1. [One-time pads](#one-time-pads)
1. [Symmetric stream ciphers](#symmetric-stream-ciphers)
1. [Symmetric block ciphers](#symmetric-block-ciphers)
1. [One-way functions](#one-way-functions)
1. [Diffie-Hellman key exchange](#diffie-hellman-key-exchange-dhke)
1. [Public-key cryptography](#public-key-cryptography)
1. [Additional references](#additional-references)

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

When the teacher unfolds the note to reveal what you wrote, he will be able to understand what you said because you did not *encrypt* the message; it was sent *unencrypted*, which is to say that it was never translated away from plaintext. If you had been able to somehow make your message unreadable to everyone except your best friend, you would have turned your plaintext into what we call *ciphertext*.

## Adversaries (eavesdroppers)

In a perfect world, one without authoritarian and boring school systems, there would be no need for you and your best friend to use or care about cryptography because there would be no context in which your communication would be restricted or risk your safety. The teacher would not be a threat to you. However, because we do not live in that perfect world, you have *adversaries* like Mr. Hastings, who are all too eager to *eavesdrop* on the notes you want to pass to your best friend.

The purpose of cryptography is to thwart the efforts of these adversaries. Perhaps counterintuitively, it is precisely because of the presence of your enemies that you have need for such powerful tools like cryptography in the first place.

## Channels (mediums)

A channel is a medium of communication: *how* the information is shared, rather than *what* information is being shared. Earlier, when briefly considered using hand signals to keep your notes from falling into your teacher's hands, what you were considering was an *alternate channel* over which to send your messages. While having multiple channels is useful, they do not necessarily change the nature of the problem.

Any given channel may be at risk of being eavesdropped on, and so simply using a different or multiple channels increases the logistical cost for an eavesdropper, but not necessarily the kind of action they must take to intercept your communications.

## Secrets (keys)

In order to produce a secret language immune from being eavesdropped, both you and your best friend must know this alternate, more private "langugage." Put another way, you must each have shared knowledge. This is, of course, exactly the same as any language, secret or not; try visiting a country where people don't speak the same language as you and you'll have a pretty good idea of what it's like trying to read encrypted messages.

In cryptography, we call this knowledge a *key* and, since the purpose of cryptography is to hide information by encoding (*encrypting*) it into a form that cannot be understood by an adversary, we rely on the *secrecy* of the keys in order to protect us. Without knowing what the key is, e.g., without knowing how to speak the same language, eavesdroppers cannot understand the conversation.

Fundamentally, there are two kinds of keys. For most of human history, there was only ever one kind of key, called a *shared* key (sometiems also called a *shared secret*). This is crypto-speak for the fact that all parties privy to the conversation must have the same knowledge in order to meaningfully participate in that conversation. Put yet another way, this simply means that if you want to speak French to someone who does not yet know that language, you must teach them the language so that you share the same knowledge (an understanding of the French language) with them. Without such shared knowledge, communication is not possible through the "algorithm" called French.

Another term for this kind of key is a *symmetric* key, so termed because the same knowledge is needed both to encrypt (turn the plaintext into the ciphertext) as well as to decrypt (turn the ciphertext back into plaintext). This is how human languages work, of course: if you know English, then you can (more or less) communicate with everyone else who also knows English and there is no other knowledge that must be gained. You don't, for instance, have to know French *and* English. One and only piece of information is needed, a kind of metaphoric "symmetry" in both the composing and the understanding of a given message.

Then in 1874, an academic logician named William Stanley Jevons correctly anticipated the development of an entirely new class of cryptographic key, what we now call an *asymmetric* key. As you can probably infer, these keys are so termed because in and of themselves, they can only perform one side of the encrypt-or-decrypt operation. Either the key can encrypt a plaintext, or it can decrypt a ciphertext, but not both.

This turned out to be a rare and truly revolutionary leap forward, yet a practical asymmetric cryptographic security protocol would not be developed for more than a century. For now, it's simply enough to understand that asymmetric keys are always paired: there is one key for encryption and a different (but "magically" mathemticatically related) key for decryption. Since there are always a pair of two keys for asymmetric cryptography to work, we talk about *key pairs* instead of single shared keys.

You will also hear about asymmetric keys discussed as *public-key* or *public-private* crypto. The term "public" comes from the fact that asymmetric cryptography makes it possible to communicate completely privately despite being under constant observation by your adversary. I.e., it is possible to be *in public* yet have a completely *private* conversation with someone who shares no prior secret knowledge with you whatsoever.

This mathematical understanding, translated into material capability, is what gave birth to the cypherpunk movement, is arguably at the root of hacker culture, and is so fundamentally powerful with such mind-bendingly far reaching implications that governments the world over have been desperately trying to control who can and who can not wield this power. More on that later.

## Ciphers (algorithms)

> :construction: TK-TODO

# Naive encryption schemes

> :construction: TK-TODO: Some notes for now.

For example, let's presume that your secret language just replaces one word with another. Your original plaintext message…

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

By substituting one word for another, we have transformed our plaintext into *ciphertext*. That is to say, we have encrypted it by processing using a very simplistic cipher, which in this case is simply changing one word to a second equivalent word. Of course, the result of this process only has meaning if you know what word it should be mapped back into.

One good thing about this new note is that it's far less risky to send, because Mr. Hastings will not have any idea that it is about him! Unfortuantely, if you do not also tell your friend about your choice of mapping one word to a specific other word, along with exactly which word each should be mapped into, your friend will also have no idea what you're talking about. In other words, if you do not share the *key* with your friend, only you can decrypt the message (retrieve the plaintext from the ciphertext).

In this simple example, the table that maps one word to the other is the secret knowledge that must be shared between the two of you to be useful, so it is called a *shared key*. This is similar to the way both (or all) of your parents can open the front door to your home: they share two copies of the same key to the same lock.
>
> Decoder ring (aka Ceasar cipher, transposition cipher, etc)
>
> https://www.exploratorium.edu/ronh/secret/secret.html

![Animated GIF of a decover ring](https://web.archive.org/web/20200507231338if_/https://d18l82el6cdm1i.cloudfront.net/uploads/mJjzGTfhA5-121448.gif)

# Why we need randomness

> :construction: TK-TODO

# Pseudo-random number generators

> :construction: TK-TODO

# Exclusive OR

> :construction: TK-TODO

# One-time pads

> :construction: TK-TODO

# Symmetric stream ciphers

> :construction: TK-TODO

# Symmetric block ciphers

> :construction: TK-TODO

# One-way functions

> :construction: TK-TODO

# Diffie-Hellman key exchange (DHKE)

Fast forward past most of the 20<sup>th</sup> century. It is now 1976. Although almost no one realizes it, nor would most people even notice its significance for decades to come, the world is about to change forever.

Even though the world has truly unbreakable encryption at its fingertips in the form of strong symmetric ciphers, no one has been able to figure out a safe way of distributing the secrets needed to drive those ciphers. After all, it doesn't matter how good your encryption tools are if the decryption keys are readily available to your adversary. Unfortunately, you can't encrypt the keys themselves, of course, because that's the very thing the recipient of your message needs in order to decrypt your messages!

In other words, assuming you are constantly monitored and surveilled (and, let's be real, that is exactly what the FBI did to Black freedom fighters during and before COINTELPRO, and what the NSA along with other governments are doing to everyone today), how would you and your friend ever be able to telecommunicate without risking your encryption keys themselves being discovered or intercepted by your adversary?

The answer came when two cryptographers born and raised in New York City named [Whitfield Diffie](https://en.wikipedia.org/wiki/Whitfield_Diffie) and [Martin Hellman](https://en.wikipedia.org/wiki/Martin_Hellman) published their paper titled "New Directions in Cryptography." In the paper, Diffie and Hellman described for the first time a mathematically secure method for two people to both come up with the exact same key (a shared secret) while constantly being under active observation by their adversary. Importantly, this method never reveals any information whatsoever that would disclose the secret they independently arrived at.

Their solution, now called *[Diffie-Hellman key exchange](https://en.wikipedia.org/wiki/Diffie%E2%80%93Hellman_key_exchange)*, was deceptively simple and elegant, and is still used to this day. It relies on two key assumptions:

* [Exponentiation](https://en.wikipedia.org/wiki/Exponentiation) is [commutative](https://en.wikipedia.org/wiki/Commutative_property): this is a fancy way of saying that when you multiply a number with another number, it does not matter which number you started with. For example, 4 &times; 2 equals 8, but notice that 2 &times; 4 also equals 8. It doesn't matter if you begin with 4 or begin with 2, as long as you multiply the *same* values. This is, of course, true and no one on Earth is able to change this. So, we're good on this front.
* We have a one-way function to use (in this case, the [discrete logarithm problem](https://en.wikipedia.org/wiki/Discrete_logarithm_records)) in order to make it difficult for an observer to know the inputs of our operations. Thankfully, no cryptographer, mathematician, or three-letter spy agency has ever been able to solve this mathematical problem; the discrete logarithm problem is, in fact, still a one-way function. So, we're good on this front.

For as long as these facts remain true, Diffie-Hellman key exchange is secure, simple, and fast. Here's how it works.

> :warning: The exact values used in this description is (intentionally) *NOT* cryptographically secure. There *are* certain caveats about the properties that each numerical component in a Diffie-Hellman key exchange must satisfy in order to be safe. Please do *not* use these numbers yourself; they are way too small and are intended simply to make understanding the concept easier.

Recall that our goal is to come up with a shared secret key (a big random number) that will drive the encryption scheme we will use to encipher our note to our best friend. However, we are such insubordinate students that we are now being watched all the time. This means we have no covert channels available to us, and must come up with a way to independently arrive at the same shared secret.

Rather than choose a shared secret key (number) directly, we instead publicly agree on a shared number that will serve as the basis for our future number after some clever calculations. This base number is not sensitive information, so we simply signal one another from across the room. Let's say we settle on the number 3.

|                           | You | Friend |
| -                         | --- | ------ |
| Base number ("generator") | 3   | 3      |

Diffie and Hellman called this base number a *generator*, so you'll often see this abbreviated as *g* in mathematical formulas. In real-life applications, it's important that this number has a very specific relationship to the next number we're going to pick (technically a [primitive root modulo N](https://en.wikipedia.org/wiki/Primitive_root_modulo_n)) so whatever we come up with here will have some important restrictions for the next step.

Next, we'll also publicly agree on another number; this also need not be a secret. We're going to use this second number in part of a modulo operation later on. Let's say that, given our prior choice, we decide on the number 17 this time.

|                                | You | Friend |
| -                              | --- | ------ |
| Base number ("generator")      | 3   | 3      |
| Second number ("prime modulo") | 17  | 17     |

Again, in real-life applications, it's important that this second number have certain special properties. To be safe for use in a Diffie-Hellman key exchange, this second number must be a *prime* number (a number evenly divisible only by itself and the number 1), so it's often written as *p* in mathematical formulas.

Finally, we each have to pick one more number. However, it's very important that this last selection remain truly secret. You don't ever share this with your friend, and your friend will not share it with you. Remember, your teacher is still watching. Let's say you (secretly, in your head) pick the number 15. You have no idea what your friend picks, but you trust them to have picked something equally random. Likewise, your friend doesn't know what private random number you picked. Meanwhile, your teacher has observed everything that you have communicated, but since you never communicated your private random number at all, your teacher is as equally ignorant of that as your friend is:

|                                | You | Friend | Teacher saw |
| -                              | --- | ------ | ----------- |
| Base number ("generator")      | 3   | 3      | 3           |
| Second number ("prime modulo") | 17  | 17     | 17          |
| Private random number          | 15  | ?????? | ??????????? |

At this point, believe it or not, we have all the raw materials we need to perform this secret-concocting mathematical "magic trick" right in front of our teacher's very eyes.

The first step we take is to raise the base number to the power of our private random number. "Raising to the power of" just means multiplying over and over again. So, privately (in our "head") we simply do 3 &times; 3, which gives us 9. Now we have 14 more multiplications to perform. So we take 9 and we multiply it by 3 again, giving us 27. We do this another 13 times. This can be more simply written as 3<sup>15</sup> (or, in most computer programming languages, as `3^15`). This gives us fourteen million three hundred forty eight thousand nine hundred seven (14,348,907).

We're not done. Next, we take that very large number and divide it by the second number we publicly agreed on (17, in this example) looking for the *remainder*. This operation is known as modulo, and asks the question "what whole number is left over if we cannot evenly divide the first number by the second number?" In our case, the remainder is 6, because 14,348,907 does *not* evenly divide into 17 at all. That's intentional; we will have left over numbers. It's those numbers we care about. In computer programming languages, this is written as `14348907 % 17`.

Our result for these values is 6. This value is also not going to be our shared secret, but we do have to share it with our friend. Thankfully, this intermediate value is not at all sensitive, so we just send it along to them without fear that it will expose our private number to the teacher. Meanwhile, our friend has performed the exact same calculation, but they used their own random private number instead of ours, and they came up with some result, which they send to us. Suppose they send us the number 12.

|                                | You | Friend | Teacher saw |
| -                              | --- | ------ | ----------- |
| Base number ("generator")      | 3   | 3      | 3           |
| Second number ("prime modulo") | 17  | 17     | 17          |
| Private random number          | 15  | ?????? | ??????????? |
| Our intermediary value         | 6   | 6      | 6           |
| Friend's intermediary value    | 12  | 12     | 12          |

Now comes the real math magic. Recall that when you multiply numbers together, it doesn't matter what order you do the multiplication in. We've already raised the base number by our own private number (3<sup>15</sup>) modulo the second shared number, seventeen (3<sup>15</sup> mod 17).

Let's perform this same calculation, but with our *friend's intermediary value* instead of the original base number: 12<sup>15</sup> mod 17. Our result is 10. This final value is now our shared secret, and we can use it as the key to our symmetric cipher because we can be 100% confident that our friend also got the same exact result as we did.

|                                     | You | Friend | Teacher saw |
| -                                   | --- | ------ | ----------- |
| Base number ("generator")           | 3   | 3      | 3           |
| Second number ("prime modulo")      | 17  | 17     | 17          |
| Private random number               | 15  | ?????? | ??????????? |
| Our intermediary value              | 6   | 6      | 6           |
| Friend's intermediary value         | 12  | 12     | 12          |
| Secret key (12<sup>15</sup> mod 17) | 10  | 10     | ??????????? |

How come we can be so sure that our friend has the same secret key as we have? Let's look at the same process from our friend's point of view this time.

We have publicly agreed on the values of 3 and 17 as our base ("generator") and our special prime. Then our friend came up with a random private number of their own. We don't care what it is, but let's say it was 13. When they performed the intermediary calculation, they sent us an intermediary result of 12, because 3<sup>13</sup> mod 17 equals 12. We then gave them a value of 6, so they performed 6<sup>13</sup> mod 17, which, sure enough, equals 10.

This works because of the commutative property of exponentiation we assumed would be true earlier. Notice that both you and your friend have actually performed mathematically equivalent calculations, just performed in an admittedly confusing way.

* You privately performed 3<sup>15<sup>13</sup></sup> mod 17. This is because the second exponentiation (the 13) was chosen by your friend, not you, and delivered to you already "mixed in" to intermediary base number 12 as the *result* of your friend's original calculation. (12<sup>15</sup> mod 17, the calculation your friend indirectly chose for you, is the same as 6<sup>13</sup> mod 17, the calculation you indirectly chose for your friend.)
* Meanwhile, your friend privately performed 3<sup>13<sup>15</sup></sup> mod 17. Their second exponentiation (the 15) was chosen by you, not your friend.

Look closely and you'll notice that the only difference between your ultimate calculation and your friend's is the order in which you each performed the exponentiation. However, as shown earlier, changing the order of these specific operations does not change the end result for either of you. What it *does* do is keep your private, randomly-chosen numbers, well, private, and also keeps the result of your calculations private. This means, try as they might, your teacher cannot deduce your encryption key, and thus cannot read any messages you now send to one another encrypted with this shared key, even though they were always and are still able to eavesdrop on everything you have been sending to one another.

This mathematical slight of hand forms the start of every security protocol that needs to establish a secure connection, such as loading a bank website or logging in to a remote server via SSH, over an insecure and clearly wiretapped channel such as the Internet.

# Public-key cryptography

> :construction: TK-TODO

# Additional references

* [Code: The Hidden Language of Computer Hardware and Software](https://en.wikipedia.org/wiki/Code:_The_Hidden_Language_of_Computer_Hardware_and_Software)
* [Khan Academy: Diffie-Hellman key exchange](https://www.khanacademy.org/computing/computer-science/cryptography/modern-crypt/v/diffie-hellman-key-exchange-part-2)