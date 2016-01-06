---
title: Arrays
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is an Array?

An array is an ordered collection or list of values that is integer-indexed, meaning each value is automatically assigned an integer for its place in the array, starting at zero.
An array can contain a combination of different types of data (numbers, strings, objects, etc...).

# What are some examples of information that would be Arrays as opposed to some other data type?

Many things that we see in the real world would require arrays in order keep records of the data or information pertaining to them. For instane,
if I wanted to write a program that keeps track of the books I'm reading, it would be useful to use arrays as the information stored will be a variety of 
types. I might want to use numbers to show the total number of pages the book contains and perhaps an index to different chapters or topics. I would need strings to 
capture my favorite quotes or passages. All of this data could be stored in an array for each book. I would also be able to use arrays for a phonebook app
that keeps track of contacts and their respective contact information for the same reason as the first example. I would most likely want to make
an ordereed list that contains multiple kinds of data,

# What is one way, using Ruby, to retrieve the 6th element in an Array? How about the 8th element? What happens if you try to retrieve the value of the _9999th_ element (or some element that doesn't exist in the array)?

Say we had a simple array called my_simple_array that contained the following data:
["dog", "cat", "mouse", "flea", 23, "zipper", "boomerang"]
We would be able to retreive the 6th element in the array like so:
my_simple-array[5]
Notice that we wouldn't use [6] because the indices in Ruby arrays are zero-based (they start at zero instead of "1").

# The previous question asks about finding, for example, the 6th element in an Array. Is it possible to find the **-6th** (Notice the negative symbol!) element in an Array? What does that even mean?

It is possible to find the -6th index in an array. Instead of starting at the beginning (left) side of the array (at zero, of course), using a negative
index would begin at the end (the right side) of the index and would go to the right 6 indices in this case. Because my above array example contained 6 
indices, using my_simple_array[6] would retrieve "dog" in this example. 

# How would you perform an operation on every element inside an Array?

While researching, I found two different ways that could allow one to perfor an operation on every element inside an array: Array#map and Ay#each. The main difference between
the two (from what I can tell) is that Array#map actually returns a new array with whatever operations were performed, while Array#each would return the original array.


# How do you add elements to an Array?

The best way to add elements to an Array is by using the Array#push method. "Push" allows us to add elements to the end of an Array.
Here is an example:
italian_food= ["pizza", "calzone", "spaghetti"]
puts italian_food.push("calamari")

From this, we would get the following as a result:
pizza
calzone
spaghetti
calamari

An easier way (when creating a new array, for instance), might be to simply do the following:
italian_food[3] = "calamari"

# Given the Array `["Laura", "Fiona", "Tori"]`, how would you replace `"Fiona"` with `"Florence"` so that you end up with `["Laura", "Florence", "Tori"]`?
The easiest way that I know how to do this is simply to refer to the index of "Fiona" (in this case the index is "1") and redefine it, so to speak (not sure if that's the right terminology).
Example:
Array[1] = "Florence"
Then, using "puts Array" should then give us ["Laura", "Florence", "Tori"]. 

I hope i'm understanding the question correctly.

# What do the methods `push`, `pop`, `shift`, and `unshift` do?

The "push" method allows you to add an element to the end (right side) of an array (see above example). 
The "pop" method lets remove the element at the end (right side) ofan array.
The "shift" method removes the element at the front (left side) of an array.
The "unshift" method adds an element to the front (left side) of an array.


# How do you determine how many elements are in an Array?

The "length" method can tell us how many elements are in an Array.

Example:
italian_food= ["pizza", "calzone", "spaghetti"]
puts italian_food.length would give us "4" as a result.

# How would you reverse the order of elements in an Array?

Using the "reverse" method would give us a new array with the contents of the original array in reverse order.

Example:
italian_food= ["pizza", "calzone", "spaghetti"]
puts italian_food.reverse would give us: 
spaghetti
calzone
pizza

# How would you convert a String `"Sumeet Jain"` into an Array `["Sumeet", "Jain"]`? How about to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`? How would you convert the Array back into a String?

By using "split" we can take a string and put it into an Array. 
str = "Sumeet Jain"
array = str.split(" ") 
#note the space in beteen the quotes
=> ["Sumeet", "Jain"

To acheive the second result, you would simply eliminate the space between the quotes as follows:
str = "Sumeet Jain"
array = str.split("")
=> ["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]

To put the above array back into a string, we would use the "join" method like this:
array = ["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]
str = array.join
=> "Sumeet Jain"
