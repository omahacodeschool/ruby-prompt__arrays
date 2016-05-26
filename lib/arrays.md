---
title: Arrays
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is an Array?

An array is an ordered collection of objects.

# What are some examples of information that would be Arrays as opposed to some other data type?

An array could be used to store any sort of list where you need to access the items individually.  For example, the list of items in a grocery list app that would need to be added separately and removed as they're purchased.

# What is one way, using Ruby, to retrieve the 6th element in an Array? How about the 8th element? What happens if you try to retrieve the value of the _9999th_ element (or some element that doesn't exist in the array)?

Because, like strings, they index from 0, array[5] would return the 6th element, and array[9] the 8th.  Again, as with strings, any element that doesn't exist will return nil.

# The previous question asks about finding, for example, the 6th element in an Array. Is it possible to find the **-6th** (Notice the negative symbol!) element in an Array? What does that even mean?

Yes; it counts from the end instead of the beginning.

# How would you perform an operation on every element inside an Array?

The each method allows easily iterating on every element in the array.

# How do you add elements to an Array?

You can assign elements directly using an index, like array[5] = "a new 6th item".  If you don't care what index it gets, you can more easily add an item using the push method, which inserts the element as the last item in the array.

# Given the Array `["Laura", "Fiona", "Tori"]`, how would you replace `"Fiona"` with `"Florence"` so that you end up with `["Laura", "Florence", "Tori"]`?

["Laura", "Fiona", "Tori"][1] = "Florence" 

This works if you know specifically that Fiona is the second element.  If you didn't already know that, you'd need to use the index method first.

# What do the methods `push`, `pop`, `shift`, and `unshift` do?

Push adds an element to the end.  Pop removes an element from the end and removes it.  Shift and unshift work on the beginning; shift pulls the first element off, and unshift inserts an element at the beginning.

# How do you determine how many elements are in an Array?

You can get the length of the array using the length method.

# How would you reverse the order of elements in an Array?

Similarly, you can reverse the elements using the reverse method.

# How would you convert a String `"Sumeet Jain"` into an Array `["Sumeet", "Jain"]`? How about to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`? How would you convert the Array back into a String?

Using the split method and specifying to split on spaces would return an array of words in the string.  Using the chars method will return the individual characters in an array.  Using the join method on either array with either a string of " " for the first result or nothing for the second will convert the array into a single string.