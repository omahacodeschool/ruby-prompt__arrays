---
title: Arrays
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is an Array?

An array is a collection of ordered objects.  They are indexed to an integer, and are thus stuck in place (unless the array is edited).  So, the first object in the array is indexed to 0, the second object is indexed to 1, and so on.  The end of the array can be counted backwards from -1.  Arrays can be multidimensional (having any number of n-tuples) assigned to the integers.  Like [4,23,27] could be a single object in the array (properly formatted, of course).

# What are some examples of information that would be Arrays as opposed to some other data type?

As stated above, multidimensional objects are suited for arrays.  Another type of collection that would do well in arrays would be lists that the user needs to have in a specific order (for instance, the list of persons in the order that they arrived so that they might be able to give a door prize to the first persons that had arrived).  

# What is one way, using Ruby, to retrieve the 6th element in an Array? How about the 8th element? What happens if you try to retrieve the value of the _9999th_ element (or some element that doesn't exist in the array)?

Let's say that we have an array with the name alphabet, with the following collection of objects: alphabet = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm'].  To retrieve the sixth's element of that array, you use: alphabet[6], which will return g in this case.  If I tried to input alphabet[9999], I would get a nil return, or the default value.

# The previous question asks about finding, for example, the 6th element in an Array. Is it possible to find the **-6th** (Notice the negative symbol!) element in an Array? What does that even mean?

It is possible to find the -6th element in the array.  Arrays can identify the element by counting backwards.  The negative means that the count will start from the end of the array.  In the case of alphabet, it will return h as value. 

# How would you perform an operation on every element inside an Array?

A way to perform an operation on every element inside an array would be to use the map! function. Map! allows for the new edited versions of the elements to replace the elements in their place.  So, if we were to write alphabet.map! { |x| x + "!" } it would return #=> ['a!', 'b!', 'c!', 'd!', 'e!', 'f!', 'g!', 'h!', 'i!', 'j!', 'k!', 'l!', 'm!'].
Of course, there are times where we would not want to permanently alter an array, but rather return a new, edited array (this answer is edited due to comments).  The map function would return a new array, whereas map! edits the existing one.  There would be times it would be useful to keep the original array around, and there would be times where we would want to have several edited versions of the original array, requiring map over map!.

# How do you add elements to an Array?

Apparently there are several methods/operations for adding elements to arrays.  If we would like to add an element to the end of the array, we can use push or <<.  If we wanted to add 'n' to the end of alphabet, we could write alphabet.push('n'). There is an unshift command, alphabet.unshift('n') that would add that element 'n' to the beginning of the array.
A two-place operative insert can insert the element at any place in the array.  Writing alphabet.insert(4, "n") will insert it into the fourth spot in that array.

# Given the Array `["Laura", "Fiona", "Tori"]`, how would you replace `"Fiona"` with `"Florence"` so that you end up with `["Laura", "Florence", "Tori"]`?

I can think of one way to do it, that would involve two commands, the delete_at and insert commands.  I'm going to call this array names. You could write 
names.delete_at(1)
names.insert(1, "Florence")
puts names.print

This should print out ["Laura," "Florence", "Tori"]

# What do the methods `push`, `pop`, `shift`, and `unshift` do?

The method push adds an item to the end of the array.  Pop is a method used to remove an element from an array.  It can be used by itself to remove the last element from the array, or a particular element or elements can be specified with its associated integer and removed.  
The shift method removes the first element from the array.  It is similar to pop, in that it removes elements, but if a number is specified, say (3), it will remove the first three elements from the array, or return the default (nil if not specified) if there is nothing in the array for what has been identified to be removed with shift.  The unshift method does the opposite of shift, and adds elements to the front of the array.  It does not delete elements that were in the front, but moves them down in the array to later/higher associated integers.

# How do you determine how many elements are in an Array?

The count method returns how many elements there are in the array.

# How would you reverse the order of elements in an Array?

Fittingly, the reverse method would return the elements in reverse order.   It would look like [ "j", "k", "l" ].reverse   #=> ["l", "k", "j"]

# How would you convert a String `"Sumeet Jain"` into an Array `["Sumeet", "Jain"]`? How about to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`? How would you convert the Array back into a String?

To convert a string to an array, the split method is used.  I read that the default for split uses a space character to separate strings into elements for arrays.  I hope that is the case!  To convert "Sumeet Jain"` into an Array `["Sumeet", "Jain"]` I would assign the string "Sumeet Jain" a name, sumeet = "Sumeet Jain", and the method would look like sumeet.split .
To convert "Sumeet Jain" into ["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"], I would specify a space, so it would be sumeet.split "" .
To convert the array back to a string, I would use the join method.  I would assign a name for the array jain = ["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"].
I would write sumeet_jain = jain.join 
puts sumeet_jain
If I need to convern the array sumeet_jain = ["Sumeet", "Jain"] I would have to use sumeet_jain.join(" ") to add a space between the different elements in the array.



