---
title: Arrays
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is an Array?

An array is a list of values, with each slot, or element, holding a specific value.


# What are some examples of information that would be Arrays as opposed to some other data type?

Lists of information that would need to be independently referenced, and consist of differing datatypes, would be in arrays.


# What is one way, using Ruby, to retrieve the 6th element in an Array? How about the 8th element? What happens if you try to retrieve the value of the _9999th_ element (or some element that doesn't exist in the array)?

Code to retrieve 6th element of an array:
1) array1 = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j']
2) puts array1[5]
3) Returns "f"

Code to retrieve 8th element of an array:
1) array1 = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j']
2) puts array1[7]
3) Returns "h"

Code to retrieve 9,999th element of an array:
1) array1 = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j']
2) puts array1[9998]
3) Returns nil


# The previous question asks about finding, for example, the 6th element in an Array. Is it possible to find the **-6th** (Notice the negative symbol!) element in an Array? What does that even mean?

It is possible to find the -6th element of an array. When counting using a negative number, the program will count from the last element of the array backwards, with the last element having a position of -1 (instead of a 0 like when you count from the beginning of an array). Using the array from the previous question, the array would resolve like so:

Code to retrieve -6th element of an array:
1) array1 = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j']
2) puts array1[-6]
3) Returns "e"



# How would you perform an operation on every element inside an Array?

In the case of an array where all the elements are numbers, you can:
1) define the array, 
2) use the ".each" method to specify that you what follows the method is to be performed for each array element,
3) define a variable in verticle bars that will be used as a variable for each iteration of the method, and
4) type out the operation to be performed for each array element.

For my example, I want each array element to be multiplied by the number 2, and the results displayed:
array2 = [1, 2, 3, 4, 5, 6, 7, 8]
array2.each {|z| puts z * 2}


# How do you add elements to an Array?

You add elements to an array by "shoveling" them using the syntax below:
array2 = [1, 2, 3, 4, 5, 6, 7, 8]
array2 << 9
(Result) => [1, 2, 3, 4, 5, 6, 7, 8, 9]

You can also do so by using the ".push" method:
array2 = [1, 2, 3, 4, 5, 6, 7, 8]
array2.push 9
(Result) => [1, 2, 3, 4, 5, 6, 7, 8, 9]


# Given the Array `["Laura", "Fiona", "Tori"]`, how would you replace `"Fiona"` with `"Florence"` so that you end up with `["Laura", "Florence", "Tori"]`?

I would use the following code to replace "Fiona" with "Florence":
na1 = ["Laura", "Fiona", "Tori"]
na1.delete_at(1)
na1.insert(1, "Florence")
(Result) => ["Laura", "Florence", "Tori"]

# What do the methods `push`, `pop`, `shift`, and `unshift` do?

1) The ".push" method adds an element of a specified value to the end of the array.
2) The ".pop" method removes the last element of an array and return its value.
3) The ".shift" method will remove the remove the first element of an array and return its value.
4) The ".unshift" method will add a new value to the beginning of an array.



# How do you determine how many elements are in an Array?

You can use the "size" or "length" methods to determine the number of elements in an array:
na2 = [1, 'a', 2, 'b', 3, 'c']
na2.size
(Result) => 6


# How would you reverse the order of elements in an Array?

You can reverse the order of an array by using the reverse method:
na3 = [1, 2, 3, 4, 5, 6, 7]
na3.reverse
(Result) => [7, 6, 5, 4, 3, 2, 1]


# How would you convert a String `"Sumeet Jain"` into an Array `["Sumeet", "Jain"]`? How about to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`? How would you convert the Array back into a String?

Convert a string "Sumeet Jain" into an array:
"Sumeet Jain".split(" ")
(Result) => ["Sumeet", "Jain"]

Convert "Sumeet Jain" into an array where each character is its own element (including the space):
"Sumeet Jain".split("")
(Result) => ["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]

Use the ".join" method to concatenate all array elements:
na1 = "Sumeet Jain"     => "Sumeet Jain"
na2 = na1.split("")     => ["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]
na2.join                => "Sumeet Jain"             
