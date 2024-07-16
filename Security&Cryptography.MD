Aspects of Security & Corresponding Possible Attacks:
  Confidentiality - only sender and receiver understand message's content              Eavesdrop
  Integrity - message is not altered without detection during transit                  Message Alteration
  Authentication - sender and receiver can both confirm identities of one-another      Impersonation & Hijacking
  Access & Availability - services are accessible and available to users               Access & Availability

Cryptography:

Encryption - the most basic way of data protection

Encryption Types:

  Subsitution Cipher - each unit of plaintext is replaced with corresponding ciphertext, according to the fixed system
  Due to the frequency remaining unchanged, it can be straightforward to decipher, once most common units are deciphered

  Symmetric Key Cryptography - encryption and decryption utilize the same key
  The message is broken into bits of data, which are then segmented, arithmetic operations are then performed between the key and the segments

    Main Algorithms for Symmetric Key Cryptography:
  
        DES - Data Encryption Standard:
          Uses 56 bit symmetric key, requires 64 bit plaintext input (if too long, separated in 64-k bit parts with k-bit padding)
          16 identical rounds of encryption, producing 64 bit output
          Was encryption standard in the US in 1993
          Can be bruteforced in less than a day, using modern computer
          3-DES -> Applying DES 3 times to each data block, provide more security, but also slower
  
        AES - Advanced Encryption Standard:
          Uses 128/192/256 bit symmetric key
          Requires 128 bit plaintext input
          10, 12, 14 rounds of encryption, producing 128 bit output
        Replaced DES in 2001
        Takes 1 billion billion years to bruteforce using modern computer (can be quicker if using quantum computer)

  Assymetric Key Cryptography - uses pair of keys, public and private

    RSA - one of the first assymetric key cryptography algorithms, invented in 1977 by Ron Rivest, Adi Shamir and Leonard Adleman, relevant to this day in various applications

    RSA meets encryption requirements:
      1)
      2)

    Algorithm:
      1) Generate Key: Choose large prime numbers p & q, calculate n = p*q, calculate z = phi(n) = (p-1)*(q-1), choose integer e such that: 1<e<z & e is coprime to z, solve for d: (ed) mod z = 1; e -> public exponent, d -> private exponent

      Public Key -> (n, e); Private Key -> (n, d)

      2) Encryption: Ciphertext C = Plaintext M^e mod n, using public key  (For confidentiality)
      3) Decryption: M = C^d mod n
      4) Signing: Signature S = M^d mod n, using private key  (For authenticity)
      5) Verifying: M = C^e mod n, using public key

    Segmentation: In case that plaintext is too long, it is segmented into fixed blocks that are sized smaller than n, this allows for efficient encryption/decrtyption for long messages

    
    Main issue of RSA: Requires exponentiation of huge numbers, therefore it is computantionally intensive, DES in comparison is 100x quicker.

    One possible solution: session key

    We use public-key cryptography to establish a secure connection, meaning that we authenticate (the identity of) our host. Then, one party will generate symmetric session key and exchange between sender and receiver using public-key cryptography.

We then use this symmetric session key (instead of the public key) for the subsequent message exchanges throughout the session. See the next chapter for further details.
        
