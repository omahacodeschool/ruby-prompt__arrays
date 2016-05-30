---
title: Arrays
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is an Array?

In Ruby an array is a collection of data. An array could contain multiple numbers or strings, each one having a position in the array.
An array is created using square brackets in which the items in the array are listed, separated by commas:

    starks = ["Ned", "Catelyn", "Robb", "Jon", "Sansa", "Arya", "Bran", "Rickon"]

This array lists members of the Stark family and is labelled as such using a label and "="


# What are some examples of information that would be Arrays as opposed to some other data type?

An array is a collection of data, so any kind of lists, whether that's a list of names, dates, or other sets of data.


# What is one way, using Ruby, to retrieve the 6th element in an Array? How about the 8th element? What happens if you try to retrieve the value of the _9999th_ element (or some element that doesn't exist in the array)?

To find out what exists in the 6th position, you can use square brackets with a specified number after the label. This will look a lot like the way you find a specific character in a string. And like a string, the first object is at position 0, so to find the sixth item you'll want to find the element in position 5.
To find the sixth member of the Stark family you would use:

    starks[5]

and the VM would return "Arya" as it is in the fifth position. To find the 8th element you would use "starks[7]" and get "Rickon" as he is the eighth member of the Stark family. 
Attempting to find an element at a position that doesn't exist will result in a "nil" because that position is empty.


# The previous question asks about finding, for example, the 6th element in an Array. Is it possible to find the **-6th** (Notice the negative symbol!) element in an Array? What does that even mean?

A negative number between the square brackets will tell the VM to start counting backwards, starting with the last object at the -1 position. To find the object in the -6th position you would use the same method as above:

    starks[-6]

This will return the answer "Robb".


# How would you perform an operation on every element inside an Array?

To perform an operation on each element in an array you use the ".each" method. 
With .each you can start a loop and it will execute the specified code on each object in the array individually. You can also use curly brackets for simpler processes and the VM will recognize that it will repeat the operation on each element, like this:

    starks.each {|x| puts x " says hello"}

This will return each name with "says hello" after it. The 'x' between the vertical slashes is a variable that represents the elements in the array. Then we can use that variable in any way necessary.


# How do you add elements to an Array?

You can add elements using the "shovel" operator (<<). This method appends an element to the end of an array like this:

    starks << "Talisa"

This will add the string "Talisa" to the end of the starks array.


# Given the Array `["Laura", "Fiona", "Tori"]`, how would you replace `"Fiona"` with `"Florence"` so that you end up with `["Laura", "Florence", "Tori"]`?

You can replace an item in an array by specifying a position and defining a new element for it. To replace "Fiona" you need to determine that strings position, in this case 1.
Then, like when you want to find out whats at a specific position, you list the position in square brackets, then "=", and the new element like this:

    ary = ["Laura", "Fiona", "Tori"] 
    ary[1] = "Florence"

This tells the VM to replace the element at position 1 with the new string "Florence".


# What do the methods `push`, `pop`, `shift`, and `unshift` do?

The method "push" appends objects to the end of the array much like "<<" but it allows you to append multiple elements to the array at once.
The "pop" method does just the opposite, removing elements from the end of an array. You can specify the number of elements to remove using parentheses.
The "shift" method works like "pop" but it removes the first element in the array and shifts all of the other elements in the array one position closer to the first. Like "pop", you can specify a number of elements to remove with a number in parentheses.
Finally you can use "unshift" to prepend an element to the first position in an array. Like "push" you can prepend multiple elements, the first being at position 0, the next at position 1, and so forth


# How do you determine how many elements are in an Array?

The .length method will return the number of elements in an array.


# How would you reverse the order of elements in an Array?

To reverse the order of elements in an array you use ".reverse!". This will reorder the elements in the array itself. Using ".reverse" without the exclamation point creates a new array from the original with all of the elements in reverse order.


# How would you convert a String `"Sumeet Jain"` into an Array `["Sumeet", "Jain"]`? How about to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`? How would you convert the Array back into a String?

To convert a string into an array, use the .split method. This will turn the string into substrings that are split where there were spaces in the original string.
To turn each character of the string into a substring in an array, still use the .split method, but now you add a modifier to the end in parentheses like this:

    "Sumeet Jain".split(//)
    
Now the VM will split the string and return an array with 11 elements, each being one character including the space. This works because the two slashes in parentheses do not have a space in between them. If you did put a space between them the string would split anywhere there is a space.
To join all those substrings back into one string, use the .join method. This will not add spaces where the first string was split, but we can specify a separator in parentheses like this:

    ["Sumeet", "Jain"].join(" ")
    
This will return a string "Sumeet Jain". Not defining a separator will return "SumeetJain".