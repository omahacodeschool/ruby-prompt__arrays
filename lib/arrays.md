---
title: Arrays
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is an Array?

An array is a type of data that stores information as a list. They can contain strings or numbers as integers or float numbers.

# What are some examples of information that would be Arrays as opposed to some other data type?

Arrays are used when you want to store and sort information into defined categories, which makes them different from other data types.
Example: Names can be stored in arrays and be chosen when needed. Basically, anything you need list of would be an array.

# What is one way, using Ruby, to retrieve the 6th element in an Array? How about the 8th element? What happens if you try to retrieve the value of the _9999th_ element (or some element that doesn't exist in the array)?

Arrays start at 0 instead of 1. So, in order to retrieve the 6th element, you would use [5]. For the 8th element, you would use [7]. You need to subtract one in order to the element you are looking for.
If you try to retrieve an element that does not exist, it comes back as nil, or nothing.

# The previous question asks about finding, for example, the 6th element in an Array. Is it possible to find the **-6th** (Notice the negative symbol!) element in an Array? What does that even mean?

If you search for a negative element, such as -6, you will be given the 6th element from the end, not the beginning, as the negative inverses the search. The reason -6 is the 6th is because when using the inverse, it starts at -1, as there is no -0.
Therefore, -1 will always retrieve the last element.

# How would you perform an operation on every element inside an Array?

In order to perform an operation on every element inside an array, you can loop through using the each method, which refers to each element inside it.

# How do you add elements to an Array?

To add an element to an array, use the push method. It will automatically add the element to the end of the array instead of to a new one. It literally pushes an element into an array.

# Given the Array `["Laura", "Fiona", "Tori"]`, how would you replace `"Fiona"` with `"Florence"` so that you end up with `["Laura", "Florence", "Tori"]`?

In order to replace something in an array, search through the array for the element using a while loop.
The index is set at zero so that it starts at the first element. From there, have the original array. While the loop runs within the array, it searches for "Fioana" so that it can replace it with "Florence". Make sure it searches by an increment of one.

# What do the methods `push`, `pop`, `shift`, and `unshift` do?

Push: adds (or pushes) an element at the end of an array
Pop: removes (or pops out) the last element of an array
Shift: removes the first element of an array, causing the other elements to shift down in numerical position
Unshift: adds objects to the front of an array, caushing the other elements to shift up in numerical position

# How do you determine how many elements are in an Array?

To find how many elements are in an array, use the length method (.length).

# How would you reverse the order of elements in an Array?

To reverse the order of elements in an array, use the reverse method (.reverse).

# How would you convert a String `"Sumeet Jain"` into an Array `["Sumeet", "Jain"]`? How about to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`? How would you convert the Array back into a String?

String to array: use split method. Split the string at the space. "Sumeet Jain".split" " results in ["Sumeet", "Jain"]
Array to string: use the join (.join) method. It will join all elements of the array into a single string.