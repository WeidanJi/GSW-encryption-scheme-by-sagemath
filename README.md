# Ring-GSW

This is an implemention of ring GSW cryptosystem. Cite the paper: "Bootstrapping Fully Homomorphic Encryption with Ring Plaintexts Within Polynomial Noise".

## KeyGen

p<<q, such as p = 3, q = 2**20

The plaintext is a ring element over R_p.

The public key is A = [a, b]^T, b = as+pe.

The secret key is t = [-s, 1].

## Encrypt, Decrypt

The encryption is C = AR+mG, R is a random matrix over {0,1}, G = [g^T, 0\\0, g^T] is a gadget matrix.

The decryption is m = <t, C_k>_q mod p. 

The correctness is ||eR||<q/2, (m+peR) mod p = m. 


