---
title: Arrays
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is an Array?

An array is a collection of objects that are indexed by integer, starting with 0.

# What are some examples of information that would be Arrays as opposed to some other data type?

Obviously arrays are different than strings in that you can put a whole bunch of strings in an array and then they’re indexed by number and you can call then up accordingly, instead of just having a whole load of strings out there individually. Arrays are different than hashes in that arrays are just indexed by number and hashes are indexed by “keys,” but I haven’t gotten that far into hashes yet so I’m still hazy on the significance of this difference. 

# What is one way, using Ruby, to retrieve the 6th element in an Array? How about the 8th element? What happens if you try to retrieve the value of the _9999th_ element (or some element that doesn't exist in the array)?

Let’s say the array is called this_array. If you want to retrieve the 6th element, you would say “puts this_array[5]” and that will bring back the 6th item in the array since Ruby starts counting at zero. If you want the 8th element just put 7 in the brackets. If you try to retrieve the value of an element that doesn’t exist (like the 9999th element in an array of 200), Ruby answers “nil” meaning there is nothing in that position.

# The previous question asks about finding, for example, the 6th element in an Array. Is it possible to find the **-6th** (Notice the negative symbol!) element in an Array? What does that even mean?

Yes, you can use the negative positions of an array if you’re looking for a character based on it’s distance from the end of the array. Ruby just counts backward instead of forward. 

# How would you perform an operation on every element inside an Array?

You do that using the each method. This method will let you do something to each item in an a block of code, but it won’t actually change the original array.

# How do you add elements to an Array?

You can use the shovel operator (<<), also known as push (same as using “.push”), or simply a “+” sign ([1,2,3] + [4] = [1,2,3,4])  to add something to the end of an array. Unshift lets you add things to the beginning of an array (see below for more on push/unshift).

# Given the Array `["Laura", "Fiona", "Tori"]`, how would you replace `"Fiona"` with `"Florence"` so that you end up with `["Laura", "Florence", "Tori"]`?

You can replace elements in an array using .replace, but thus far I’m only able to figure out how to replace all of the elements and not just point to a specific one. I’m assuming there is indeed a way to do that. I’m stuck:

array = ["Laura", "Fiona", "Tori"]
array.replace(["Laura", "Florence", "Tori"]) 
array

Oooops – just realized this one was still open. Thanks for the extra guidance on how to do this. I get it now. To replace just one element with another, you can do it the same way you can assign it a value in the first place:

this_array = Array.new
this_array[0] = "food"
this_array[1] = "clothing"
this_array[2] = "shelter"
this_array[0] = "netflix"      # if you decide your priorities have changed, you just re-assign that position
this_array

# What do the methods `push`, `pop`, `shift`, and `unshift` do?

Push adds something to the end of an array. Pop removes something from the end of an array. Shift will take something off of the beginning of an array (or .shift(2) will chop off the first two items – or however many correspond to the number you put in the parentheses). Unshift has the opposite effect and allows you to add an element or elements to the beginning of an array.

# How do you determine how many elements are in an Array?

If your array is called “this_array,” enter “this_array.length” and Ruby returns the number of elements in the array.

# How would you reverse the order of elements in an Array?

If your array is called “this_array,” enter “this_array.reverse” and Ruby will give you all of the elements in the array in reverse order.

# How would you convert a String `"Sumeet Jain"` into an Array `["Sumeet", "Jain"]`? How about to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`? How would you convert the Array back into a String?

You can convert a string into an array using the split method:  "Sumeet Jain".split(',') will return the array ["Sumeet", "Jain"]. Conversely, you can turn an array into a string using the join method:  ["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"].join = "Sumeet Jain".