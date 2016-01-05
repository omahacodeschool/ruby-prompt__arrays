---
title: Arrays
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is an Array?

An array in Ruby is essentially a list of objects (strings, numbers, etc.), signified by brackets ([ ]), that are indexed with integers. Each slot of an array can act like a variable and when counting through an array, we start with '0'. A negative index reverses the count with '-1' referring to the last slot of the array, '-2' the second to last, and so forth.

# What are some examples of information that would be Arrays as opposed to some other data type?

I suppose some examples of information found in an array could be chapters of a book, ingrediants of a recipe, or names in an address book.

# What is one way, using Ruby, to retrieve the 6th element in an Array? How about the 8th element? What happens if you try to retrieve the value of the _9999th_ element (or some element that doesn't exist in the array)?

Using Ruby, we can retrieve the 6th element of an array by calling the index number '5', since arrays start the count at '0'. For the 8th, we call the index number '7'. For example: names = [Chris, Bill, Jane, Megan, Joe, Vince, Sophie, Nicole]; puts names[7]; Nicole. If you attempt to retrieve an element outside the rance of the array, 'nil' will be returned.

# The previous question asks about finding, for example, the 6th element in an Array. Is it possible to find the **-6th** (Notice the negative symbol!) element in an Array? What does that even mean?

es, retrieving an element with a negative integer from an array starts the count at the end rather than the start of the array. If using my array 'names' from above, printing the -6th element would result in 'Jane' being printed to the console.

# How would you perform an operation on every element inside an Array?

You can use the method 'each' to perform an operationon every element. Again using my 'names' array: names.each do |name|; puts "Hi, I'm " + name + "!" end; "Hi, I'm Chris!", "Hi, I'm Bill!", etc.

# How do you add elements to an Array?

You can add elements to an array with the method 'push'. This method adds the element to the end of the array.

# Given the Array `["Laura", "Fiona", "Tori"]`, how would you replace `"Fiona"` with `"Florence"` so that you end up with `["Laura", "Florence", "Tori"]`?

To replace "Fiona" with "Florence", you can do this: Array[1] = "Florence".

# What do the methods `push`, `pop`, `shift`, and `unshift` do?

The method "push" adds an element to the end of an array, "pop" removes the last element from the array and tells you what it was, "shift" retrieves and removes the first element from an array, and "unshift" adds an element to the first slot of an array.     

# How do you determine how many elements are in an Array?

I've found multiple methods that determine the ammount of elements in an array, including ".length", ".count", and ".size".

# How would you reverse the order of elements in an Array?

You would need to use the method ".reverse" on the array.

# How would you convert a String `"Sumeet Jain"` into an Array `["Sumeet", "Jain"]`? How about to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`? How would you convert the Array back into a String?

To convert the string "Sumeet Jain" to an array, we could call the ".split" method on it. In order to make an array with each character split, we could call the ".split" method with the argument "(//)" on the string.