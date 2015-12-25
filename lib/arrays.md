---
title: Arrays
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is an Array?

An array basically acts as a list of variables that can be modified, ordered, recalled, etc. however you command later on.

# What are some examples of information that would be Arrays as opposed to some other data type?

Any type of information that belongs to a group that you'll later want to organize--this could be lists of names, exam scores, a price list, an inventory count, etc.

# What is one way, using Ruby, to retrieve the 6th element in an Array? How about the 8th element? What happens if you try to retrieve the value of the _9999th_ element (or some element that doesn't exist in the array)?

You can call the 6th element of an array using the code puts arrayname[6], while you can call the 8th element using the same code but an 8 instead of 6. If you're not counting like a programmer, you'll need to subtract one from the number in brackets, as the first element recieves the 0 position. If you call an element that doesn't exist in the array, the program will return 'nil'.

# The previous question asks about finding, for example, the 6th element in an Array. Is it possible to find the **-6th** (Notice the negative symbol!) element in an Array? What does that even mean?

Yes, this will find the sixth from last element within the array.

# How would you perform an operation on every element inside an Array?

This can be done with the .each do command. Here's my example from attempting to figure it out for myself:
letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p']
letters.each do |letra|
    puts 'I can say ' + letra + '!'
end

# How do you add elements to an Array?

You just need to add another item to the already established bracketed list.

# Given the Array `["Laura", "Fiona", "Tori"]`, how would you replace `"Fiona"` with `"Florence"` so that you end up with `["Laura", "Florence", "Tori"]`?

Aside from replacing it on the original array list, you can use the code names[1] = 'Florence'.

# What do the methods `push`, `pop`, `shift`, and `unshift` do?

Push adds an object to the end of an array, while pop deletes the last object (and tells you what that deleted object is). Shift removes the first object from the array, while unshift adds a new object at the beginning.

# How do you determine how many elements are in an Array?

I would use the .length command.

# How would you reverse the order of elements in an Array?

I would use the .reverse command.

# How would you convert a String `"Sumeet Jain"` into an Array `["Sumeet", "Jain"]`? How about to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`? How would you convert the Array back into a String?

This is how I converted the string into an array consisting of the two words:
"Sumeet Jain".split(" ")
To convert the string into an array that consists of each separate letter, you need to delete the space from between the quote marks in the parentheses.
To do the opposite, the .join command works the same way:
["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"].join("")
And to convert an array consisting of the two words of your name into a string, you need to add a space between the quote marks in the parentheses.