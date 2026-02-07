# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:
# Program:
```
import numpy as np
import math
L = 0
hs = 0
p = []
lk = []
n = int(input("Enter the number of Samples : "))
for i in range (n):
  pr = float(input(f"Enter the probability of sample values {i + 1}:"))
  p.append(pr) # Moved inside the loop
for j in range (n):
  l = float(input(f"Enter the length of the sample values {j + 1}:"))
  lk.append(l) # Moved inside the loop
# Avg length of the code word
for k in range (n):
  Avg1 = p[k] * lk[k]
  L = L + Avg1 # Moved inside the loop
# Entropy
for k in range (n):
  e = p[k] * math.log(1 / p[k], 2)
  hs = hs + e # Moved inside the loop
hs = round(hs,3)
# Efficiency
eff = hs / L
eff = round(eff,3)
# Redundancy
red = round(1 - eff,3)
# Variance
var = 0
for k in range(n):
  var1 = p[k] * (lk[k]-L)**2
  var = var + var1 # Moved inside the loop
var = round(var,3)
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff}")
print(f"Redudancy is : {red}")
print(f"Variance is : {var}")
```
# Calculation:
![WhatsApp Image 2026-02-07 at 2 21 15 PM](https://github.com/user-attachments/assets/5a73be78-40c7-4693-9b58-46979c9afef9)
![WhatsApp Image 2026-02-07 at 2 21 15 PM (1)](https://github.com/user-attachments/assets/afa78131-35e3-45a4-9229-a273c0a8bd5a)




# Output
Average Codeword Length is : 2.625

Entropy is : 2.625

Efficiency is : 1.0

Redudancy is : 0.0

Variance is : 0.484
# Results:
For the given discrete memoryless source with probabilities
{0.125,0.0625,0.25,0.0625,0.125,0.125,0.25}, both Huffman and Shannon–
Fano coding were applied. The simulation was carried out in Python
(Google Colab). Since the source probabilities are exact powers of
two, the codeword lengths match the ideal values, giving zero
redundancy and 100% coding efficiency. Both Huffman and Shannon–Fano
yield identical results.
