# Task 1 – Steganography & Base64

## Challenge

A hidden Base64 string was embedded inside an image.  
The goal was to decode it and identify the password.

### Base64 Payload


## Approach

1. Extract the Base64 text from the image (already provided in the assignment).
2. Decode the Base64 string.
3. Read the plaintext output to identify the password.

### 🔧 Tools used

- CyberChef (online Base64 decoder)
- Python script (`decode_base64.py`)

### Decoding with CyberChef

Steps:
1. Open https://gchq.github.io/CyberChef/
2. Paste Base64 string
3. Apply "From Base64"
4. Output reveals the hidden password

### Decoding with Python

## Key learning

- Base64 is not encryption — just an encoding method  
- Useful for identifying hidden data in steganography challenges  
- Good practice for quick triage of suspicious encoded strings


Run:
