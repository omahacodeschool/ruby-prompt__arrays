---
title: Arrays
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is an Array?

An array is a collection of information stored as a list. 

# What are some examples of information that would be Arrays as opposed to some other data type?

Considering that arrays can be comprised of any data type, any information that tends to be listed or stored as a database would work well as an array, such as a table of contents of a book or names of students in a class. 

# What is one way, using Ruby, to retrieve the 6th element in an Array? How about the 8th element? What happens if you try to retrieve the value of the _9999th_ element (or some element that doesn't exist in the array)?

One way to retrieve an element of an Array would be to use the element's index. For example for the 6th element in an array it would be "array[5]". As well as for the 8th, it would be "array[7]. If you try to retrieve an element that doesn't exist in the array, ruby will return nothing. 

# The previous question asks about finding, for example, the 6th element in an Array. Is it possible to find the **-6th** (Notice the negative symbol!) element in an Array? What does that even mean?

It is possible to return the -6th element in an array. What this means is that ruby will begin counting from the end of the array. So in the example given, -6 would return the 6th element from the end of the array.

# How would you perform an operation on every element inside an Array?

In addition to using a loop that passes through it every element of an array, a more eloquent way to perform an operation on every element inside an array would be to use the "each" method. 

# How do you add elements to an Array?

There are multiple ways to add elements to an array. Unshift and Push are two array methods that can add elements to the beginning and end of the array respectively, whereas insert, can be used to specify at which position to add the new element.  

# Given the Array `["Laura", "Fiona", "Tori"]`, how would you replace `"Fiona"` with `"Florence"` so that you end up with `["Laura", "Florence", "Tori"]`?

In order to replace "Fiona" with "Florence" in this example, assuming these names are stored in array "names", simply using the "names[1] = "Florence"" command will work.

# What do the methods `push`, `pop`, `shift`, and `unshift` do?

As I mentioned in my previous answer, unshift and push are two methods to add elements to an array, doing so at the beginning with unshift and the end with push. Shift and Pop are their opposing methods which will remove an element from an array again from the beginning and the end respectively.

# How do you determine how many elements are in an Array?

The length method can be used to determind how many elements are in an Array.

# How would you reverse the order of elements in an Array?

The reverse method can be used to reverse the order of elements in an Array. For example "names.reverse" would output each of the names stored in array "names" in reverse order.

# How would you convert a String `"Sumeet Jain"` into an Array `["Sumeet", "Jain"]`? How about to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`? How would you convert the Array back into a String?

By using the "split" method, you can convert a string into an array. By defining a delimiter, the split method can be tweaked to separated the string at specific places. For the first example, ["Sumeet Jain"].split(" ") would produce the first output. For the second example, placing a "//" in the parentheses following "split" would produce the second output. As for converting the array back into a string you can use the to_s method or the join method.  
