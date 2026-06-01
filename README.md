# EX-NO14-HASH-ALGORITHM

## AIM:
To implement HASH ALGORITHM

## ALGORITHM:

1. Hash Algorithm is used to convert input data (message) into a fixed-size string, typically a hash value, which uniquely represents the original data.

2. Initialization:
   - Choose a hash function \( H \) (e.g., SHA-256, MD5, etc.).
   - The message \( M \) to be hashed is input.

3. Message Preprocessing:
   - Break the message \( M \) into fixed-size blocks. If necessary, pad the message to make it compatible with the block size required by the hash function.
   - For example, in SHA-256, the message is padded to ensure that its length is a multiple of 512 bits.

4. Hash Calculation:
   - Process the message block by block, applying the hash function \( H \) iteratively to produce an intermediate hash value.
   - For SHA-256, each block is processed through a series of logical operations, bitwise manipulations, and modular additions.

5. Output:
   - After all blocks are processed, the final hash value (digest) is produced, which is a fixed-size output (e.g., 256-bit for SHA-256).
   - The resulting hash is unique to the input message, meaning even a small change in the message will result in a completely different hash.

6. Security: The strength of the hash algorithm lies in its collision resistance, ensuring that it is computationally infeasible to find two different messages that produce the same hash value.


## Program:
```
#include <stdio.h>
#include <string.h>

int main() {
    char msg[100];
    unsigned int hash = 0, receivedHash;
    int i;

    printf("Enter message: ");
    scanf("%s", msg);

    for(i = 0; msg[i] != '\0'; i++) {
        hash = hash + msg[i];
    }

    printf("Generated Hash: %X\n", hash);

    printf("Enter received hash: ");
    scanf("%X", &receivedHash);

    if(hash == receivedHash)
        printf("Hash verification successful");
    else
        printf("Hash verification failed");

    return 0;
}
```

## Output:
<img width="1387" height="737" alt="image" src="https://github.com/user-attachments/assets/c17e71bc-ccd9-4448-9b7b-6c1c11e9e344" />

## Result:
The program is executed successfully.
