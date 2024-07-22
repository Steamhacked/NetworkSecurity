Generate Key:
  Choose p & q - large prime numbers, that product of which -> n is of desired key length
  n = p*q -> key length [bits] -> modulus for both public & private key
  calculate $$z = \phi(n) = (p-1)*(q-1)$$ (Euler's Totient Function)
  choose integer e, such that -> 1 < e < z & e is coprime to z
  find e: solve for d: ed mod z = 1 (modular multiplicative inverse of e)

  (n, e) -> public key, (n, d) -> private key

Encryption:
  C = M^e
Decryption:
  M = C^d
Signing:
  S = M^d
Verifying:
  M = S^e
