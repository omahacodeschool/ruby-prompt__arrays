---
title: Arrays
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is an Array?

A way of making a list

# What are some examples of information that would be Arrays as opposed to some other data type?

['Alvin', 'Simon', 'Theodore'] [1, 2.0, 'warp speed']

# What is one way, using Ruby, to retrieve the 6th element in an Array? How about the 8th element? What happens if you try to retrieve the value of the _9999th_ element (or some element that doesn't exist in the array)?

First name your array such as WeDidntStartTheFire. List your objects such as ['Harry Truman', 'Doris Day', 'Red China', 'Johnnie Ray', 'South Pacific', 'Walter Winchel', 'Joe DiMaggio', 'Joe McCarthy', 'Richard Nixon', 'Studebaker', 'Television', 'North Korea', 'South Korea', 'Marilyn Monroe'].
To retrieve the 6th element use WeDidntStartTheFire[5]. To retrieve the 8th element WeDidntStartTheFire[7]. When retrieving the 9999th element nil, nothing, is produced because there is nothing in that slot.

# The previous question asks about finding, for example, the 6th element in an Array. Is it possible to find the **-6th** (Notice the negative symbol!) element in an Array? What does that even mean?

To find the -6th element you would use WeDidntStartTheFire[-6].  This would produce the object 6th from the end of the array.  You would not need to adjust your requested number to be one off because it still counts the first object as zero.

# How would you perform an operation on every element inside an Array?

Use the method each. Name.each do |variable|

# How do you add elements to an Array?

Insert new elements with name.insert(3, 'text'). 3 being the position it should be inserted to.

# Given the Array `["Laura", "Fiona", "Tori"]`, how would you replace `"Fiona"` with `"Florence"` so that you end up with `["Laura", "Florence", "Tori"]`?

Use delete_at to delete the number 1 element. Then use the insert method above to insert 'Florence' as the number 1 element.

# What do the methods `push`, `pop`, `shift`, and `unshift` do?

Push adds an object to the end of your array. Pop removes the last object from the array. Shift removes the first element from the array and returns it. Unshift adds objects to the beginning of the array.

# How do you determine how many elements are in an Array?

use name.count

# How would you reverse the order of elements in an Array?

puts name.reverse

# How would you convert a String `"Sumeet Jain"` into an Array `["Sumeet", "Jain"]`? How about to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`? How would you convert the Array back into a String?

'Sumeet Jain'.split(' ') and 'Sumeet Jain'.split("").   Using .join after either array would convert it back to a string.