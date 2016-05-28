---
title: Arrays
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is an Array?

An array is a data object representing an ordered list of values. 

# What are some examples of information that would be Arrays as opposed to some other data type?

Said simply, an array is a list that stays in a given order - i.e., the order you wrote it. 
An array is an object referencing other objects, vs. the number and string data types, which represent an object itself. 
Consider an ingredient list to bake a cake. The list "contains" milk, eggs, and flour, but it doesn't really contain those things (like a cake would)
Arrays can contain any type of data object.

# What is one way, using Ruby, to retrieve the 6th element in an Array? How about the 8th element? What happens if you try to retrieve the value of the _9999th_ element (or some element that doesn't exist in the array)?

The array could first be defined, which would look something like: array = ['a', 'b', 'c', 'd', 'e', 'w', 'x', 'y', 'z']
To retrieve the 6th element - the 'w' - we would actually enter puts array[5], because the first slot (where 'a' is) is the zero slot.
To retrieve the 8th element - the 'y' - we would enter puts array[7]
If we try to retrieve an element that isn't there, the program responds with a nil value, represented by a blank row

# The previous question asks about finding, for example, the 6th element in an Array. Is it possible to find the **-6th** (Notice the negative symbol!) element in an Array? What does that even mean?

It is possible to find the -6th element in an array - in the array defined above, it is the 'd' value.
The negative value means it will begin counting backwards, staring at the end of the list. 
When it starts at the end, however, it does not start with zero.
Thus we can expect the [-6] element to be the sixth from the end, whereas the [6] element would be the 7th from the left.

# How would you perform an operation on every element inside an Array?

To perform an operation on every element within an array, we use the each method. 
For example, given the array below, to list the names with a lowercase, we'd write:
["Laura", "Fiona", "Tori"].each{ |i| puts i.downcase}

# How do you add elements to an Array?

To add an element, we can use two left-angled brackets: <<
Referencing the defined array from before, to add the letter 'q', we'd type: array << 'q'

# Given the Array `["Laura", "Fiona", "Tori"]`, how would you replace `"Fiona"` with `"Florence"` so that you end up with `["Laura", "Florence", "Tori"]`?

Since this array is short and can thus we can easily identify the position of the value we want to change,
we can easily do that via index. That code would look like this:
  names = ["Laura", "Fiona", "Tori"]
  names[1].replace("Florence")
  puts names

# What do the methods `push`, `pop`, `shift`, and `unshift` do?

Push permanently adds elements to the end of an array (via .push or <<)
Pop permanantly removes elements from the end of an array (via .pop or .pop(n), n = # to remove)
Shift permanently removes elements from an array (like .pop), but removes from the front (via .shift or .shift(n), n = # to remove)
Unshift permanantly adds elements to the beginning of an array

# How do you determine how many elements are in an Array?

To determine how many elements in an array, we can use the count method (e.g. array.count)

# How would you reverse the order of elements in an Array?

To temporarily reverse the elements in an array, we'd use the .reverse method.
To permanently reverse the elements in an array, we'd add an exclamation point to the method: .reverse!

# How would you convert a String `"Sumeet Jain"` into an Array `["Sumeet", "Jain"]`? How about to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`? How would you convert the Array back into a String?

To convert a string into an array, we can use the split method. 
Whether we convert it into words or characters depends on what we use as the delimiter.
To convert it to words, we'd use a space as a delimiter, notated by " ".
To convert it to letters, we'd use no space, notated by "".
Here's how that code might look:
  name = "Sumeet Jain"
  words = name.split " "
  puts words

  letters = name.split ""
  puts letters

To convert the array back to a string, we can use the join method. That code:
  letters = ["S","u","m","e","e","t"," ","J","a","i","n"]
  string = letters.join
  puts string

To convert the words array back to a string, we'd join using the space as a delimiter
  words = ["Summeet", "Jain"]
  string = words.join(" ")
  puts string
