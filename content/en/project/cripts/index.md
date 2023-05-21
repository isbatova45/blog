---
title: Asymmetric Encryption
summary: Public key encryption methods - implementation scheme, advantages and disadvantages, the most famous systems
tags:
  - Deep Learning
date: '2023-05-05T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: Photo by rawpixel on Unsplash
  focal_point: Smart


url_code: ''
url_pdf: ''
url_slides: ''
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: example
---

In public-key encryption, each party creates a pair of keys, a public key and a private key. These keys are linked to each other, so a message encrypted with the public key can only be decrypted with the corresponding private key.
An important point is that when creating keys, it is possible to generate very large numbers in such a way that, knowing the public key, it is impossible to calculate the private key in any way. Thus, ensuring reliable encryption of messages is based on the knowledge of the private key exclusively by its owner. The idea of asymmetric encryption is based on a complex mathematical question that allows you to build one-way functions. Given x, the function y = f(x) is easily determined. But at the same time, it is very difficult to calculate x from a known value of y. y is used as the public key and x as the private key. For all encryption methods with a public key, the absence of other methods has not been mathematically strictly proven; the calculation of the private key by brute force. Cryptosystems with public keys differ in the form of one-way functions.

If it is necessary to transfer information from the interlocutor to the interlocutor, a single scheme for the implementation of asymmetric encryption operates. To begin with, the first interlocutor chooses an algorithm and a pair of public and private keys. The public key is sent to the second interlocutor over an open, insecure channel. After that, the second interlocutor encrypts the information using the sent public key and sends the received cipher back to the first interlocutor, who decrypts the message using the private key created at the beginning. At the same time, if it is necessary to establish a communication channel in both directions, then operations before decrypting messages are performed by both interlocutors. Thus, everyone will know their private, public keys and the public key of the interlocutor.

Thus, if we denote by EA the public key of the interlocutor A, by DA the private key of the interlocutor A, then v=EA(u) is the result of encrypting the message u, and u=DA(v) is the result of decrypting the message v. In this case, the transformations must be such that for any u the equality DA(EA(u))=u holds true.

Public key cryptography is used as an independent means of protecting information, as well as a means of distributing keys, and as a means of user authentication. However, like any system, this encryption method has its advantages and disadvantages relative to symmetric encryption.

The advantages include the absence of the need to transfer the secret key over a reliable channel and the knowledge of the decryption key by only one of the interlocutors. In addition, in large networks, the number of keys will be significantly less than in a symmetrical system.
The disadvantages include the complexity of making changes to the algorithm, longer keys, a slower process of encrypting and decrypting a message, and the need for more computing resources to use.

Let's take a look at some of the most famous systems based on encryption using a public key.

In 1977, scientists at the Massachusetts Institute of Technology developed the RSA encryption algorithm based on the factorization problem (the factorization problem). This system was named RSA after the first letters of the names of scientists and became the first algorithm suitable for both encryption and digital signature.
In this algorithm, prime numbers p and q are chosen, which are kept secret, and only their product N=p*q and the encryption key (public key) are published. The private key, that is, the decryption key, is secret and is generated using knowledge of the factorization of the numbers N (that is, knowledge of p and q).

The ElGamal system is based on the difficulty of computing discrete logarithms in finite fields. Includes encryption algorithm and digital signature algorithm. The scheme was proposed by Taher El-Gamal in 1984. In fact, he developed one of the variants of the Diffie-Hellman algorithm .: he improved the system and received two algorithms that were used for encryption and for authentication. But ElGamal's algorithm was not patented and therefore became a cheaper alternative, as there were no license fees to pay. The algorithm is believed to be covered by the Diffie-Hellman patent.

McEliece's system is based on algebraic coding theory (decoding of complete linear codes) and was the first scheme to use randomization in the encryption process. Designed by Robert McAlice in 1978.
For the private key, a binary error-correcting Gopp code is chosen, for which an efficient decoding algorithm (Peterson's algorithm) is known. The public key is obtained by disguising the selected code as a complete linear one.

In conclusion, I want to say that asymmetric encryption is more secure than symmetric encryption. Public key cryptographic systems are currently widely used in various network protocols, in particular, in the TLS protocols and its predecessor SSL (underlying HTTPS), in SSH. Also used in PGP, S/MIME.
