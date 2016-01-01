---
title: Arrays
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is an Array?

An array is used to organize information into an ordered list. 
The list can be made up of strings, integers, floats, booleans, or any other data type. 

# What are some examples of information that would be Arrays as opposed to some other data type?

In Ruby, an array is denoted by square brackets [ ]. Inside the brackets you can create a list of elements separated by commas. 
The brackets define that it would an array.

# What is one way, using Ruby, to retrieve the 6th element in an Array? How about the 8th element? What happens if you try to retrieve the value of the _9999th_ element (or some element that doesn't exist in the array)?

Each element in an array can be accessed via an index. 
For example [ 1, 2, 3, 4, 5][0] would get us the '1' from the list because the values start at '0'.
if you try to retrieve the 9999th number it would come back as 'nil' or nonexistant.

# The previous question asks about finding, for example, the 6th element in an Array. Is it possible to find the **-6th** (Notice the negative symbol!) element in an Array? What does that even mean?

it is possible to retrieve the -6th element. If I did [ 1, 2, 3, 4, 5, 6, 7, 8, 9][-6] it would give me 4. 
It starts at the end of my index and counts backwards 6.

# How would you perform an operation on every element inside an Array?

you would use something similar to Array.[](...) [or] Array[...] [or] [...] depending on what it is you wanted to accomplish. Like Array.index or Array.length.

# How do you add elements to an Array?

Elements may be added using the 'push' function or '<<'. I.E. array = ['laura', 'fiona', 'tori']
array.push('jimmy')
gives us => ["laura", "fiona", "tori", "jimmy"]

# Given the Array `["Laura", "Fiona", "Tori"]`, how would you replace `"Fiona"` with `"Florence"` so that you end up with `["Laura", "Florence", "Tori"]`?

you would use the replacement code i.e. 
a = ['Laura', 'Fiona', 'Tori']
a.replace(['Laura', 'Florence', 'Tori'])

# What do the methods `push`, `pop`, `shift`, and `unshift` do?

'Push' pushes the given object onto the end of the array. 'Pop' removes the last element from array and returns it, or nil if array is empty.

# How do you determine how many elements are in an Array?

You would create your array (i.e. array = [ 1, 2, 3, 4, 5, 6, 7, 8, 9]) and then type array.length and it will tell you how many elements are inside.

# How would you reverse the order of elements in an Array?

You would write your array (i.e. array = [ 1, 2, 3, 4, 5, 6, 7, 8, 9]) and then simply type array.reverse and it will reverse the order they appear.


# How would you convert a String `"Sumeet Jain"` into an Array `["Sumeet", "Jain"]`? How about to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`? How would you convert the Array back into a String?

To convert it into an array you would type in something like name = 'Sumeet Jain' and then simply do name.split. 
To make it break up into the individual letters you would have to add to the split with ("") so it should look like name.split("")
To convert it back to an Array you would type in the name of your array and add ".join" so it would look like:
a = ['Sumeet', ' Jain']
a.join("")