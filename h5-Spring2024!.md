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

Source: [National Cybersecurity Alliance](https://staysafeonline.org/online-safety-privacy-basics/password-managers/)
[Tero Karvinen h5 Spring 2024!](https://terokarvinen.com/2024/information-security-2024-spring/#h5-spring2024)
Here is a list of a few password managers as recommended by many online sources:

- Keeper
- Bitwarden
- 1Password
- NordPass
- Dashlane
- LastPass
- pass
- KeePassXC

### Information regarding Password Managers

Threats it Protects Against:

- Password Theft:

KeePassXC protects against password theft by securely storing all passwords in an encrypted database, making it difficult for attackers to access them.
Phishing Attacks: It helps users avoid falling victim to phishing attacks by allowing them to generate strong, unique passwords for each website, reducing the risk of credentials being compromised.
Keylogging: KeePassXC can mitigate the risk of keylogging attacks by offering a feature to auto-type passwords into websites, bypassing the need for manual typing.
Brute Force Attacks: It utilizes strong encryption algorithms and key derivation functions to make it computationally expensive for attackers to crack passwords through brute force.

- Encrypted Information:

KeePassXC encrypts all sensitive information stored in its database, including passwords, usernames, notes, and other metadata associated with each entry.
Non-encrypted information typically includes the entry titles and group names.

- License:

KeePassXC is licensed under the GNU General Public License (GPL) version 2.0 or later. This license allows users to use, modify, and distribute the software freely, provided they adhere to the terms of the license, such as maintaining the copyright notice and sharing any modifications under the same license.

- Data Storage:

By default, KeePassXC stores the encrypted database locally on the user's device, whether it's a computer, smartphone, or other compatible device.
Users have full control over where they choose to store the database file, whether it's on their local hard drive, an external drive, or a cloud storage service.

- Data Protection:

KeePassXC employs strong encryption algorithms such as AES (Advanced Encryption Standard) to protect the contents of its database.
The database is secured with a master password, key file, or both, adding an additional layer of security.
Additionally, KeePassXC offers features like two-factor authentication (2FA) integration and secure clipboard handling to further enhance data protection.


### Use of Password Manager

I decided to trust Tero Karvinen's recommendation for password manager, so I went with KeePassXC.

First step was to download it following the directions from the website [KeePassXC](https://keepassxc.org/)

![keepassXC1](https://github.com/PanosArvan/Information-Security/assets/145275148/1a9a0821-6b52-4f9b-a7f5-0a933055c1be)

![keepassXC2](https://github.com/PanosArvan/Information-Security/assets/145275148/d977a83f-aace-48e4-bcd1-3f5c00df6ab2)

![keepassXC3](https://github.com/PanosArvan/Information-Security/assets/145275148/12e68287-4287-446b-ab57-ba9d3cfb6c0a)

And here it is opened:

![keepassXC4](https://github.com/PanosArvan/Information-Security/assets/145275148/3f96a7d2-6768-46e5-9c36-b81f2c10ea67)

![keepassXC5](https://github.com/PanosArvan/Information-Security/assets/145275148/63d968c7-1d9a-4788-8ca2-55c4114c0987)

First I can create a new database and go through some of the options available regarding security, the best options are mostly used:







