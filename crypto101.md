# Introduction to Cryptography.

In this brochure our goal is to give you a brief introduction to the Cryptography world and related areas. It is not a comprehensive 
introduction so we provide firther references for you to keep expanding your knowledge about the field of Crypto. Cryptography is a 
very formal field so we mainly provide references to textbooks.

We hope you enjoy it and that it will spark more interest into the Crypto world! Welcome to the Crypto & Privacy Village!

## What is Cryptography?
According to the glossary of the National Institute of Standards and Technology (NIST) we founf the following definition for Cryptography:
"The discipline that embodies the principles, means, and methods for the transformation of data in order to hide their semantic content, 
prevent their unauthorized use, or prevent their undetected modification."

From the same source, another complementary definition of Cryptography is:
"The science of information hiding and verification. It includes the protocols, algorithms and methodologies to securely and consistently 
prevent unauthorized access to sensitive information and enable verifiability of the information. The main goals include confidentiality, 
integrity authentication and source authentication."

## Why do we need Cryptography?
We need to start by defining the three basic services of security:
- *Confidentiality*: preserving authorized restrictions on information access and disclosure, including means for protecting personal privacy and proprietary information.
- *Integrity*: guarding against improper information modification or destruction and ensuring information non-repudiation and authenticity.
- *Availability*: ensuring timely and reliable access to and use of information.

The above definitions are taken from the [NIST SP 800-12 Rev. 1
An Introduction to Information Security](https://csrc.nist.gov/publications/detail/sp/800-12/rev-1/final) and, are best know as the CIA Triad.

So, back to the original question, why do we need Crypto? Well, as humans, we have the basic needs of Confidentiality and Integrity with our own Personal Information (PI) and the information that we use at our jobs. And cryptography help us with keeping our data Confidential but also with Integrity. We do not want a attacker to mess with our data in any form. We want our social messages and e-mail to be confidential and our Personal Health Informatgion (PHI) to be genuine and unaltered. Failure to do so can have strong consequences to our lives.

## Two types of Cryptography
Generaly speacking, the field of Cryptography is divided into two sub-fields: 
- **Symmetric-key Cryptography** or also known as private-key cryptography.
- **Asymmetric-key Cryptography** or also known as public-key cryptography.

### Symmetric-key Cryptography
We have to imaginary users, Alice and Bob. They one to exchange secure messages between them because they are very concious about their Confidentiality and Privacy. In order for Alice and Bob to eschange secure messages, they must use a *encryption schemes* or algorithm to transform their *plain text* messagges into a *ciphertext* message.

In order to secure a message, both, Bob and Alice must get and share a *key*. For instance, Bob wants to send a confidential message to Alice. No body else should be able to read this message but Alice and Bob. They have manage to meet and share a secret key so they both can send each other encrypted messages. So now Bob must take the key and the plain text message for Alice, and pass it through a process known as *encryption* that, by use of the key and a *encryption scheme* will produce a *ciphertext*. Only those in posetionof the secret key are able to read the message. 

In the other end of the communication channel, Alice will receive the ciphertext or encrypted message, and using the shared secret key, will pass the ciphertext trought a *decryption* process in order to get back the plain text. During the decryption proces, the same encryption scheme is used to decrypt the message.

Let's use an image to explain the process.

### Asymmetric-key Cryptography


## References
1. [Privacy Canada](https://privacycanada.net/short-list-of-classical-ciphers/)
2. [Crypto Couple](https://cryptocouple.com/#)