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

  Assymetric Key Cryptography
        
