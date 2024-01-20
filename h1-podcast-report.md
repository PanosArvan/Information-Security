# The Phreaky World of PBX Hacking

-Phone hacking costs companies billions of dollars each year and it keeps increasing.

-One of those ways is to call a company's phone with the expectation of getting to the voice mail and then redirect the forwarding number to their pay-per-min line.

-In that way they can start charging the companies everytime they call it. This works on line phones.

-Some companies use something called a phone branch exchange or PBX. This system gives guidance to the phones how to operate. The system though is online.

-Many of the PBX systems remain unsecured or given to the security contractor that is the least expensive, usually getting subpar quality.

-For a hacker, a PBX system that hasn't been properly set-up is an easy target to penetrate. 

-If they find the IP address of the PBX they can make calls that originate from that office, hence racking up big sums of money to that company's phone bill.

-The FBI will not help unless they have enough data. But reporting is something that most companies want to avoid due to bad publicity.

-Nonetheless, at some point FBI did gather enough data to notice patterns. Their efforts led to two names: Farhan Arshad and Noor Aziz Uddin.

-Those two were put in the Cyber's Most Wanted List with a 50.000$ bounty for any information leading to them.

-Those people fled back to Pakistan where the FIA, the Federal Investigation Agency of Pakistan, got a tip eventually from someone that knew the cellphone number of Uddin.

-Then by tracking the GPS of that phone, they eventually raided his house, where they found both of them. Now they are in jail.

-In total it is claimed they costed 50 million dollars in damages. Before their arrest the two were investing in land and businesses.

## Sources

[EP 1: THE PHREAKY WORLD OF PBX HACKING](https://darknetdiaries.com/transcript/1/)


# Installing Debian

I followed the installation guide. Karvinen 2021: [Install Debian on VirtualBox](https://terokarvinen.com/2021/install-debian-on-virtualbox/)

I didn't encounter an error. I chose Debian 64 bit before hand to avoid the first error that would usually appear.

This is the result of the Debian desktop after getting all the updates and installing Guest Additions.

![Screenshot of my Debian](https://github.com/PanosArvan/Information-Security/assets/145275148/14a88319-f3bf-46a9-94c7-6c13f25a7db6)

# Challenge at Cryptopals - 01 - Hex to Base64

Using python.

First I changed Hex to bytes:

    `hex_string = "49276d206b696c6c696e6720796f757220627261696e206c696b65206120706f69736f6e6f7573206d757368726f6f6d"
    bytes_data = bytes.fromhex(hex_string)

    print("Hex string:", hex_string)
    print("Bytes data:", bytes_data)`

and got this result:

![Screenshot 2024-01-20 144322](https://github.com/PanosArvan/Information-Security/assets/145275148/2506e694-dbab-42e8-a70c-bf21eab0adfe)

Then I changed bytes to Base64:

    `import base64

    hex_string = "49276d206b696c6c696e6720796f757220627261696e206c696b65206120706f69736f6e6f7573206d757368726f6f6d"
    bytes_data = bytes.fromhex(hex_string)

    base64_encoded = base64.b64encode(bytes_data).decode('utf-8')

    print("Hex string:", hex_string)
    print("Bytes data:", bytes_data)
    print("Base64 encoded:", base64_encoded)`

In order to do that I had to add "import base64" and base64.b64encode.().decode() which was referenced from this site: [docs.python](https://docs.python.org/3/library/base64.html)

The "print("Bytes data:", bytes_data)" line is unneccessary but I chose to keep it to see the middle input also.

[ChatGPT](https://chat.openai.com/) was also used to get an idea of how to proceed as posts in forums had many variations on how to proceed. I found python to somehow be simpler.
