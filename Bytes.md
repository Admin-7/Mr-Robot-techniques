[[Wiki|Home]] ▸ [[Foundations]] ▸ **Bytes**

# What is a *byte*?

If you've never encountered the term "8-bit byte" before, this part might be confusing. All an 8-bit byte means is "a group of 8 binary digits." Any single series of binary digits that we treat as a single value is called a "byte." The length of the series can technically be whatever you like, but is almost universally agreed to be exactly eight. Hence the 8 in "*8*-bit byte."

Similarly, a *bit* is more verbosely termed a *binary digit*, and it's simply a number written in base 2. In base 2 numerical notation, the decimal (base ten) numbers `0` and `1` are written just as you'd expect (`0`, and `1`, respectively), but the number "two" is written as `10` (pronounced like "1 two and 0 ones"), not `2`. As you can see, we must group at least two bits together to represent the number "two," giving us a "2-bit byte." By the same logic, the number "three" is written as `11` in binary because this represents "1 two and 1 ones," which sums to three. We still only need two bits to do this. But continuing this pattern gives us `100` for "four" because this is "1 four, 0 twos, and 0 ones," and now we are forced to group at least three bits one after the other to represent the number we want to express, giving us "3-bit bytes."

Computer manufacturers continued this pattern until they settled on an agreement with software engineers to use 8-bit bytes unless otherwise stated, making it the conventional default for the overwhelming majority of systems we use today. This agreement to use 8-bit bytes made hexadecimal very handy. Each hexadecimal digit, with its sixteen possible values (zero through fifteen), needs four bits to represent it, as shown in the following table:

| Hexadecimal number | 8's place (fourth bit) | 4's place (third bit) | 2's place (second bit) | 1's place (first bit) | Pronounced                          |
|--------------------|------------------------|-----------------------|------------------------|-----------------------|-------------------------------------|
| 0                  | 0                      | 0                     | 0                      | 0                     | "0 eights, 0 fours, 0 twos, 0 ones" |
| 1                  | 0                      | 0                     | 0                      | 1                     |                                     |
| 2                  | 0                      | 0                     | 1                      | 0                     |                                     |
| 3                  | 0                      | 0                     | 1                      | 1                     |                                     |
| 4                  | 0                      | 1                     | 0                      | 0                     |                                     |
| 5                  | 0                      | 1                     | 0                      | 1                     |                                     |
| 6                  | 0                      | 1                     | 1                      | 0                     |                                     |
| 7                  | 0                      | 1                     | 1                      | 1                     |                                     |
| 8                  | 1                      | 0                     | 0                      | 0                     |                                     |
| 9                  | 1                      | 0                     | 0                      | 1                     |                                     |
| A                  | 1                      | 0                     | 1                      | 0                     |                                     |
| B                  | 1                      | 0                     | 1                      | 1                     |                                     |
| C                  | 1                      | 1                     | 0                      | 0                     |                                     |
| D                  | 1                      | 1                     | 0                      | 1                     |                                     |
| E                  | 1                      | 1                     | 1                      | 0                     |                                     |
| F                  | 1                      | 1                     | 1                      | 1                     | "1 eight, 1 four, 1 two, and 1 one" |

Four bits of an "8-bit byte" is exactly half, meaning that one 8-bit byte can be represented with exactly two hexadecimal digits. That's why you'll so often see two hexadecimal digits used to represent the numeric value of a single byte.