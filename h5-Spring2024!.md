# [€ Schneier 2015: Applied Cryptography](https://learning.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/10_chap02.html#chap02-sec003)

## 2.3 ONE-WAY FUNCTIONS

One-way functions characteristics:

- They don't truly exist.
- They are easy to compute but difficult to reverse.
- In their simple form they are not useful for cryptography as you can only encrypt but not decrypt.
- The trapdoor one-way function though, can be used for cryptography as it allows, through the use of the secret trapdoor, to decrypt the message with ease.

## 2.4 ONE-WAY HUSH FUNCTIONS

- One-way has values are fundamental in modern cryptography.
- They compress variable-length input strings into fixed-length output strings, providing a "fingerprint" of the original data.
- While easy to compute in one direction, they are computationally difficult to reverse, ensuring security.
- They are public. And for that reason widely used for file verification and ensuring data integrity.
- They are crucial in financial transactions to prevent unauthorized changes to transaction amounts.
- Hash functions without a key allow anyone to verify the hash, while those with a key restrict verification to designated recipients.
- A Message Authentication Code (MAC) is a one-way has function with a key. That allows a user to check a has only if they key is in his possesion.


