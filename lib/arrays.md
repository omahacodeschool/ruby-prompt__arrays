---
title: Arrays
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is an Array?

An Array is a data object that stores an ordered list of values.

# What are some examples of information that would be Arrays as opposed to some other data type?

a collection of elements, each selected by one ore more identifying keys. 

# What is one way, using Ruby, to retrieve the 6th element in an Array? How about the 8th element? What happens if you try to retrieve the value of the _9999th_ element (or some element that doesn't exist in the array)?

puts arr[5] would get you the 6th element. Since arrays are zero-based indexed.

puts arr[7] would get you the 8th element.

puts arr[9999] in an array with less elements than stated would return nil.

# The previous question asks about finding, for example, the 6th element in an Array. Is it possible to find the **-6th** (Notice the negative symbol!) element in an Array? What does that even mean?

Yes it is possible, with the last element in the array being -1.

# How would you perform an operation on every element inside an Array?

By using the .each method.

# How do you add elements to an Array?

By using the .push fucntion. 

# Given the Array `["Laura", "Fiona", "Tori"]`, how would you replace `"Fiona"` with `"Florence"` so that you end up with `["Laura", "Florence", "Tori"]`?

I would just set arr[1] = "Florence"

# What do the methods `push`, `pop`, `shift`, and `unshift` do?

Push modifies the array by adding an element to the end of the array.

Pop is used to remove the last element from the array.

Shift removes the first element from the array and moves the other elements down one position.

Unshift adds an element to the array at position 0 and moves all other elements up one position. 

# How do you determine how many elements are in an Array?

By using the .count function. 

# How would you reverse the order of elements in an Array?

By using the .reverse function.

# How would you convert a String `"Sumeet Jain"` into an Array `["Sumeet", "Jain"]`? How about to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`? How would you convert the Array back into a String?

By using .split(' ') to convert the String `["Sumeet", "Jain"]`,

By using .split('') to convert the String to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`,

By using .join(' ') to convert the fisrt Array back into a String,

And by using .join to convert the second Array back into a String.