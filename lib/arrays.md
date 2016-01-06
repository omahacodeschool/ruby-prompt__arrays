---
title: Arrays
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is an Array?
An Array is a Ruby data type that stores an ordered list of values.  
An Array is a number-indexed list.  
Values in a Array can be any type of object, including other Arrays.


# What are some examples of information that would be Arrays as opposed to some other data type?
Some examples of information that would be Arrays are a collection of values or list of data.


# What is one way, using Ruby, to retrieve the 6th element in an Array? How about the 8th element? What happens if you try to retrieve the value of the _9999th_ element (or some element that doesn't exist in the array)?
We can retrieve the 6th element in an Array by using the #[5] method, the 8th element using the #[7] method.
If we try to retrieve the value of an element that doesn't exist in our Array we will get => nil as a result.


# The previous question asks about finding, for example, the 6th element in an Array. Is it possible to find the **-6th** (Notice the negative symbol!) element in an Array? What does that even mean?
Assuming the Array contains at least 6 elements, we can find the -6th element.  The -6th element would be the 6th to last.


# How would you perform an operation on every element inside an Array?
Here we can perform an operation on every element inside an Array by using the Enumeral method '.map'.
For example, array = [1,2,3,4,5,"Fiona"].map{ |element| element * 3} => [3, 6, 9, 12, 15, "FionaFionaFiona"]


# How do you add elements to an Array?
We can add elements to an Array using the shovel '<<' operator or '.push' method.


# Given the Array `["Laura", "Fiona", "Tori"]`, how would you replace `"Fiona"` with `"Florence"` so that you end up with `["Laura", "Florence", "Tori"]`?
Although probably not the best example, we can use the '.map { |item| block} method where ["Laura", "Fiona", "Tori"].map{ |item| item.gsub("Fiona","Florence")} => ["Laura", "Florence", "Tori"]
Here the '.map{ |item| block} invokes the given block item.gsub for the "Fiona" element and creates a new Array containing "Florence" instead of "Fiona".


# What do the methods `push`, `pop`, `shift`, and `unshift` do?
The '.push' method adds element(s) to the end of an Array.
The '.pop' method removes and returns the last element(s) of an Array.
The '.shift' method removes the first element(s) of an Array.
The '.unshift' method adds element(s) to the front of an Array


# How do you determine how many elements are in an Array?
We can determine the number of elements in an Array via the '.count' method or the '.length' method.


# How would you reverse the order of elements in an Array?
We can reverse the order of elements in an Array by using the '.reverse' operator.


# How would you convert a String `"Sumeet Jain"` into an Array `["Sumeet", "Jain"]`? How about to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`? How would you convert the Array back into a String?
To convert a String into an Array we can use the '.split' method, i.e. "Sumeet Jain".split => ["Sumeet", "Jain"]
To convert an Array to a String we can use the '.join' method without an argument.