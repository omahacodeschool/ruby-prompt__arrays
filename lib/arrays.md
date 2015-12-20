---
title: Arrays
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is an Array?

An array is a data object in Ruby that is comprised of an ordered list of some sort of data.  You can fill an array with fixnums, floats, or strings.  You can mix and match.  It's up to the user really.  

Could one of the items in an Array be an Array itself?

Yes, one of the items in an array could be an array itself.  While I'm a bit fuzzy on the possible uses for such a beast, making an array an item in another array creates a two-dimensional array.  Though it's a bit tricky to visualize what you're doing after you've added a third dimension to the mix, by making items in the array that is in another array arrays themselves, I have heard arrays of 7 or 9 dimensions mentioned in association with encryption and codes.  

# What are some examples of information that would be Arrays as opposed to some other data type?

Arrays are great for making lists of data to iterate through.  If you want to do something to a collection of data repeatedly, creating a list and looping through it is great for that.  A array is a good way to collect a big chunk of data and then organize it.  So, let's say you've got an unordered list of names and you want to bring some order to the chaos.  If you have that list as an array you can apply the sort method to it and voila you've got a list in alphabetical order.  If you had a collection of weather data and you wanted to order it from lowest temperature to highest or compare it to another collection of data, you could put it all in an array and accomplish those things via some of the methods available to us for manipulating lists.

# What is one way, using Ruby, to retrieve the 6th element in an Array? How about the 8th element? What happens if you try to retrieve the value of the _9999th_ element (or some element that doesn't exist in the array)?

A simple way to retrieve a given element in an array is to indicate the numerical position of an element in the array.  So, if you've got an array, array_1 = [1,2,3,4,5,6,7,8,9] and you wanted it to return 6, you'd tell the computer the numerical position of 6 in array_1 like so array_1[5].  This might look a bit odd as when counting from 1 to 6, 6 is obviously in the sixth position.  However, as far as the computer is concerned, the count starts with 0, not 1.  So, if you're looking for the first element of array_1, you'd tell the computer array_1[0].  If you wanted the 8th element, same thing.  If you wanted the 9999th element, it'd return a blank.  You can actually create empty arrays, as such, I think that an array is an ever expandable list.  So, if you ask it to retrieve an element that's not in the list, there's a blank space for it, it's just not filled.  Not entirely sure that's how it works, but that's how it made sense to me.

Can you cite the specific term for the value in that blank space?

"nil", evidently, when considering arrays, values that aren't explicitly set to something are set as "nil".  Thus, when you ask for the 9999th element in a given array, assuming you don't have anything set to that particular position, Ruby will return "nil" as that's sort of the default value of a blank space in an array.  Sound about right?


# The previous question asks about finding, for example, the 6th element in an Array. Is it possible to find the **-6th** (Notice the negative symbol!) element in an Array? What does that even mean?

Yes, much as with our earlier prompt about strings, if you tell the computer to search for the **-6th** element in an array it'll start counting from the end of your list backwards.  So if you've got an array like array_1 = [1,2,3,4,5,6,7,8,9] and tell it to look for the **-6th** element of that array, it'll give you 4.  Much like in the discussion of elements of a string, when counting right to left, the count starts with 1, not 0.

# How would you perform an operation on every element inside an Array?

You can iterate through all the elements of an array with a loop.  Something in the form of "for element in array_1..."  Alternatively, you can use the each method to iterate over all the elements in an array.  So, for our array_1 you could say something like ,array_1.each { |x| print x * 3, " "}.  Translated into English that's telling the computer "In array_1, for each variable x multiply it times three and put a space between the results."

# How do you add elements to an Array?

One quick way to do it, using the aforementioned array_1, would be to say array_1[9] = 10.  This is telling the computer that the ninth element is equal to 10.  This only works though if you're trying to tack something onto the end of the array.  If you tried to insert an element into a spot in the array that is already occupied, it wouldn't work.  Say you wanted to insert 4.5 between 4 and 5.  If you tried to use this method, and wrote array_1[5] = 4.5 all you'd be doing is replacing the 5.  So, naturally, we want a method that will allow us to do more than merely add elements to the end of our array.  To do this, you have a number of options.  For example, you can add an element using the push method.  So, you'd write array_1.push(11) if you wanted to tack an 11 onto the end of array_1.  If you wanted to add a 0 to the beginning of our list, you could say array_1.unshift(0).  If you wanted to try to insert 4.5 between 4 and 5 without merely replacing 5 like we did earlier, you could say array_1.insert(4, 4.5).  In that case 4 would be the argument designating the element after which the insertion will be made and 4.5 would be the argument indicating what you were insterting. And so on...

# Given the Array `["Laura", "Fiona", "Tori"]`, how would you replace `"Fiona"` with `"Florence"` so that you end up with `["Laura", "Florence", "Tori"]`?

A quick way to do this would be simply to say array[1] = "Florence".  Essentially, you're telling the computer to go to position 1 and put "Florence" in that position.

# What do the methods `push`, `pop`, `shift`, and `unshift` do?

Push adds an element onto the end of an array.  Pop removes and returns the last item in an array.  Both push and pop modify the array they're used on.  Shift removes the first element of an array and returns it, thus shifting the position of all the elements that follow down by 1.  Unshift does the opposite of this and tacks an element onto the beginning of an array and increases all the numerical positions of the elements that follow up by 1.

# How do you determine how many elements are in an Array?

You'd use the length method.  Again, for our array_1, you'd say something like puts array_1.length and it should print out the number of elements in array_1.

# How would you reverse the order of elements in an Array?

You'd use the reverse method.  So, for array_1, you'd say array_1 = array_1.reverse and the order that the elements are in should reverse.

# How would you convert a String `"Sumeet Jain"` into an Array `["Sumeet", "Jain"]`? How about to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`? How would you convert the Array back into a String?

To convert the string "Sumeet Jain" into an array, you'd use the split method.  So, you'd say "Sumeet Jain".split(" ").  The quotes in the parentheses indicate that the method should use a space to determine where to make its cuts.  However, I found that if you just left that space blank, it would make the same array without that delimiting info.  To break, "Sumeet Jain" down into individual letters and a preserve the space as requested, you'd do the same thing, but instead of having a space between the quotation marks, you'd have no space whatsoever.  So, "Sumeet Jain".split("").  To put Humpty Dumpty back together again, you'd use the join method.  So, if we wanted to make our array_1 into a string of numbers, we'd say array_1.join().  This would produce "123456789".  If you wanted to have the numbers separated by something, you'd include something in the parantheses.  For example, array_1.join("*") will produce "1*2*3*4*5*6*7*8*9".  This is, of course assuming that we're using the array_1 that we started with and not the array_1 we've been modifying throughout this.