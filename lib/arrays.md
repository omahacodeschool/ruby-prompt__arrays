---
title: Arrays
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is an Array?

A data type that stores objects as an ordered list.  In other languages they are simply referred to as lists.  
In ruby they are enclosed in square brackets [ ].

# What are some examples of information that would be Arrays as opposed to some other data type?

I would use an array for anything that can be written in list form.  
Hashes are better when data can be paired.  
Strings are used if you have a block of text.

# What is one way, using Ruby, to retrieve the 6th element in an Array? How about the 8th element? What happens if you try to retrieve the value of the _9999th_ element (or some element that doesn't exist in the array)?

Elements are stored in a zero based index so the first element is [0] and the second element in [1] and so on.
Here is an example:

array = ["ant", "bat", "cat", "dog", "elk", "fox", "gnu", "hen"]
puts array[5] => fox
puts array[7] => hen
puts array[9999] =>

nothing is returned when you try to retrieve a value that does not exist in the array.

# The previous question asks about finding, for example, the 6th element in an Array. Is it possible to find the **-6th** (Notice the negative symbol!) element in an Array? What does that even mean?

Yes it is possible.  It counts from the end of the array.
It would return the sixth element from the end.
In my previous example:

array = ["ant", "bat", "cat", "dog", "elk", "fox", "gnu", "hen"]
puts array[-6] => cat


# How would you perform an operation on every element inside an Array?

You can use a loop iteration or the each operator.

# How do you add elements to an Array?

You can use the push method or the << method.  For example,

array = ["ant", "bat", "cat"]
array.push("dog", "elk")
array << "fox"
puts array => ant, bat, cat, dog, elk, fox



# Given the Array `["Laura", "Fiona", "Tori"]`, how would you replace `"Fiona"` with `"Florence"` so that you end up with `["Laura", "Florence", "Tori"]`?

Given the length of the array, I would just assign [1] to Florence instead of Fiona

array = ["Laura", "Fiona", "Tori"]
array[1]="Florence"
puts array => Laura, Florence, Tori

# What do the methods `push`, `pop`, `shift`, and `unshift` do?

All four methods modify an array in place.
push - adds an element to the end of the array
pop - removes the last element of the array
shift - removes the first element of the array
unshift - adds an element to the beginning of the array



# How do you determine how many elements are in an Array?

Use the .length method

# How would you reverse the order of elements in an Array?

Use the .reverse method

# How would you convert a String `"Sumeet Jain"` into an Array `["Sumeet", "Jain"]`? How about to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`? How would you convert the Array back into a String?

string = "Sumeet Jain"
string.split => ["Sumeet", "Jain"]

string = "Sumeet Jain"
string.chars => ["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]

array = ["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]
array.join => "Summet Jain"