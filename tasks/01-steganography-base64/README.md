# Task 1 – Steganography & Base64

## Challenge

> A hidden Base64 string is embedded in an image.  
> Decode it and identify the password.

We are given a Base64-encoded string extracted from the image:

```text
cGFzc3dvcmQ6MTIzNDU2Nzg5MA==

Approach

Extract the Base64 payload from the image (this step was provided in the assignment).

Decode the Base64 string.

Identify the password contained in the decoded text.

I used CyberChef (online tool) to decode the string, as well as a simple Python script included in this folder.

Using CyberChef

Open: https://gchq.github.io/CyberChef/

Paste the string: cGFzc3dvcmQ6MTIzNDU2Nzg5MA==

Add the From Base64 operation.

The decoded output clearly shows the password in plain text.

Tools used

CyberChef (web-based): Base64 decoding

Key learning

Understanding of basic steganography workflow when the payload is text-based and Base64-encoded.
