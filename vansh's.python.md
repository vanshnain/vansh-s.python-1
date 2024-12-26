# Question 1

```bash
import math

def roots():
  print("Enter the required values to get roots of a quadratic equation.")
  a=int(input("Enter coefficient of x^2: "))
  b=int(input("Enter coefficient of x: "))
  c=int(input("Enter value of the constant: "))
  D=b*b-4*a*c
  rootD=math.sqrt(abs(D))
  if D>0:
    print("The roots of the quadratic equation are real and different. They are:")
    print((-b+rootD)/(2*a))
    print((-b-rootD)/(2*a))
  elif D == 0:
    print("The roots of the quadratic equation are real and equal. Their value is:")
    print(-b/(2*a))
  else:
    print("Roots of the quadratic equation are not real.")
    
roots()
```
### Code output-
![FireShot Capture 026 - Trinket_ run code anywhere - trinket io](https://github.com/user-attachments/assets/353b1cd1-c0b7-4650-94f2-cb4e57501648)

# Question 2

### j)
```bash
n=int(input("Enter a number to be checked: "))

def prime(n):
  
  if n==2:
    print("Entered number is prime.")
    return
  if n==1 or n==0:
    print("Not Applicable")
    return

  flag=0
  for i in range(2,int(n**0.5)+1):
    if n%i==0:
      flag=1
      break
    else:
      flag=0
  if flag==0:
    print("Entered number is prime.")
  else:
    print("Entered number is not prime.")
    
prime(n)
```
### Code output-
![FireShot Capture 027 - Trinket_ run code anywhere - trinket io](https://github.com/user-attachments/assets/7f1578ea-a8e7-4d93-81af-d2f6fa18ddcd)

### k)
```bash
def isPrime(n):

    if(n==1 or n==0):
      return False
  
    for i in range(2,n):
        if(n%i==0):
          return False
    return True

N = int(input("Enter number till which prime numbers are to be generated:"))

for i in range(1,N+1):
  if(isPrime(i)):
    print(i)
```
### Code output-
![image](https://github.com/user-attachments/assets/5d4ea093-6e00-4a6d-84a5-d57ac357274b)

### l)
```bash
def genratePrime():
    flag=False
    count=0
    i=2
    while(count<n):
        flag=True
        for j in range(2,int(i**0.5)+1):
            if i%j==0:
                flag=False
                break
            else:
                flag=True
        if flag :
            print(i)
            count+=1
        i+=1
        
n=int(input("Enter the number of primes you want: "))
genratePrime()
```
### Code output-
![image](https://github.com/user-attachments/assets/c64ab863-1594-43e4-a500-63c79f0fd962)

# Question 3

```bash
def pyramid(n):
    for i in range(1, n + 1):
        print(" " * (n - i) + "*" * (2 * i - 1))

def reverse_pyramid(n):
    for i in range(n, 0, -1):
        print(" " * (n - i) + "*" * (2 * i - 1))

pyramid(5)
reverse_pyramid(5)
```
### Code output-
![image](https://github.com/user-attachments/assets/3622b841-9461-4b88-b6a5-0b0c59d3ac37)

# Question 8

```bash
def character_info():
    char=input("Enter a character:")
    if char.isalpha():
        print("Letter")
        if char.isupper():
            print("Uppercase")
        else:
            print("Lowercase")
    elif char.isdigit():
        print("Digit")
        number_names = ["ZERO", "ONE", "TWO", "THREE", "FOUR", "FIVE", "SIX", "SEVEN", "EIGHT", "NINE"]
        print(number_names[int(char)])
    else:
        print("Special Character")
character_info()
```
### Code output-
![image](https://github.com/user-attachments/assets/4e642dc0-c41a-464f-8e09-907ff8263af9)

# Question 9

```bash
def str_ops(s, target, repl):
    # Part (a): Find the frequency of a character in a string
    freq = 0
    for c in s:
        if c == target:
            freq += 1

    # Part (b): Replace a character by another character in a string
    replaced = ""
    for c in s:
        if c == target:
            replaced += repl
        else:
            replaced += c

    # Part (c): Remove the first occurrence of a character from a string
    removed_first = ""
    found = False
    for c in s:
        if c == target and not found:
            found = True
            continue
        removed_first += c

    # Part (d): Remove all occurrences of a character from a string
    removed_all = ""
    for c in s:
        if c != target:
            removed_all += c

    return freq, replaced, removed_first, removed_all

str_ops("hello python","o","a")
```
### Code output-
![image](https://github.com/user-attachments/assets/bfe84da2-cbc5-42c4-a884-a320ee59a588)

# Question 10

```bash
def swap_first_n(str1, str2, n):
    if n > len(str1) or n > len(str2):
        return "n is too large"
    new_str1 = str2[:n] + str1[n:]
    new_str2 = str1[:n] + str2[n:]
    return new_str1, new_str2

result = swap_first_n("hello", "world", 2)
print(result) 
```
### Code output-
![image](https://github.com/user-attachments/assets/c9a144f7-03bb-4691-b6a0-900702e001c3)

# Question 11

```bash
def find_substring_indices(main_str, sub_str):
    indices = []
    i = main_str.find(sub_str)
    while i != -1:
        indices.append(i)
        i = main_str.find(sub_str, i + 1)
    if indices:
      print(indices)
    else:
      print("-1")

find_substring_indices("hello hello", "lo")
find_substring_indices("hello world", "xyz")
```
### Code output-
![image](https://github.com/user-attachments/assets/4913ee3c-3acc-4a39-9be2-c26299d647ed)

# Question 12

```bash
def cubes_of_even_numbers_loop(lst):
    result = []
    for x in lst:
        if x % 2 == 0:
            result.append(x**3)
    print(result)

cubes_of_even_numbers_loop([1, 2, 3, 4, 5, 6])

# WAP to create a list of cubes of only even integers from an input list using list comprehension

def cubes_of_even_numbers_comprehension(lst):
    print([x**3 for x in lst if isinstance(x, int) and x % 2 == 0])

cubes_of_even_numbers_comprehension([1, 2, 3, 4, 5, 6])
```
### Code output-
![image](https://github.com/user-attachments/assets/a0fcb947-6923-4849-9bec-d9d23b6a0ae0)

# Question 13

### m)
```bash
filename=input("Enter filename:")
file=open(filename, 'r') 
lines = file.readlines()
num_lines = len(lines)
num_words = sum(len(line.split()) for line in lines)
num_chars = sum(len(line) for line in lines)
print(num_chars, num_words, num_lines)
```

### n)
```bash
def character_frequency_in_file(filename):
    freq = {}
    with open(filename, 'r') as file:
        text = file.read()
        for char in text:
            freq[char] = freq.get(char, 0) + 1
    print(freq)

character_frequency_in_file("sample.txt")
```

### o)
```bash
def reverse_words_in_file(filename):
    with open(filename, 'r') as file:
        words = file.read().split()
    print(' '.join(reversed(words)))

reverse_words_in_file("sample.txt")
```
