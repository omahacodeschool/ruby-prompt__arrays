---
title: Arrays
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is an Array?

An Array is a list or collection of data. I can be a variety of data types.

# What are some examples of information that would be Arrays as opposed to some other data type?

An Array is a good way to store lists or a collection of data. You could use an Array to create a contact list or a grocery list for example. Writing each item of a list over and over again using seperate strings would take a while to accomplish and keep organized. An Array is a much better solution.

# What is one way, using Ruby, to retrieve the 6th element in an Array? How about the 8th element? What happens if you try to retrieve the value of the _9999th_ element (or some element that doesn't exist in the array)?

To retrieve the sixth element in an Array you would call it by it's index within the Array. Array's use zero based indexing so the first element of an Array starts at [0] and goes up from there. So to find the 8th element in an Array you would use [7]. If you were to try to access an element that doesn't exist Ruby would return nil.

# The previous question asks about finding, for example, the 6th element in an Array. Is it possible to find the **-6th** (Notice the negative symbol!) element in an Array? What does that even mean?

You can access elements within the Array using negative numbers which starts counting at the end of the Array. The last number in the Array would start with [-1] index. So as long as there are enough elements in the Array you would be able to find the [-6] element in an Array.

# How would you perform an operation on every element inside an Array?

The .each method allows you to run a block of code on/with each element inside an Array.

# How do you add elements to an Array?

The .push method of the Array Class allows you to add an element to the end of an Array.

# Given the Array `["Laura", "Fiona", "Tori"]`, how would you replace `"Fiona"` with `"Florence"` so that you end up with `["Laura", "Florence", "Tori"]`?

To replace an element in an Array you would use the .replace method on the specific element you wish to switch out. You would first tell Ruby which element in the Array you are planning to replace, "Fiona"[1], and then use the .replace method on that element. _"Fiona"[1].replace("Florence")_

# What do the methods `push`, `pop`, `shift`, and `unshift` do?

The method .push allows you to add one or more elements to the end of an Array while the .unshift method lets you do the same to the beginning of an Array.
The .pop method removes the last element in an Array while the .shift method removes the first element of an Array.


# How do you determine how many elements are in an Array?

You can use the .length method to determine how many elements are in an Array.

# How would you reverse the order of elements in an Array?

The .reverse method for the Array Class reverses the order of elements within an Array.

# How would you convert a String `"Sumeet Jain"` into an Array `["Sumeet", "Jain"]`? How about to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`? How would you convert the Array back into a String?

To convert a String into an Array I would use the .split method. You can use the .scan method with a regex(/\w/) to create a string out of each letter without the space or use the .split("") method to include the space as a string. To convert the Array back into a String I would use the .join("") method.