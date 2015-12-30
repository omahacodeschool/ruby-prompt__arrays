---
title: Arrays
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is an Array?

The Array is a data object that stores an ordered list of values.

# What are some examples of information that would be Arrays as opposed to some other data type?

words, integers, floats, strings

# What is one way, using Ruby, to retrieve the 6th element in an Array? How about the 8th element? What happens if you try to retrieve the value of the _9999th_ element (or some element that doesn't exist in the array)?

arr = [1, 2, 3, 4, 5, 6, 7]
puts arr[6]

or

You can address different elements in an array using numbers and than call those numbers.

arr = []

arr[0] = "a"
arr[1] = "b"
arr[6] = "c"

puts array_assign[6] returns c

If you try to call an element that doesn't exsist its returns nil

# The previous question asks about finding, for example, the 6th element in an Array. Is it possible to find the **-6th** (Notice the negative symbol!) element in an Array? What does that even mean?

Yes. It means the - is calling to the last element of an array as -1 so it will return the 6th element from the end.

# How would you perform an operation on every element inside an Array?

By using the each and map methods.

["hi", "bye"].map { |s| s.reverse } returns ["ih", "eyb"]

# How do you add elements to an Array?

You can use the push or << method. 

arr = ["yes", "no"] 
arr.push("maybe") or arr << "maybe"

# Given the Array `["Laura", "Fiona", "Tori"]`, how would you replace `"Fiona"` with `"Florence"` so that you end up with `["Laura", "Florence", "Tori"]`?

arr = ["Laura", "Fiona", "Tori"]
arr[1].replace("Florence")
puts arr.join(", ")

# What do the methods `push`, `pop`, `shift`, and `unshift` do?

Push adds an element to an array
Pop removes and returns the last element of an array
Shift removes and returns the first element of an array. Shifting the remaining elements down.
Unshift will add a new element to the beginning of the array

# How do you determine how many elements are in an Array?
Using .length

arr = [1, 2, 3]
arr.length

# How would you reverse the order of elements in an Array?
Using .reverse

arr = [1, 2, 3]
arr.reverse

# How would you convert a String `"Sumeet Jain"` into an Array `["Sumeet", "Jain"]`? 

"Summet Jain".split

#How about to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`? How would you convert the Array back into a String?

["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"].join

