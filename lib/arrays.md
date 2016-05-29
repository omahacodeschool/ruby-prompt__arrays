---
title: Arrays
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is an Array?

	An Array is a data object that stores an ordered list of values. The index must be an integer. 

# What are some examples of information that would be Arrays as opposed to some other data type?

	An Array is very handy to use for lists or keeping information sorted. You wouldn't add list of student number, student name and there information into one big string but into an Array to keep it sorted. 

# What is one way, using Ruby, to retrieve the 6th element in an Array? How about the 8th element? What happens if you try to retrieve the value of the _9999th_ element (or some element that doesn't exist in the array)?

	I would call by the index of the array such as array[6] or array[8]. If the element in the array being retrieved doesn’t exist you’ll receive nill response. 

# The previous question asks about finding, for example, the 6th element in an Array. Is it possible to find the **-6th** (Notice the negative symbol!) element in an Array? What does that even mean?

	The negative symbol starts the search for the element starting from the end of the array and going backwards.  

# How would you perform an operation on every element inside an Array?

	You would use the either loop or the each method.  An example for the each method is
arr.each do |x|
    puts x
end


# How do you add elements to an Array?
	You can use the push method to add objects to end of an array. 

# Given the Array `["Laura", "Fiona", "Tori"]`, how would you replace `"Fiona"` with `"Florence"` so that you end up with `["Laura", "Florence", "Tori"]`?

	I would use the delete_at method to remove Fiona at index 1 position and then the insert method for Florence at the index 1. 
	
# What do the methods `push`, `pop`, `shift`, and `unshift` do?

	The push method adds an element at end of an array.
	The pop method removes last element in an array and returns it.
	The shift removes the first element and returns it and shifts all other elements down by one. 
	The unshift method prepends object to the front and move other elements upwards.


# How do you determine how many elements are in an Array?

	I would use the length or count method on the array. 
	
# How would you reverse the order of elements in an Array?

	I would use the split method an example would be
	“Summet Jain”.split(‘ ‘)


# How would you convert a String `"Sumeet Jain"` into an Array `["Sumeet", "Jain"]`? How about to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`? How would you convert the Array back into a String?

	I would use the join method such as
	["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"].join(‘’)