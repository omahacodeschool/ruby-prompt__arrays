---
title: Arrays
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is an Array?

An array is just a collection of items in order. The items are put in order by separating them with commas, with the first item in position 0, 
next item in position 1, etc. Each comma-delimited item is a variable, and can be acted on individually by the program. 
You can put almost anything in an array, including strings and numbers, and mix them in the same array. 

# What are some examples of information that would be Arrays as opposed to some other data type?

It seems to me the important thing about an array, as opposed to just a list, is that you can point to a specific slot or slots in the array and 
work with whatever is in that slot, instead of only working with the entire list. So for example a membership list, which you might use to communicate with all members or specific ones. 
Or perhaps a list that is in some kind of ranking order. For instance, a list, in order, of the people who finished the Omaha Marathon, if you were
giving some kind of award to the first 20 finishers. Concert ticket orders that are being filled on a first-come, first-served basis.


# What is one way, using Ruby, to retrieve the 6th element in an Array? How about the 8th element? What happens if you try to retrieve the value of the _9999th_ element (or some element that doesn't exist in the array)?

You can ask Ruby for the 6th element. Say I have an array called TestArray. Because I like to see output, I would write puts TestArray[6] to 
show the element in slot 6. For the 8th element, change TestArray[6] to TestArray[8]. 

# The previous question asks about finding, for example, the 6th element in an Array. Is it possible to find the **-6th** (Notice the negative symbol!) element in an Array? What does that even mean?

The code line "puts TestArray[-6]" would produce the 6th item from the end of the array. 

# How would you perform an operation on every element inside an Array?

To perform an operation on every element in an array, or even a range of them, you would use a loop.
In repl.it I made an array with the names of the seven dwarves in the Snow White story.
(First I put "Grouchy" or "Grumpy" but fixed it.) Anyway, the code below produces the names in the array one at a time.
From The Bastard's Book it looks like there would be several ways to do make a loop that does this.

TestArray.each do |x|
    puts x
end

# How do you add elements to an Array?

With Ruby there seem to be several ways to do anything. In repl.it I used the "push" method. It adds new items after the last item in the 
existing array. The program below returns a list of 10 Snow White characters beginning with "Happy" and ending with "the Evil Queen."
Note to me: At least on repl.it, and I extrapolate from that everywhere, if I have a space, as in TestArray.push (variables) 
instead of TestArray.push(variables) I get an error message. 

TestArray = ["Happy", "Dopey", "Sleepy", "Sneezy", "Grumpy", "Bashful", "Doc"]
TestArray.push("Snow White", "the Huntsman", "the Evil Queen")
puts TestArray.join(", ")


# Given the Array `["Laura", "Fiona", "Tori"]`, how would you replace `"Fiona"` with `"Florence"` so that you end up with `["Laura", "Florence", "Tori"]`?

This "works" but there must be a better way to do it. It returned the "["Laura", "Florence," Tori"]" array but seems limited. If you had 
25 replacements instead of one making a separate array for each one would be clunky. I learned a little about "map" method, and not-enough-yet about what a block is. 
#Replace Fiona with Florence in an array
Names = ["Laura", "Fiona", "Tori"]
NewName = ["Florence"]
Names.map! do |x| x=="Fiona"? NewName: x 
end
puts Names

#BETTER WAY TO DO THIS
#VERSION 1
#Thank you for the help. This is the most simple way
#to replace "Fiona" with "Florence." It's main limit is you have
#to already know where "Fiona" is in the array. So I did VERSION 2 and 3.
Names = ["Laura", "Fiona", "Tori"]
Names[1]="Florence"
puts Names #(The output here is Laura, Florence, Tori on separate lines.)

#VERSION 2
#This was an intermediate stage, and I just wanted
#to save it in my notes. 
#I wanted to do a scalable version. If there were 10,632 names in 
#the array instead of 3, I wanted to be able to find the value
#"Fiona" in the list, and replace it with "Florence."
#With this one, I thought there must be a method to find
#out what position in the array would go with the value "Fiona" and I found "index." 
Names = ["Laura", "Fiona", "Tori"]
Names.index "Fiona" #This returned the value 1 in green text in repl.it.

#VERSION 3
#On a hunch I put [Names.index "Fiona"], which had returned "1" in green type,
#into the space where I had the [1] in version 1. 
#It made the substitution I was looking for, and seems like
#it would work in a much larger array. 

Names = ["Laura", "Fiona", "Tori"]
Names[Names.index "Fiona"]="Florence"
puts Names #(The output here is the same as Version 1. This line is just my way of finding out if it worked.)












# What do the methods `push`, `pop`, `shift`, and `unshift` do?

"Push" adds items after the last item in an array. "Pop" is the opposite of "Push." It removes the last item in an array. If there is a
number in parentheses next to the method, like Pop(2), it deletes the last (whatever the number is) items in the array. In the sample I worked up 
on repl.it, the "pop" removed "Bashful" and "Doc" and the "push" added the three variables in the parentheses.

#Using Push and Pop methods to change the content of an array
TestArray = ["Happy", "Dopey", "Sleepy", "Sneezy", "Grumpy", "Bashful", "Doc"]
TestArray.pop(2)
TestArray.push("Snow White", "the Huntsman", "the Evil Queen")

"Shift" and "Unshift" are like "Pop" and "Push" except that they do their work at the beginning of an array instead of
at the end. Shift more or less equals Pop, and Unshift more or less equals Push. The "shift" method in my little program below deleted "Happy" through "Sneezy" from the front of TestArray, and "unshift" 
added the three variables in parentheses to the beginning of the array, so that "Snow White" is now the first variable in the array.
If I go back to remembering that each item in an array is in some kind of enumerated "slot," then "shift/unshift" become easier to remember,
because it seems to me that unshift would shift all of the other variable in the array over to make room at the beginning of the array, and "shift"
would move them all over to fill in the positions that were previously occupied by the variables that were "shifted" out.
"Pop" and "Push" would leave everything at the beginning of the array in place.

TestArray = ["Happy", "Dopey", "Sleepy", "Sneezy", "Grumpy", "Bashful", "Doc"]
TestArray.shift(4)
TestArray.unshift("Snow White", "the Huntsman", "the Evil Queen")
puts TestArray
puts TestArray

# How do you determine how many elements are in an Array?

I would use the "length" method. If I have an array called "TestArray" and it has 7 items in it, TestArray.length would return 7. 

# How would you reverse the order of elements in an Array?

I would use the "reverse" method. If I have an array called "TestArray" with 1,2,3,4,5 in it, TestArray.reverse would return 5,4,3,2,1.

# How would you convert a String `"Sumeet Jain"` into an Array `["Sumeet", "Jain"]`? How about to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`? How would you convert the Array back into a String?

Kind of proud I got this one. Less looking up. Found there was a "split' method and tried it in repl.it. Worked.
Split makes sense. It does what the name says it does. It splits the string when it finds whatever is in the quote marks.
I guess what I set up would only work if the keyboarding was accurate. A double space 
String = "Sumeet Jain"
String.split(" ") #returns array ["Sumeet", "Jain"]
String.split("") #returns array with each letter and the space as separate variables in an array
String.split("  ") #if you accidentally put a double space, it returns ["Sumeet Jain"] because 
it didn't find what it wanted.
"Split" seems to have a default of splitting at each space. I used a longer string, 
String = "We, the People of the United States, in order to form a more perfect Union . . ."
String.split #returned each word as a separte variable, the commas stayed with the variable preceding them, and
every dot in the ellipsis was a separate variable in the newly formed array because I had added spaces between.