---
title: Arrays
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is an Array?

An array is a list of items.

# What are some examples of information that would be Arrays as opposed to some other data type?

Team rosters would work well in an array, as would an ingredient list.

# What is one way, using Ruby, to retrieve the 6th element in an Array? How about the 8th element? What happens if you try to retrieve the value of the _9999th_ element (or some element that doesn't exist in the array)?

If your array is simply
Days = ['Sunday','Monday','Tuesday','Wednesday','Thursday','Friday','Saturday']
#you can simply
Days[whatver day you want to call]

# The previous question asks about finding, for example, the 6th element in an Array. Is it possible to find the **-6th** (Notice the negative symbol!) element in an Array? What does that even mean?

Sure, with this method, Ruby would count down, starting at 0 then negative, backwards around the array until the right one.

# ?How would you perform an operation on everey lement inside an Arrayy 

I am really struggling with this.... am I trying to add bullets to a list of names?  or make a list of numbers to perform mathmatical opperations on?

# How do you add elements to an Array?

I like the 'push method' to add elements to an array.  after you have defines the array, the '<<' symbols are used to add to the end of the array.
teams = ['packers','bears','lions','vikings']
teams << 'cowboys'
teams << 'Lil Cyclones'

# Given the Array `["Laura", "Fiona", "Tori"]`, how would you replace `"Fiona"` with `"Florence"` so that you end up with `["Laura", "Florence", "Tori"]`?

I am actually replaceing the '1' spot in the array, so...
names = ["Laura", "Fiona", "Tori"]
names[1]='Florence'
names

# What do the methods `push`, `pop`, `shift`, and `unshift` do?

The Push Method will add elements to the end of your array, the pop method will remove the last object in the array, while the shift command will remove
the first element.  The unshift method will put an element at the beginning of an array
names = ["Laura", "Fiona", "Tori"]
names.unshift('Brett')
names

# How do you determine how many elements are in an Array?

by puting .size at the end of the name of the array, ruby will tell you how many elements are present.
names = ["Laura", "Fiona", "Tori"]
names.unshift('Brett')
names
puts names.size

# How would you reverse the order of elements in an Array?

with the reverse command, I made a new variable that would be just for the array in reverse
names = ["Laura", "Fiona", "Tori"]
try = names.reverse
puts try

# How would you convert a String `"Sumeet Jain"` into an Array `["Sumeet", "Jain"]`? How about to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`? How would you convert the Array back into a String?

The split command will convert a string to an array, then adding ("") will give every character its own space in the array.
"Sumeet Jain".split