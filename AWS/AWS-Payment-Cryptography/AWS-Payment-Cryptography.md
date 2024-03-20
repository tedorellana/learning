# AWS-Payment-Cryptography

## Topics

### Translate PIN:
- Translate the PIN data from onse set of keys to another wihout expose the encrypted data. Process performed in the HSM.
- Used for P2PE encryption where the working keys should change but the processing system does not need or is not permitted to decrypt the data.
- Inputs:
  - Encrypted data.
  - Encryption key used to encrypt.
  - Parameters used to generate input values.
  - Key to encrypt the output.
  - Parameters to generate the output.
- Output:
  - New encrypted dataset
  - Parameters to generate the encrypted dataset.

### P2PE (Point to point encryption)
- Encryption standard established by PCISSC (Payment Card Industry Security Standards Council).
- Cardholder information is encrypted immediately after card is used by a point-of-sale and isn´t decrypted until it has beend processed by the payment processor.

### DUKPT (Derived Unique Key Per Transaction)
- Key management standard used to define use of one-time encryption keys on phyisical devices (POSs).
- Usually leverages 3DES.

### AWK (Acquire Working Key)
- Used to exchange data between an acquireer/acquirer processor and a netowrok.
- Leverages 3DES.
- 

### Triple DESS
- Key length used for this encryption is 168 bits (3x56).
- Effectivity is just 112 bits.
- Is being replacing by AES.
- Typically used for credit cards or other electronic payments.
- 64 bit per block.

Steps to encrypt:
  1. Encrypt with key 1 DES.
  2. Decrypt with key 2 DES.
  3. Encrypt with key 3 DES.

### AES (Advanced Ecnryption Standard)
- Is a cipher blocks system with a permanent length of 128 bits per block.
