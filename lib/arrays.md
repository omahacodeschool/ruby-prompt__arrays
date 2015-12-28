---
title: Arrays
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is an Array?

An array is an object in Ruby used to store an ordered list of values.  Each value within the array acts as a variable. 

# What are some examples of information that would be Arrays as opposed to some other data type?

An array would be useful for storing information that someone might want to recall easily at some later point in time.  
For example: if someone wanted to store a list of names (i.e. Paul, John, George) they could store them as a list of variables:
name1 = Paul
name 2 = John
name 3 = George
or they could store the names as the array:  names = [Paul, John, George]

# What is one way, using Ruby, to retrieve the 6th element in an Array? How about the 8th element? What happens if you try to retrieve the value of the _9999th_ element (or some element that doesn't exist in the array)?

One way to retrieve an element in an array is to use [].  
For example: in the array   numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9]
If someone wanted to retrieve the 6th character they would type:  "puts numbers[6]" and Ruby would return the 6th character which in this case would be 7.
Ruby will return any character in the array's index that someone puts inside the [], and Ruby will return "nil" if the absolute value of the number inside the [] falls
outside the actual number of characters within the array.  

# The previous question asks about finding, for example, the 6th element in an Array. Is it possible to find the **-6th** (Notice the negative symbol!) element in an Array? What does that even mean?

Yes.  In the above example if someone wanted to find the -6th character using: numbers[-6] Ruby would return the 6th character from the end of the array.
In this case Ruby would return 4. 

# How would you perform an operation on every element inside an Array?

To perform an operation to every element inside an array Ruby uses the .each method.
If I wanted to multiply each number in the previous array by 10 I would write:
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9]
numbers.each do |x|
    puts x * 10
end


# How do you add elements to an Array?

One way to add information to an array is to use "+" to add another array.  To add the numbers 10 and 11 to the numbers array above I would type : numbers + [10, 11].
Whatever I put inside the [] will be added to the end of the array.

Another way to add to an array is by using the .push method.  This method also adds information to the end of an array and would look like this: numbers.push(10, 11).
Unlike the first method, .push will modify the numbers array.  Which means that each time I use the numbers array later in the code it will
include the numbers 10 and 11.

One final way to add to an array is by using << to push information into an array.  Similar to .push, this method modifies the array but only allows for one piece of information
to be added at one time.  i.e  "numbers << 10"  will add the number 10 to the end of the array, but an error will occur if I try to do "numbers << 10, 11"


# Given the Array `["Laura", "Fiona", "Tori"]`, how would you replace `"Fiona"` with `"Florence"` so that you end up with `["Laura", "Florence", "Tori"]`?

One way to replace "Fiona" with "Florence" would be to use the command: array[1] = "Florence".  This is telling Ruby, that the element with the index of 1
is now equal to "Florence".

# What do the methods `push`, `pop`, `shift`, and `unshift` do?

'push' will add elements to the end of an array.
'pop' will delete the last element in an array and return it to you.
'shift' will return the first element in an array and then delete it.  It will then shift all other elements in the array down by one.
'unshift' will add elements to the front of an array.  It will then shift the other elements in the array up by 1.

# How do you determine how many elements are in an Array?

Arrays keep track of thier length at all times.  At any time you can use .length to check the length of an array.  

# How would you reverse the order of elements in an Array?
".reverse" will return the elements in the array in reverse order.  ".reverse!" will reverse the array in place.  Meaning that if I were to write: numbers.reverse!
the next time I typed "puts numbers" Ruby would return the array in reverse order. 

# How would you convert a String `"Sumeet Jain"` into an Array `["Sumeet", "Jain"]`? How about to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`? How would you convert the Array back into a String?

One method to convert "Sumeet Jain" into the array ["Sumeet", "Jain"] would be the .split method.  The .split method, by default, will split the string at all spaces in the string.
To convert "Sumeet Jain" into an array where each character is its own element use .split(//)