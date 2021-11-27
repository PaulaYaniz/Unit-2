# QUIZ 005
## Given an integer N, show the multiplication table. 
Example:

tableM(N=2)  →  2x1=2 ; 2x2=4 ; 2x3=6 ; 2x9=18
````
n = int(input())

for m in range(1,11):
  print(n,"x", m, "=", n*m)
````
# QUIZ 006
## Output TRUE if the given string begins with 'mix', except the 'm' can be anything, so 'pix', '9ix'..., all count.
Examples

MixStart('mix snacks') → TRUE       MixStart('pix snacks') → TRUE       MixStart('piz snacks') → FALSE
````
MixStart = input()
if MixStart.startswith('ix', 1):
  print(True)
else:
  print(False)
 ````
# QUIZ 007
## Given a string, create a function that outputs each letter with its index:
Example:

letters('hello') →  [‘0 -> h’,
						    ‘1 -> e’,
						    ‘2 -> l’,
						    ‘3 -> l’,
						    ‘4 -> o’]
````
def letters(a):
  ilast = len(a)-1
  i = 0
  list = []
  while i <= ilast:
    letter = a[i]
    list.append(letter)
    i += 1
  return list

a = input()
listletters = letters(a)
#print(listletters)

i = 0
for letter in listletters:
  print(i, " -> ", letter)
  i += 1
````
# QUIZ 008
## Create a function. Inputs is an list of integers, find the largest absolute value.  Tip: you can use the abs() function.
Example:

maxAbs([-4, 5, 6, -7]) → “max absolute is 7” 
maxAbs([-1, 0, 1]) → “max absolute is 1”
maxAbs([-100, 0, 3,-200]) → “max absolute is 200” 
````
def maxAbs(l):
  l2 = []
  for n in l:
    l2.append(abs(n))
  return(max(l2))

m = maxAbs([-3, 5, -8])
print("max absolute is", m)
````
# QUIZ 009
## Given an array of sorted integers, find the missing number.
Example:

missingNumber([1, 2, 3, 5, 6, 7]) → 4 
missingNumber([4, 5, 6, 8, 9, 10]) → 7
missingNumber([73, 74, 75, 76, 78, 79]) → 77 
````
def missingNumber(l):
  for i in range(len(l) -1):
    # print(l[i], l[i+1])
    if l[i] + 1 != l[i+1]:
      return l[i]+1

print("Missing number:", missingNumber([1, 2, 3, 5, 6, 7]))
````
# QUIZ 010
## Given an array of sorted integers, find the largest difference between neighbouring numbers.
Example:

BigNeighbour([1, 2, 3, 5, 6, 7]) → 2 (because 3 to 5) 
BigNeighbour([0, 5, 6, 10]) → 5 (because 0 to 5)
BigNeighbour([73, 74, 174, 76, 78, 79]) → 100 
````
def BigNeighbour(l):  
  l2 = []
  for i in range(len(l) -1):
    l2.append((l[i+1] - l[i]))
  return max(l2)
  
print(BigNeighbour2([1, 2, 3, 5, 6, 7]))
#User will need to change the print for different numbers
````
# QUIZ 011
## Given an array of numbers, output TRUE if the array is length 1 or more, and the first element and the last element are equal. Otherwise output FALSE.
Example:

SameFirstLast([1, 2, 3]) → FALSE
SameFirstLast([1, 2, 3, 1]) → TRUE
SameFirstLast([1, 2, 1]) → TRUE
````
l = []
a = 1 
while(a != ""):
  a = input()
  if a != "":
    l.append(int(a))

print(l)
print(len(l) > 0 and l[0] == l[-1])
````
# QUIZ 012
## Given an list of words, find the average word length.
Example:

wordlength(["home","car","travel","beach"])→4.5
wordlength(["sun","sat","cut","can"]) → 3
wordlength("police", "abacus"]) → 6
````
s = str(input())
print(s)
l = s.split(",")
print(l)
sum = 0
for e in l:
  sum += len(e)
average = sum/len(l)
print(average)
````
