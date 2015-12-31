---
title: Arrays
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is an Array?

An array is an ordered list that stores data. We define what is in the array within brackets [ ] and can perform functions on the array as a whole instead of having to perform the function on each variable individually.

# What are some examples of information that would be Arrays as opposed to some other data type?

Arrays should be used for lists or intergers that belong together. Using an array for items that would frequently need different functions applied to them would probably not be the most effective storage method. For example, you could put the names of all the Enfield students in an array (since we will similar experiences applied to each of us).

# What is one way, using Ruby, to retrieve the 6th element in an Array? How about the 8th element? What happens if you try to retrieve the value of the _9999th_ element (or some element that doesn't exist in the array)?

If, for example, you named your array "arr," you could retrieve the 6th element by typing arr[5] or the 8th element by typing arr[7]. This will make you sound like a pirate that can't count, BUT in arrays, the first element is actually the "zeroeth" element, not the first, so I should stop using that word. If the position you ask for (arr[9999]) doesn't exist, it will return "nil" or just a blank line, because there is nothing in that position on the list.

# The previous question asks about finding, for example, the 6th element in an Array. Is it possible to find the **-6th** (Notice the negative symbol!) element in an Array? What does that even mean?

You CAN find negative placement. If asking for arr[5] results in the 6th from the BEGINNING of the list, arr[-6] is finding the sixth from the END.

# How would you perform an operation on every element inside an Array?

To perform an operation on every element in an array, you have to let the computer know to separate the elements again, and apply the opperation to every part. This can be done with .each

# How do you add elements to an Array?

You can use push or unshift to add to an array, depending on where you would like to add the new element (push adds to the end of the list, unshift adds to the beginning and moves every element down)

# Given the Array `["Laura", "Fiona", "Tori"]`, how would you replace `"Fiona"` with `"Florence"` so that you end up with `["Laura", "Florence", "Tori"]`?

Since "Fiona" is in the first spot (array-wise) you can replace it within an array by saying arr[1] = "Florence" and now "Fiona" is "Florence"

# What do the methods `push`, `pop`, `shift`, and `unshift` do?

These methods add and remove elements to your array. Push and unshift add to an array (push adds to the end, unshift adds to the beginning of the list). Pop removes from the end of the array, shift removes from the beginning. The important distinction is that shift/unshift will change the location of your existing elements on the list, and pop/push will not.

# How do you determine how many elements are in an Array?

You can use .length to determine the number of elements in an array. 

# How would you reverse the order of elements in an Array?

Ruby has a lovely .reverse function, so you can apply that to an array and it will reverse the order of the elements 

# How would you convert a String `"Sumeet Jain"` into an Array `["Sumeet", "Jain"]`? How about to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`? How would you convert the Array back into a String?

Turning a string into an array is "splitting" it (.split) ie taking the single destination of a string and making it into multiple items on a list. So, if name = Sumeet Jain, you can also say arr = name.split, and the string now becomes the two words. If you put “” after .split it tells ruby that you want the individual characters within a string (“s” “u” etc)
Since splitting the name turned it into an array, you can bring it back to a string by joining it back together with .join!