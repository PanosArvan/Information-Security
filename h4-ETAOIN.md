# ETAOIN

## [Schneier 2015: Applied Cryptography: Chapter 1: Foundations](https://learning.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/08_chap01.html#chap01-sec001)

### 1.1 Terminology

A cryptosystem is comprised of the cryptographic algorithm, the ciphertexts, the keys and all the possible plaintexts.
There are two types of algorithms.

Symmetric and Assymetric.

On the symmetric one the encryption and decryption key are the same. Hence the key must remain secret and somehow transferred between the ones that need it. 
On the asymmetric one the keys are different. The encryption key is public and the decryption one is private.

### 1.2 Steganography

Steganography hides secret messages within innocuous ones, employing historical methods like invisible inks or modern techniques like embedding messages within graphic images by altering the least significant bits. This allows for large messages to be hidden inconspicuously. Additionally, Peter Wayner's mimic functions alter messages to resemble other types of content, potentially evading detection by automated scanning systems.

### 1.3 Substitution Ciphers and Transposition Ciphers

Cryptography, in its historical context, primarily involved character-based algorithms, where characters were substituted or transposed within plaintext to generate ciphertext. While modern cryptography operates on bits instead of characters, the underlying principles of substitution and transposition remain.

Substitution ciphers replace plaintext characters with corresponding ciphertext characters. Variants include simple substitution, where each character maps to one ciphertext character; homophonic substitution, where one plaintext character can map to several ciphertext characters; polygram substitution, which encrypts characters in groups; and polyalphabetic substitution, composed of multiple simple substitution ciphers using different keys.

Transposition ciphers maintain the same characters but rearrange their order. Columnar transposition is a common example. Cryptanalysis of these ciphers often involves frequency analysis or other techniques to deduce the original plaintext.

Rotor machines, like the Enigma used in World War II, automated encryption through mechanical wheels wired to perform substitution. Each rotor performs a simple substitution, and their configurations change dynamically during encryption, adding complexity to the cipher. Despite their complexity, rotor machines were eventually broken through cryptanalysis.

While classical cryptography laid the groundwork for modern techniques, including those used in computer security, modern cryptography typically involves more complex algorithms operating on bits rather than characters.

### 1.4 Simple XOR


XOR encryption, a basic bitwise operation, is often used in commercial software but offers minimal security. It involves XORing plaintext with a keyword to generate ciphertext. However, XOR encryption is easily breakable, even without computers. By analyzing coincidences, the key length can be determined, allowing for decryption. Despite its prevalence, XOR encryption should not be relied upon for robust security measures.

### 1.5 One-Time Pads

The one-time pad encryption scheme, developed in 1917, offers perfect security by using a nonrepeating set of truly random key letters to encrypt plaintext. Each key letter is used only once, ensuring security. However, key generation must be truly random, and keys must never be reused. While highly secure, one-time pads are impractical for large data transmissions due to key length requirements and require perfect synchronization between sender and receiver. Despite limitations, they find use in ultra-secure, low-bandwidth channels.

### 1.6 Computer Algorithms

Most common cryptographic algorithms:

1. DES (Data Encryption Standard): It's a symmetric algorithm, which means that the same key is used for encryption and decryption.
2. RSA: Assymetric algorithm, can also be used for digital signatures.
3. DSA (Digital Signature Algorithm): Only used for digital signatures.

### 1.7 Large Numbers

Here the author refers to significantly large numbers that he uses to navigate around examples in the rest of the book.


## Encryption - Decryption through AES and PowerShell

I use Windows PowerShell to encrypt and decrypt files using AES encryption. PowerShell provides access to .NET Framework classes, including cryptographic functions, making it suitable for this task.

At first this is coded in PowerShell:

`# Define the path to the file to encrypt
$fileToEncrypt = "C:\Users\panar\OneDrive - Haaga-Helia Oy Ab\Documents\Folder to be encrypted\file.txt"

# Define the path for the encrypted file
$encryptedFile = "C:\Users\panar\OneDrive - Haaga-Helia Oy Ab\Documents\Folder to be encrypted\encrypted_file.enc"

# Generate a random encryption key
$encryptionKey = [System.Security.Cryptography.Aes]::Create().Key

# Get the file content
$fileContent = Get-Content -Path $fileToEncrypt -Encoding Byte

# Create a new AES encryptor object
$aes = [System.Security.Cryptography.Aes]::Create()
$aes.Key = $encryptionKey
$aes.IV = $aes.Key

# Create a memory stream for encryption
$memoryStream = New-Object System.IO.MemoryStream
$cryptoStream = New-Object System.Security.Cryptography.CryptoStream $memoryStream, $aes.CreateEncryptor(), "Write"

# Encrypt the file content
$cryptoStream.Write($fileContent, 0, $fileContent.Length)
$cryptoStream.FlushFinalBlock()

# Write the encrypted content to the encrypted file
[System.IO.File]::WriteAllBytes($encryptedFile, $memoryStream.ToArray())

# Close streams
$memoryStream.Close()
$cryptoStream.Close()

# Display encryption key (for decryption)
Write-Host "Encryption Key:" $([System.Convert]::ToBase64String($encryptionKey))`
