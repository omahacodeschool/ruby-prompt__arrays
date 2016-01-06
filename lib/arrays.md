---
title: Arrays
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is an Array?

An array is a data object that stores an ordered list of values. 

# What are some examples of information that would be Arrays as opposed to some other data type?

Arrays can consist of any data type (even more arrays), and are accessed by index numbers. Strings are read character-by-character, in contrast. Arrays can also be used to control flow, though I am not sure just how this works.
Any list whose contents would need to be recalled individually could be stored in an array. 

# What is one way, using Ruby, to retrieve the 6th element in an Array? How about the 8th element? What happens if you try to retrieve the value of the _9999th_ element (or some element that doesn't exist in the array)?

Retrieving an element can be done with:

arr = []
arr[0] = "Jones"
arr[1] = "Koresh"
arr[2] = "Rajneesh"
arr[3] = "Applewhite"
puts arr [2]

Because Ruby is zero-based indexed, to access the 6th element, use:

puts arr [5]

For the 8th element,

puts arr [7]

If we try to retrieve an element that doesn't exist in the array, we get an empty line.

# The previous question asks about finding, for example, the 6th element in an Array. Is it possible to find the **-6th** (Notice the negative symbol!) element in an Array? What does that even mean?

Yes, the -6th element in the array would be the 6th from the end, counting backwards with the last element being '1'.

# How would you perform an operation on every element inside an Array?

Using my above example, I put the cult leaders' names into lowercase:

arr.each{ |x| puts x.downcase}      

# How do you add elements to an Array?

Simply, we can add elements to an array using:

arr.push ("Jouret"),("Shinrikyo") 

# Given the Array `["Laura", "Fiona", "Tori"]`, how would you replace `"Fiona"` with `"Florence"` so that you end up with `["Laura", "Florence", "Tori"]`?

I came up with:

arr = ["Laura", "Fiona", "Tori"]
arr.map! { |element|
   if(element == "Fiona")
       "Florence" 
   else
       element
   end
}
puts arr

# What do the methods `push`, `pop`, `shift`, and `unshift` do?

'push' will insert an element into the array, at the last index. 'pop' will remove the element in the last index. 'unshift' will add an element to the first index, shifting all other elements up one.

# How do you determine how many elements are in an Array?

my_array.length

# How would you reverse the order of elements in an Array?

my_array.sort.reverse

# How would you convert a String `"Sumeet Jain"` into an Array `["Sumeet", "Jain"]`?  

"Sumeet Jain".split (' ')

# How about to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`?

"Sumeet Jain".split ('')

# How would you convert the Array back into a String?

arr = "Sumeet Jain".split ('')
puts arr
puts arr.join ('')