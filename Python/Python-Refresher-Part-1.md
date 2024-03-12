## Python Refresher Part 1
- Date : 2024-03-12
- Tags : #python #python-refresher
  
Began learning the fundamentals of Python
- Strings
- Integers
- Floats
- Variables
- String Assignment
- String Formatting
- Getting User Input
```py
first_name = input("Enter your first name: ") # assigns input to first_name
print(first_name)

days = int(input("How many days until your birthday? "))

print(f"Hi {first_name}, only {days} days until your birthday!")

weeks = (round(days/7, 2)) # rounds to 2 decimal places

print(f"Hi {first_name}, only {weeks} weeks until your birthday!")

sentence = "Hi {}, only {} weeks until your birthday!"

print(sentence.format(first_name, weeks))
```
- Lists
```py
my_list = [80, 96, 72, 100, 8]
print(my_list)
print(my_list[1]) # just like in JavaScript, the index prints the element in that index position

print(my_list[-1]) # the -1 index is the first element from the end

my_list[0] = 25 # just like in JS, this reassigns index 0
print(my_list)

print(len(my_list)) # this is Python way of finding length of array

print(my_list[0:2]) # Python way of slicing (prints 0, 1, up to but not including 2)

# INSERT AND DELETE

my_list.append(1000) # inserts 1000 at the end of array
print(my_list)

my_list.insert(2, 1000) # inserts at a specific index
print(my_list)

my_list.remove(8) # deletes the value from the array
print(my_list)

my_list.pop(0) # removes the value at index 0
print(my_list)

my_list.sort() # sorts numerically smallest to highest
print(my_list)
```
