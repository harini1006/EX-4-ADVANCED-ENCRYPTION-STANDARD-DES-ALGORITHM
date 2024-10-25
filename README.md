# EX-7-DATA-ENCRYPTION-STANDARD ALGORITHM
## DATE:
## Aim:
  To use Data Encryption Standard (DES) Algorithm for a practical application like URL Encryption.

## ALGORITHM: 
  1. AES is based on a design principle known as a substitution–permutation. 
  2. AES does not use a Feistel network like DES, it uses variant of Rijndael. 
  3. It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits. 
  4. AES operates on a 4 × 4 column-major order array of bytes, termed the state

## PROGRAM:
```
Developed by:Harini V
Register no.: 212222230044
```
```
#include <stdio.h>
#include <string.h>


  void xor_encrypt_decrypt(char *input, char *key) {
int input_len = strlen(input);
int key_len = strlen(key);

for (int i = 0; i < input_len; i++) {
    input[i] = input[i] ^ key[i % key_len]; // XOR encryption
}
}

int main() {
char url[] = "https://lms2.ai.saveetha.in/";
char key[] = "secretkey"; // Simple key for XOR encryption

printf("Original URL: %s\n", url);

// Encrypt the URL
xor_encrypt_decrypt(url, key);
printf("Encrypted URL: %s\n", url);

// Decrypt the URL (since XOR is reversible using the same key)
xor_encrypt_decrypt(url, key);
printf("Decrypted URL: %s\n", url);

return 0;
}
```
## OUTPUT:
![{75A1D24A-92FC-410F-8ECF-82A7187FCBF0}](https://github.com/user-attachments/assets/73b6a457-1c07-401e-b149-30eb9b09c15e)


## RESULT: 
Thus , to use Data Encryption Standard (AES) Algorithm for a practical application like URL Encryption is done successfully.
