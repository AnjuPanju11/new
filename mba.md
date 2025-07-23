 
---

## 🔹 1. What is Entropy?

**Definition:**  
Entropy measures the average information or uncertainty in a message.

**Formula:**  
H = – ∑ P(x) × log₂ P(x)

**Example:**  
If you always get same reply from a friend (“Yes”), entropy is low. If reply changes often, entropy is high.

**Trick:**  
Entropy = Surprise level.  
No surprise = low entropy, full guessing = high entropy.

---

## 🔹 2. Shannon-Fano Coding (for M = 2, M = 3)

**Definition:**  
It’s a coding technique where frequent symbols get shorter codes.

**Steps:**  
1. Arrange symbols by decreasing probability  
2. Divide into equal probability groups  
3. Assign binary digits  
4. Repeat until all symbols are coded

**Example:**  
Texting: You use “k” for “okay” often (short code for frequent word).

**Trick:**  
Frequent = short  
Rare = long

---

## 🔹 3. Redundancy and Uncertainty

**Definition:**  
- Redundancy: Extra bits added for error detection  
- Uncertainty: Not knowing what message comes next

**Example:**  
- Saying “Hello Hello” on a bad call = Redundancy  
- Tossing coin = Uncertainty

**Trick:**  
Redundancy = Safety  
Uncertainty = Guessing

---

## 🔹 4. Find Entropy of Given Probabilities

**Definition:**  
Use entropy formula with given probabilities.

**Example:**  
P = [1/2, 1/4, 1/8, 1/16, 1/32, 1/32]  
Plug into formula to get H.

**Trick:**  
More variation in P → more surprise → more entropy.

---

## 🔹 5. Bernoulli & Poisson Process

**Definition:**  
- Bernoulli: Binary outcomes (Success/Fail)  
- Poisson: Random events in time (like number of calls per hour)

**Example:**  
- Tossing coin = Bernoulli  
- Cars passing in 1 hour = Poisson

**Trick:**  
Bernoulli = Binary  
Poisson = Phone calls

---

## 🔹 6. BCH Codes

**Definition:**  
BCH is an error-correcting code that fixes multiple-bit errors.

**Example:**  
Used in CDs, QR codes where small damage still lets us read data.

**Trick:**  
BCH = Big Correction Helper

---

## 🔹 7. Generator Matrix for (6,3) Block Code

**Definition:**  
It’s a matrix used to generate all possible codewords from input data.

**Example:**  
Input (3-bit) × Generator Matrix = Output (6-bit codeword)

**Trick:**  
G matrix = Codeword machine

---

## 🔹 8. CRC (Cyclic Redundancy Check)

**Definition:**  
CRC detects data errors using binary division and remainder.

**Steps:**  
1. Append zeros  
2. Divide by generator  
3. Append remainder = transmitted message

**Example:**  
Used when downloading files or streaming — it checks if data is correct.

**Trick:**  
CRC = Check Received Content

---

## 🔹 9. Diffie-Hellman Key Exchange

**Definition:**  
Method for two people to generate same secret key over public network.

**Example:**  
You and friend both get a shared secret without anyone seeing it.

**Trick:**  
Diffie-Hellman = Digital Handshake

---

## 🔹 10. Confusion and Diffusion

**Definition:**  
- Confusion: Complex relation between key and cipher  
- Diffusion: Spread out message bits over cipher

**Example:**  
1-bit change → Entire cipher changes = high confusion & diffusion

**Trick:**  
Confuse the hacker, Diffuse the message

---

## 🔹 11. Soft vs Hard Decoding & Viterbi Algorithm

**Definition:**  
- Hard decoding: Uses 0/1 directly  
- Soft decoding: Uses signal confidence  
- Viterbi: Decoding method for error correction

**Example:**  
Used in mobile and satellite communications.

**Trick:**  
Hard = Harsh  
Soft = Smart  
Viterbi = Very Best Decoder

---

## 🔹 12. Short Notes

### i) Linear Convolutional Code  
Encodes message using shift registers with memory.  
Used in space/military communication.

### ii) RSA  
Public key encryption with 2 keys (public & private).  
Used in secure websites (https://), digital wallets.

### iii) MDS Code (Maximum Distance Separable)  
Corrects max errors for given code length.  
Used in storage (RAID), cloud backup.

### iv) PGP (Pretty Good Privacy)  
Used in email security. Combines hashing, encryption, digital signature.

---

## 🔹 13. Source Coding Theorem

**Definition:**  
States that average code length ≥ entropy.  
Ideal code is as short as possible but still lossless.

**Example:**  
You can’t compress a file smaller than its entropy without losing info.

**Trick:**  
Source coding = Short but lossless

---

## 🔹 14. Symmetric vs Asymmetric Encryption

**Definition:**  
- Symmetric: Same key for encryption & decryption  
- Asymmetric: Different public/private keys

**Example:**  
- ZIP file with password = Symmetric  
- Online banking = Asymmetric (RSA)

**Trick:**  
Symmetric = Single key  
Asymmetric = A pair of keys

---

## 🔹 15. AES (Advanced Encryption Standard)

**Definition:**  
Block cipher encryption used worldwide. Works on 128-bit blocks.

**Example:**  
Used in WiFi security, government data encryption.

**Trick:**  
AES = America’s Encryption Standard

---

## 🔹 16. Hamming Code

**Definition:**  
Error-detecting and correcting code using parity bits.

**Example:**  
Detects & fixes 1-bit errors in data.

**Steps:**  
1. Add parity bits in 2ⁿ positions  
2. Use XOR to check

**Trick:**  
Hamming = Healing errors


