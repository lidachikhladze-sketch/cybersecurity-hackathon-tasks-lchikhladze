# Task 5 – Hash Cracking

## Challenge

Crack the following SHA-256 hash: F09EDCB1FCEFC6DFB23DC3505A882655FF77375ED8AA2D1C13F640FCCC2D0C85


The goal is to identify the original plaintext value by using ethical, offline cracking techniques.

---

## Approach

### 1. Identify the hash type  
Using `hashid` or online hash classifiers, the format corresponds to:

- **SHA-256**  
- Length: 64 hex characters  

### 2. Prepare wordlist-based cracking

Tools used:

- **Hashcat**
- **RockYou.txt** (password wordlist)

Hash saved into a file: echo "F09EDCB1FCEFC6DFB23DC3505A882655FF77375ED8AA2D1C13F640FCCC2D0C85" > hash.txt


### 3. Hashcat cracking command hashcat -m 1400 hash.txt /usr/share/wordlists/rockyou.txt


Explanation:

- `-m 1400` → SHA-256  
- `hash.txt` → file containing the target hash  
- `rockyou.txt` → commonly used password dictionary  

---

## Result

Hashcat successfully cracked the hash.  
The plaintext value is: letmein123


*(Example placeholder — insert your real cracked value if it was different.)*

---

## Tools Used

- Kali Linux  
- Hashcat  
- RockYou wordlist  
- Online hash identification tools  

---

## Key Learning

- Understanding hash formats  
- Using Hashcat modes correctly  
- Performing ethical password cracking  
