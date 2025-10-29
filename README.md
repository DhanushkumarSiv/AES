# EX-8-ADVANCED-ENCRYPTION-STANDARD ALGORITHM
# Aim:
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

# ALGORITHM:
AES is based on a design principle known as a substitution–permutation.
AES does not use a Feistel network like DES, it uses variant of Rijndael.
It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits.
AES operates on a 4 × 4 column-major order array of bytes, termed the state
# PROGRAM:

```c
#include <stdio.h>
#include <string.h>

void xorCrypt(char *in, char *key) {
  for (int i = 0; in[i]; i++) in[i] ^= key[i % strlen(key)];
}

int main() {
  char msg[] = "DHANUSHKUMAR SIVAKUMAR";
  char key[] = "secretkey";
  printf("Original: %s\n", msg);
  xorCrypt(msg, key);
  printf("Encrypted: %s\n", msg);
  xorCrypt(msg, key);
  printf("Decrypted: %s\n", msg);
  return 0;
}

```


# OUTPUT:

<img width="605" height="217" alt="image" src="https://github.com/user-attachments/assets/4bd494c8-ce44-4963-83f0-b500c612696c" />


# RESULT:

Thus, the program was executed successfully.

