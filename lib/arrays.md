---
title: Arrays
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is an Array?

Arrays are objects that store a list of values. Each value in the list is an element of the array, starting at an index of 0. 


# What are some examples of information that would be Arrays as opposed to some other data type?

Addresses, emails, and other large lists of data

# What is one way, using Ruby, to retrieve the 6th element in an Array? How about the 8th element? What happens if you try to retrieve the value of the _9999th_ element (or some element that doesn't exist in the array)?

You can retrieve array elements by using their index or negative index. 
1.) To retrieve the 6th element, you could do:
    arr = [1,2,3,4,5,6,7,8]
        puts arr[5]             #=> 6
        
2.) If you want to retrieve the 8th element, you can do arr[7]. If it's the last element in an array, it might be faster to do something like arr[-1]

3.) If you try to return the value of an element that doesn't exist, it will return nil. If you are trying to use 
floating values like 0.99998 when searching by index, it will disregard the floating numbers and only pay attention to the integers 
(i.e the numbers to the left of the decimal).  For example:
 arr = [1,2,3,4,5,6,7,8]
        puts arr[10]    #=> nil
        
 arr = [1,2,3,4,5,6,7,8]
        puts arr[0.9998]    #=> 1 
        


# The previous question asks about finding, for example, the 6th element in an Array. Is it possible to find the **-6th** (Notice the negative symbol!) element in an Array? What does that even mean?

It is possible to find the negative index in an array when working in Ruby,
as the index will wrap the array to compensate imaginary numbers (i.e. a negative number, but not a postive number)
up to the length of the string.
EXAMPLE:
arr = [1,2,3,4,5,6,7,8]
puts arr[-6]        #=> 3

The index of the example is 7. The negative index is -8


# How would you perform an operation on every element inside an Array?

Use the .each method with some sort of iteration. FOR EXAMPLE:
name=["Laura", "Fiona", "Tori"]
name.each do | i |
    i.downcase!
    puts i
end                     #=> ["laura", "fiona", "tori"]

# How do you add elements to an Array?

You can use the push or upshift method.

# Given the Array `["Laura", "Fiona", "Tori"]`, how would you replace `"Fiona"` with `"Florence"` so that you end up with `["Laura", "Florence", "Tori"]`?

name=["Laura", "Fiona", "Tori"]
name[1].replace("Florence")
puts name           #=> Tori
                        Florence
                        Laura

# What do the methods `push`, `pop`, `shift`, and `unshift` do?
1.) PUSH: adds elements to the end of an array. 
        EXAMPLE:
        arr = [1,2,3,]
        arr.push(4)         #=> [1, 2, 3, 4]
        
2) POP: removes and returns the last item in an array (last in, first out: LIFO).
        EXAMPLE:
        arr = [1,2,3,]
        arr.pop
        puts arr                #=> 1
                                    2
        
3) SHIFT: removes the first element from the array and returns it.
    EXAMPLE:
    arr = [1,2,3,]
        arr.shift
        puts arr            #=> 2
                                3
                                
4) UNSHIFT: adds elements to the beginning of the array.
    EXAMPLE
    arr = [1,2,3]
    arr.unshift(0)          #=> [0, 1, 2, 3]

# How do you determine how many elements are in an Array?

In order to determine the number of elements in an array, use the .length method. EXAMPLE:
arr = ["beep", 0, "boop", 1]
puts arr.length         #=> 4

# How would you reverse the order of elements in an Array?

To reverse the order of the elements in an Array, use the .reverse method. You can also use the push and pop methods together by pushing the elements into a secondary array, 
using the popped elemenets in the first array (pop always acts on the last element in the array, and push, unless specified will add these in sequential order into the empty second array)
You could also use a while loop with the push and pop method. 

# How would you convert a String `"Sumeet Jain"` into an Array `["Sumeet", "Jain"]`? How about to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`? How would you convert the Array back into a String?

To convert a string into an array, you can use the split method.
To split each word, you would want to do:
"Sumeet Jain".split(" ")        #=> ["Sumeet", "Jain"]
If you want to turn every character into its own element of the array, do something like:
"Sumeet Jain".split("")         #=> ["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]
To convert the array back into a string, you would use the .join method. Using the newly created array, you could do something like:
["Sumeet", "Jain"].join(" ")        #=> "Sumeet Jain"
["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"].join("")        #=> "Sumeet Jain"
