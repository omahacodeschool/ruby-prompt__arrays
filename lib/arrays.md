---
title: Arrays
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is an Array?

An Array is a list of values, often used as a way to keep large amounts of data organized.

# What are some examples of information that would be Arrays as opposed to some other data type?

Information that would be an Array in Ruby is a set of values that needs to be searched, tested, reorganized, or ammended. 
An example of information that would be an Array could be all the foods contained in a single recipe, or the individual names of all the students in a cohort.

# What is one way, using Ruby, to retrieve the 6th element in an Array? How about the 8th element? What happens if you try to retrieve the value of the _9999th_ element (or some element that doesn't exist in the array)?

You can use integers to address locations in an Array. So, you could put the index number 6 or 8 in brackets after the Array name to retrieve the 6th or 8th elements (always remembering that counting begins at 0.
If you tried to retrieve the value of a position in an Array that does not exist, the program would return 'nil', meaning nothing, because there is nothing there.

# The previous question asks about finding, for example, the 6th element in an Array. Is it possible to find the **-6th** (Notice the negative symbol!) element in an Array? What does that even mean?

Yes. Negative index values count from the end of the Array, so the '-6th' value in an Array would be the sixth value from the end.

# How would you perform an operation on every element inside an Array?

You could use the method Each to apply an operation to every object an Array points to. 
If you have an Array called 'NamesofStudents', which includes the name of every student in the upcoming Omaha Code School Cohort, you could use .each to have the computer say hi to each and every student.
You would use the Each method and a variable that Each can use to point to the objects in an Array, in this case let's say 'name', surrounded by vertical bars.
Then you can enter what you want the computer to do (in this case let's say write out "Hi, Name!", where Name is actually the individual names of the students) to each object in the Array.

# How do you add elements to an Array?

You can use the 'Push' method to add an object to the end of an Array. Using the previous example of names of students in the OCS cohort, let's say John Stamos joined late and needs to be added.
I could put NameofStudents.push 'John Stamos' to add his name to the end of the list.

# Given the Array `["Laura", "Fiona", "Tori"]`, how would you replace `"Fiona"` with `"Florence"` so that you end up with `["Laura", "Florence", "Tori"]`?

If I knew I wanted to repalce Fiona with Florence, I would search through my Array to find the object "Fiona" using the Each method.
To do this, I could ask my program to check "Fiona" against each object of an Array to find out where it matches.
Then, I could write an 'if','else' statement so for each object my program returned that matches "Fiona", it would replace that object with "Florence".
Alternatively, since we know the position of the element we are trying to modify, we can use Ruby's 'delete_at' and 'insert' methods to remove Fiona from position 1 and add Florence.

# What do the methods `push`, `pop`, `shift`, and `unshift` do?

Push adds an object to the end of an Array, where Pop removes the last object from the end of the Array and tells you what it was.
Shift and Unshift do those same actions, but to the first object in an Array.

# How do you determine how many elements are in an Array?

Use the Length method to determine how many elements are in an Array.

# How would you reverse the order of elements in an Array?

You can use the Reverse method to reverse all the elements in an Array. 

# How would you convert a String `"Sumeet Jain"` into an Array `["Sumeet", "Jain"]`? How about to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`? How would you convert the Array back into a String?

You could use the Split method on the string "Sumeet Jain" to turn it into an Array by splitting the String where a space occurs. This would split the string into two objects and separate them by a comma (forming an Array).
You could also split the String "Sumeet Jain" after every character using the Split method and splitting on an empty string delimeter, indicated by "". This will return all the characters as an Array.

Alternatively, you could split the String by characters using the Unpack method on the string. The directive 'a' will return characters as individual Strings in an Array.
Since there are 11 characters in "Sumeet Jain" (including the space), I could enter "Sumeet Jain".unpack('a'*11), which would ask my program to turn each character into a separate String in an Array 11 times.

You can covert the Array back into a String using the command .to_s or the Join command.
