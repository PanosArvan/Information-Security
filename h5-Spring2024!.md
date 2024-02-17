# [€ Schneier 2015: Applied Cryptography](https://learning.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/10_chap02.html#chap02-sec003)

### 2.3 ONE-WAY FUNCTIONS

One-way functions characteristics:

- They don't truly exist.
- They are easy to compute but difficult to reverse.
- In their simple form they are not useful for cryptography as you can only encrypt but not decrypt.
- The trapdoor one-way function though, can be used for cryptography as it allows, through the use of the secret trapdoor, to decrypt the message with ease.

### 2.4 ONE-WAY HUSH FUNCTIONS

- One-way has values are fundamental in modern cryptography.
- They compress variable-length input strings into fixed-length output strings, providing a "fingerprint" of the original data.
- While easy to compute in one direction, they are computationally difficult to reverse, ensuring security.
- They are public. And for that reason widely used for file verification and ensuring data integrity.
- They are crucial in financial transactions to prevent unauthorized changes to transaction amounts.
- Hash functions without a key allow anyone to verify the hash, while those with a key restrict verification to designated recipients.
- A Message Authentication Code (MAC) is a one-way has function with a key. That allows a user to check a has only if they key is in his possesion.


## HashCat

First I updated the system with sudo apt-get update:

![one](https://github.com/PanosArvan/Information-Security/assets/145275148/dd43019e-d62c-4eb5-8eb8-32067d1f5c23)

Then I installed hascat:

![two](https://github.com/PanosArvan/Information-Security/assets/145275148/e7124a86-94b3-4b9d-89b5-eca68affd56a)

Then I created a directory and got a dictionary of leaked passwords:

![three](https://github.com/PanosArvan/Information-Security/assets/145275148/1be04e8b-b1b7-4ed6-919a-e8eea29b1ca7)

I unzipped the the tar text file and got some info about the file:

![four](https://github.com/PanosArvan/Information-Security/assets/145275148/8751375a-b727-4e6b-adda-586a30b13b15)

Here I use hashid -m to identify a random hash:

![five](https://github.com/PanosArvan/Information-Security/assets/145275148/fab11661-0503-405c-aea4-a818942afb8b)

Then with the hashcat -m "hash" -o solved I was able to crack the code:

![six](https://github.com/PanosArvan/Information-Security/assets/145275148/1e7d0c98-d6f5-4152-a143-73363244b209)

![seven](https://github.com/PanosArvan/Information-Security/assets/145275148/2ceea95f-3a46-4df5-a307-378a96fd8aa6)

The answer was: summer.

![seven1](https://github.com/PanosArvan/Information-Security/assets/145275148/7b18b1bd-e3b0-400b-acb4-9cbd6cfe99d2)

Afterwards I tried with this has: 8eb8e307a6d649bc7fb51443a06a216f.

![eight](https://github.com/PanosArvan/Information-Security/assets/145275148/0a5553f1-9547-4034-8ba2-7ddf823a4783)

I'll use MD5 again and see the results I will get:

![nine](https://github.com/PanosArvan/Information-Security/assets/145275148/7de52436-994d-4032-a708-6c03c1679450)

![nine1](https://github.com/PanosArvan/Information-Security/assets/145275148/6979b64d-b61f-4d38-bc92-c71be3c3c302)

And the result is: February. It is also showing the previous hash search. Quite usefull to keep track.

![ten](https://github.com/PanosArvan/Information-Security/assets/145275148/798d81c3-9e55-472e-888d-09306db37b80)


## Password Managers

Source: ![National Cybersecurity Alliance](https://staysafeonline.org/online-safety-privacy-basics/password-managers/)

