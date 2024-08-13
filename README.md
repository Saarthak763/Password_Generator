# Password_Generator
import random 

uppercase="ABCDEFGHIJKLMNOPQRSTUVWXYZ"
lowercase="abcdefghijklmnopqrstuvwxyz"
digits="1234567890"
symbols="!@#$%^&*()_+=-}{[]?/<>,."
upper,lower,nums,syms=True,True,True,True

x=""
if upper:
   x += uppercase
if lower:
   x += lowercase
if syms:
   x += symbols
if nums:
   x += digits

print("Welcome to the password generator!!")
print("---------------------------------------------------------")
length = int(input("Enter the length of the password: "))
amount= int(input("Enter the amount of passwords you need: "))

for i in range(amount):
  password = "".join(random.sample(x, length))
  print(password)
  print("-------------------------------------------------------")
