# Data-Structure
1.What are data structures and why are they imporatnt?
Data structures is way of organising and storing data, which can be used effeciently. Importance-

Efficiency - the right data structure makes program faster and saves memory

Resuability-They provide reusable building blocks for writing complex algorithms.

Scalability → Good data structures help systems handle large amounts of data smoothly.

2. Explain the difference between mutable and immutable data types with examples
Mutable data types - can be changed or modified after they have been created. Eg - Lists are mutable

Immutable data types - cannot be changed or modified.Eg- tuples are immutable


# example of mutable -
Groceries = ["Banana","Tea leaves", "Atta", "Rice"]
print("before :", Groceries)
Groceries[1] = "Sugar"
print("after :", Groceries)

     
before : ['Banana', 'Tea leaves', 'Atta', 'Rice']
after : ['Banana', 'Sugar', 'Atta', 'Rice']

# example of immutable-
name = "Priya"
print("before :", name)
name = name + "nka"
print("after :", name)
     
before : Priya
after : Priyanka
3.What are the main differences between lists and tuples in Python?
Lists - are mutable and are denoted by square brackets []. They have more memory, and functions like, append, extent can be used.

Tuples- are immutable and denoted by () brackets. They have less memory, and functions like, count, index can be used.

4.Describe how dictionaries store data ?
A dictionary is an in-built function that store data in key-value pairs. Keys act like lables and values are the actual data.


Student_id = {
    "name " : "Priyanka Saha ",
    "age" : 26 ,
    "subject" : "data analysis"
}

print(Student_id)
     
{'name ': 'Priyanka Saha ', 'age': 26, 'subject': 'data analysis'}
5.Why might you use a set instead of a list in Python ?
List - List allows duplicates, maintains insertion order. It is slower and used when orders and duplicates matter.

Sets - sets don not allow duplicates, it is unorderd and faster.Used when uniqueness matters.

6. What is a string in Python, and how is it different from a list?
String - is a sequence of characters enclosed in single quotes ' ' , or double quotes " ".

Strings are immutable, while lists are mutable
Lists can store string itself.
while strings are stored within quotes, lists are stored within []
7. How do tuples ensure data integrity in Python ?
Data integrity- means, keeping data safe, consistent and unchanged. And tuples are immutabe (cannot be changed), hence they ensure data integrity.

8. What is a hash table, and how does it relate to dictionaries in Python?
Hash table - is a data structure that stores data in key-value pairs, and allows fast access.

It uses a hash function to convert each key into a number called hash value
the hash values decides the slot, where the value will be stored in memory.
student = {"name": "Priyanka", "age": 26, "course": "Python"}
print(student["age"])

Age is converted to a hash value
python jumps to that memroy slot and retrives 26
9. Can lists contain different data types in Python?
Yes. In python, lists can contain different data types within the same list.


# Example -
my_list = [26, "Priyanka", True, 3 + 5j]
print(my_list)
     
[26, 'Priyanka', True, (3+5j)]
10.Explain why strings are immutable in Python?
Immutable means , once a string is created it cannot be changed. Any kind of modification creates a new string Python internally resues string. If strings were mutable, changing one can unintentionally affect other variables


a = "Hello Priyanka"
a = a + "Saha"
print(a)
# "Hello Priyanka", is untouched, python created "Hello Priyanka Saha" as new object
     
Hello PriyankaSaha
11. What advantages do dictionaries offer over lists for certain tasks?
Dictionary uses hash value, that can be searched very fast using key. Whereas list requires scanning element by element.

List search (slow) students = ["Priya", "Arjun", "Meena"] print("Meena" in students) # O(n)

Dictionary search (fast) student = {"name": "Priya", "age": 21} print("name" in student) # O(1)

12.Describe a scenario where using a tuple would be preferable over a list?
Tuples are preffered over list in scenarios where we use data that should be unchanged. For example- in storing geograqphical locations, marks of students, fixed records, as these data sets should remain unchnaged

Example 1: storing geographical coordinates (latitude, longitude).
location = (28.6139, 77.2090) # Delhi coordinates

student_grades = { ("Priya", "Math"): 95, ("Arjun", "Science"): 88 } print(student_grades[("Priya", "Math")]) # 95
13. How do sets handle duplicate values in Python?
Set is an unordered collection of unique elements. This means duplictates are automatically removed.

When we try to add a duplicate elemen, Python checks its hash value. If the hash value already exists, python ignores the duplicate and each value appears only once


# Example
a = {1,2,3,3,4,4,4,5}
print(a)
     
{1, 2, 3, 4, 5}
14.How does the “in” keyword work differently for lists and dictionaries?
"in" with lists- checks if the value exists in the list. It finds the match. Example - fruits = ["apple", "banana", "cherry"]

print("banana" in fruits) # True print("orange" in fruits) # False

"in" with dictionaries - checks if key exists in dictionary (not the value) Exampe- student = {"name": "Priya", "age": 21, "course": "Python"}

print("name" in student) # True (checks keys) print("Priya" in student) # False (values not checked)

15.Can you modify the elements of a tuple? Explain why or why not?
No, tuples are immutable in python. Their contents cannot be changed or modified Reason- protects fixed collections of data (eg- coordinates, dates) can be used as dictionary keys or set elemnts

16. What is a nested dictionary, and give an example of its use case?
A nested dictionary is a dictionary an other dictionary. It is used to represent hierarchial/ structured data. The outer dictionaries stores keys that map to inner dictionaries. Example -


# Student data record
students = {
    "101": {"name": "Priya", "age": 21, "course": "Python"},
    "102": {"name": "Arjun", "age": 22, "course": "Java"},
    "103": {"name": "Meena", "age": 20, "course": "Data Science"}
}

print(students["101"]["name"])   # Priya
print(students["103"]["course"]) # Data Science
     
Priya
Data Science
17.Describe the time complexity of accessing elements in a dictionary?
Dictionaries in python are built on hash values.Python computes the hash of the key. It uses the hash to jump directly to the slot memory.

Time Complexity Average Case(O(1))- Lookups are constant time beacuse hashing lets python jump straight to the value
Word Case(O(n))- rare, happens only if many keys collide(all hash to same slot).

18.In what situations are lists preferred over dictionaries ?
Situations where -

We need ordered data as list maintains order
Duplicates are required, as dictionary does not store duplicates
Only values matter, keys are unnecessary
Memory efficiency is imporant Example - fruits = ["apple", "banana", "cherry"] print(fruits[0]) # apple
marks = [90, 85, 90, 75] # duplicates allowed

19.Why are dictionaries considered unordered, and how does that affect data retrieval?
Dictionaries are considered unordered collections because they use a hash table. Keys are placed in memeory based on the hash value, not in the order that we add them. Example- a = {"a": 1, "b": 2, "c": 3} print(d) # Order could vary depending on Python version

20.Explain the difference between a list and a dictionary in terms of data retrieval.
Lists are ordered collections accessed by index.To find an element by value, python has to element by element. Access by index : o(1) Search by value : 0(n) Example - fruits = ["apple", "banana", "cherry"]

Access by index → fast print(fruits[1]) # banana

Search by value → slower print("cherry" in fruits) # O(n), True

Dictionaries-store data as key-value pairs. Retrieval is done using keys via hash table Example-

student = {"name": "Priya", "age": 26, "course": "Python"}

Access by key → very fast print(student["age"]) # 21

Search by value → slower print(21 in student.values()) # O(n), True
[DATA_Structure.ipynb (1).txt](https://github.com/user-attachments/files/22518464/DATA_Structure.ipynb.1.txt
