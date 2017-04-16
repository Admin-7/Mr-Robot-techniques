> [[Wiki|Home]] ▸ [[InfoSec]] ▸ [[CTF-team]] ▸ **Identifying data formats**

During regular computer use and especially when playing [[hacking games|InfoSec#ctfs-and-hacking-games]], we encounter text or numbers that are clearly recognizable as "some kind of code" but that are hard to identify. Examples of such "codes" are long strings of letters and numbers such as `5f4dcc3b5aa765d61d8327deb882cf99`, blocks of text with peculiar endings such as `cGFzc3dvcmQ9bXlwYXNzd29yZA==`, or peculiar sequences of characters with similar prefixes such as `#FC346F` or `0x4869`. This page attempts to assist us in the identification of these data formats, providing a shared knowledge base for quickly looking up and making sense of these strings.

1. [Types of data formats](#types-of-data-formats)
    * [Numerals](#numerals)
    * [Hashes](#hashes)
    * [Encodings](#encodings)
        * [Base64](#base64)
1. [How to recognize data formats](#how-to-recognize-data-formats)
1. [Tools](#tools)

# Types of data formats

When we say "data format," we mean a representation or contents of a singular datum. For the purposes of this guide, this specifically excludes [file formats](https://en.wikipedia.org/wiki/File_format) (such as ZIP archives or executable programs). Instead, we mean an atomic piece of data, such as the value from a form field or the output of a certain function, or the way in which that atomic piece of data is represented, such as a [character encoding](https://en.wikipedia.org/wiki/Character_encoding) scheme.

## Numerals

Numerals are symbols or figures that denote a number. Since "number" is an abstract concept, all concrete uses of this concept (such as in timers or addresses) are instead represented using symbols whose meanings are agreed upon ahead of time. For example, a number represented as `0x12` is "the hexadecimal number denoted by the digits 12, that is, decimal value of eighteen." In this data format, `0x` is not part of the number, but rather a prefix describing the way the number is represented.

* **Hexadecimal**: This format uses the decimal digits and the first six letters of the alphabet to represent hexadecimal numerals.

## Hashes

Hashes are astronomically large numbers used to (usually, uniquely) represent some other contents. Their representation is often defined by standardized hashing algorithms. For example, the MD5 hashing algorithm specifies that its output should be a 33 character long hexadecimal value. In these contexts, a numeral prefix is rarely used; the MD5 hash value of the word `password` is `5f4dcc3b5aa765d61d8327deb882cf99`.

| Hash name | Output length |
|-|-|
| md2 | 32 |
| md4 | 32 |
| md5 | 32 |
| sha1 | 40 |
| sha256 | 64 |
| sha384 | 96 |
| sha512 | 128 |
|ripemd128 | 32 |
| ripemd160 | 40 |
| ripemd256 | 64 |
| ripemd320 | 80 |
| whirlpool | 128 |
| tiger128,3 | 32 |
| tiger160,3 | 40 |
| tiger192,3 | 48 |
| tiger128,4 | 32 |
| tiger160,4 | 40 |
| tiger192,4 | 48 |
| snefru | 64 |
| gost | 64 |
| adler32 | 8 |
| crc32 | 8 |
| crc32b | 8 |
| haval128,3 | 32 |
| haval160,3 | 40 |
| haval192,3 | 48 |
| haval224,3 | 56 |
| haval256,3 | 64 |
| haval128,4 | 32 |
| haval160,4 | 40 |
| haval192,4 | 48 |
| haval224,4 | 56 |
| haval256,4 | 64 |
| haval128,5 | 32 |
| haval160,5 | 40 |
| haval192,5 | 48 |
| haval224,5 | 56 |
| haval256,5 | 64 |

## Encodings

An encoding is scheme for representing some other data (often in some other format) using a different format. This becomes necessary when you need to make use of some data with a system that has technical limitations, such as when attempting to type emoji inside of a Web address, or sending a binary file attachment through a text-based messaging system like email. Like hashes, encodings are often defined by public standards and thus have easily-recognizable patterns.

### Base64

This format encodes base 64 numerals by representing each digit as an ASCII character. Usually ends with `==`.

### Percent-encoding

This format encodes arbitrary byte values by representing each value as a two-character hexadecimal digit prefixed by a percent character (`%`). For example, `%41` is equivalent to `0x41` which, in the context of a Web address (a URL), is equivalent to the character `A`.

# How to identify a data format

The following is a generalized process for going about identifying what kind of data you might be looking at. It relies heavily on context (situational awareness) and experience.

1. Consider the context. Did you encounter this data format in a file? As part of a Web address, etc?
1. Look for multiple encodings. Sometimes, data is multiply-encoded for various different contexts, like wrapping a box with different layers of wrapping paper. For example, a message might first be Base64-encoded for use in a Web application before being further URL-encoded; you'll first need to recognize the URL-encoding, then the fact that the message has been Base64-encoded.
1. …

## Tools

* [`hash-identifier`](http://tools.kali.org/password-attacks/hash-identifier) - Software to identify the different types of hashes used to encrypt data and especially passwords.
* [`HashTag.py`](https://github.com/SmeegeSec/HashTag) - A python script written to parse and identify password hashes.