---
title: Arrays
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is an Array?

An array is composed of values stored in cells. It is defined by brackets in Ruby.

# What are some examples of information that would be Arrays as opposed to some other data type?

An array and a string can form the same block of text, but because an array can
store words of the text into its cells. Strings are composed of single values.

# What is one way, using Ruby, to retrieve the 6th element in an Array? How about the 8th element? What happens if you try to retrieve the value of the _9999th_ element (or some element that doesn't exist in the array)?

If an array has n elements then to call the nth element the command array_name[n].
When a n+1 element is asked then a nil response will be given.

# The previous question asks about finding, for example, the 6th element in an Array. Is it possible to find the **-6th** (Notice the negative symbol!) element in an Array? What does that even mean?

Just like with strings, asking for a negative value for a element will start the
call from the end of the list of elements.

# How would you perform an operation on every element inside an Array?

array_name*2 will multiply each element by 2. 

# How do you add elements to an Array?

Push is what is said to be a function to put a new element into an existing array.
There is also the strategy of just saying array_name[n+1]=newvalue.

# Given the Array `["Laura", "Fiona", "Tori"]`, how would you replace `"Fiona"` with `"Florence"` so that you end up with `["Laura", "Florence", "Tori"]`?

The array element Fiona can be replaced will Florence by using array[1]=Florence.

# What do the methods `push`, `pop`, `shift`, and `unshift` do?

Push and pop will add or remove an element to or from an array at the end
respectivley. Shift and Unshift work the same way except they do the changes at 
the beginning.

# How do you determine how many elements are in an Array?

Length count or size all are capable of getting the number of elements in an array.

# How would you reverse the order of elements in an Array?

The method .reverse in Ruby can change the order from back to front.

# How would you convert a String `"Sumeet Jain"` into an Array `["Sumeet", "Jain"]`? How about to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`? How would you convert the Array back into a String?

The .split command can be used to turn a string into an array. The .split can be
followed by (//) to produce each character as its own element in an array from a 
string. The command .join is used to convert arrays into strings.