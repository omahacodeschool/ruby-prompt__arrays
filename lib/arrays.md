---
title: Arrays
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is an Array?

An array is a data object that stores an ordered list of values.

# What are some examples of information that would be Arrays as opposed to some other data type?

An array can be made up all data types and is used to organize large amounts of data.

# What is one way, using Ruby, to retrieve the 6th element in an Array? How about the 8th element? What happens if you try to retrieve the value of the _9999th_ element (or some element that doesn't exist in the array)?

Array[5] and Array[7].  Array[n] retrieves the nth element in the area, with the first element being stored at Array[0].  Trying to retrieve a nonexistant element returns 'nil'.

# The previous question asks about finding, for example, the 6th element in an Array. Is it possible to find the **-6th** (Notice the negative symbol!) element in an Array? What does that even mean?

Array[-6] retrieves the the 6th element from the end of the array.

# How would you perform an operation on every element inside an Array?

You could use for or while loops or the each method.

# How do you add elements to an Array?

Using the push method or '<<' will add an element to the end of the array, and assigning a value to a new index in an array will create a new element at that index.

# Given the Array `["Laura", "Fiona", "Tori"]`, how would you replace `"Fiona"` with `"Florence"` so that you end up with `["Laura", "Florence", "Tori"]`?

Array[1] = "Florence"

# What do the methods `push`, `pop`, `shift`, and `unshift` do?

push adds an element to the end of the array, pop removes the last element of the array, shift removes the first element of the array and shifts all elements down by one, and unshift shifts all elements up by one and adds an element to the beginning of the array.

# How do you determine how many elements are in an Array?

Array.length

# How would you reverse the order of elements in an Array?

Array.reverse

# How would you convert a String `"Sumeet Jain"` into an Array `["Sumeet", "Jain"]`? How about to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`? How would you convert the Array back into a String?

"Sumeet Jain".split(" ") and "Sumeet Jain".split("") convert them to arrays.  ["Sumeet", "Jain"].join(" ") and ["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"].join convert them back to strings.