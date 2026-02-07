# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.55,0.15,0.15,0.1,0.05} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Program:
import math

# Probabilities given
p = [0.55,0.15,0.15,0.1,0.05]

# Corresponding Huffman/Shannon-Fano code lengths
lk = [1,3,3,3,3]
n = len(p)

# Average Codeword Length
L = sum(p[k] * lk[k] for k in range(n))

# Entropy
hs = sum(p[k] * math.log(1 / p[k], 2) for k in range(n))
hs = round(hs, 3)

# Efficiency & Redundancy
eff = round(hs / L, 3)
red = round(1 - eff, 3)

# Variance of codeword length
var = sum(p[k] * (lk[k] - L) ** 2 for k in range(n))
var = round(var, 3)

print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff * 100}%")
print(f"Redundancy is : {red}")
print(f"Variance is : {var}")

# calculations
<img width="973" height="1140" alt="image" src="https://github.com/user-attachments/assets/4382a79e-3401-4110-9e3c-3bef175301d8" />

<img width="804" height="1280" alt="image" src="https://github.com/user-attachments/assets/8912f2ee-ff08-4036-a5bb-3c5607dd7624" />

# Output
<img width="324" height="144" alt="Screenshot 2025-09-19 092450" src="https://github.com/user-attachments/assets/df27fe19-79fc-403d-80af-5c222a08ef04" />


# Results:
Hence the average code word length, entropy, variance, redundancy, and efficiency are found for  {0.55,0.15,0.15,0.1,0.05} usinf huffman
