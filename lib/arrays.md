---
title: Arrays
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is an Array?

An array is an ordered collection of objects. Each object in an array is given an integer index value, beginning with 0. Arrays are similar to strings but can contain many more types of objects, such as numbers, strings, and other arrays.

# What are some examples of information that would be Arrays as opposed to some other data type?

A list of non-consecutive numbers would contained in an array, as would a combination of fixnums and floats. A list of strings would also be an array. 

# What is one way, using Ruby, to retrieve the 6th element in an Array? How about the 8th element? What happens if you try to retrieve the value of the _9999th_ element (or some element that doesn't exist in the array)?

Each element in an array is assigned an index number, starting with 0, and an element can be retrieved by using that index. For example, if an_array = ["blue", "red", "yellow", "green", "purple", "orange", "black", "white"], then print an_array[5] will return "orange". The same would be true for the 8th element, print an_array[7] would return "white". Because there is no 50th element, calling print an_array[50] will return nil.

# The previous question asks about finding, for example, the 6th element in an Array. Is it possible to find the **-6th** (Notice the negative symbol!) element in an Array? What does that even mean?

It is possible to find a negative index in an array. If a negative index is accessed, the indexing order is reversed and the last value is assigned 0 rather than the first. So calling print an_array[-5] would return "yellow".

# How would you perform an operation on every element inside an Array?

An iterator such as the .each method would be used to perform an operation on every element in an array. For example, the code an_array.each do |x| x.capitalize end would capitalize each element in an_array.

# How do you add elements to an Array?

There are multiple ways to add elements to an array. Elements of one array can be added to the end of another array by using '+'. Calling the .push method will also add elements to the end of an array. Using '<<' has the same result as using the .push method. 

# Given the Array `["Laura", "Fiona", "Tori"]`, how would you replace `"Fiona"` with `"Florence"` so that you end up with `["Laura", "Florence", "Tori"]`?

A value in an array can be changed in a way that is similar to looking up the value using its index. In the above array, array[1] would return "Fiona", and array[1] = "Florence" would reassign the value of "Florence" to the index 1. I actually discovered this while playing with replacing elements in hashes. The way I had initially found to replace an element in an array was to iterate through the array with the .each method, and call the .sub method on each element. For example, for the above array, I would write array.each do |x| x.sub("Fiona", "Florence") end. 

# What do the methods `push`, `pop`, `shift`, and `unshift` do?

The push method adds an element to the end of an array, while the pop method removes the last element in an array. The unshift method adds an element to the beginning of an array and shifts all other elements up one index number. The shift method removes the first element of an array and shifts all other elements down one index number.

# How do you determine how many elements are in an Array?

The .length method will return the number of elements in an array. Running an_array.length will return 8.

# How would you reverse the order of elements in an Array?

The .reverse method will reverse the order of the elements in an array.

# How would you convert a String `"Sumeet Jain"` into an Array `["Sumeet", "Jain"]`? How about to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`? How would you convert the Array back into a String?

Calling the .split method on a string will convert it into an array, splitting the characters in the string into array elements based on a specified delineator. The code "Sumeet Jain".split(" ") will return ["Sumeet", "Jain"], using the space character as the delineator. "Sumeet Jain".split("") has no delineator and will return ["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]. The .join method converts the array back into a string by joining the elements of the array into a single string. The .join method can accept an argument which specifies a character to insert between the array's elements in the outputted string. ["Sumeet", "Jain"].join would return "SumeetJain", while ["Sumeet", "Jain"].join(" ") would return "Sumeet Jain".