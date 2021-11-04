# QUIZ 005
## Given an integer N, show the multiplication table. 
Example:

tableM(N=2)  →  2x1=2 ; 2x2=4 ; 2x3=6 ; 2x9=18
````
n = int(input())

for m in range(1,11):
  print(n,"x", m, "=", n*m)
````
