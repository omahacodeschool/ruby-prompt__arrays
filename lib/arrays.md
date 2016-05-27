---
title: Arrays
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is an Array?

    #An Array is an ordered list of objects, you know that it is an array by the 
    #square brackets.
    
    #example: ['dog', 'cat', 'bird', 21]
    
# What are some examples of information that would be Arrays as opposed to some other data type?

    # list of names
    # list of numbers
    # scores (if you don't need to relate the score to a name or other object)
    # prices of a specific object sold by different companies

# What is one way, using Ruby, to retrieve the 6th element in an Array? How about the 8th element? What happens if you try to retrieve the value of the _9999th_ element (or some element that doesn't exist in the array)?

    #You can use element indexes to retrive a given element of an array
    # example: if x was the given array, to retrive the 6th element of x you would 
    # do x[5], to retrieve the 8th element of x you would do x[7].
    #If you try to retrieve an element that doesn't exist from an array then a
    #blank space would be returned, it would not produce an error.
    

# The previous question asks about finding, for example, the 6th element in an Array. Is it possible to find the **-6th** (Notice the negative symbol!) element in an Array? What does that even mean?

    # Yes it is possible to find the -6th element of an array. Using the same
    # method as above, x[-6] would return the 6th to last element of a given array.
    # It is reading from the last element of an array to the first, instead of the
    # other way around.

# How would you perform an operation on every element inside an Array?

    # One way to perform an operation on every element inside an Array would be to
    # use the map method. This will create a new array. It you want it to replace
    # the elements instead of making a new array use map! method.
    
    #example: x = [1,2,3]
              x.map! { |x| x*2}
              print x  #=> [2,4,6]

# How do you add elements to an Array?

    # One way is to "add" arrays: x = ['dog', 'cat'] 
    #                             x += ['mouse']  #=>  ['dog', 'cat', 'mouse']
    #Another way to add elements to an Array would be to use the push method. You can
    #add multiple elements at the same time and it modifies the original array so 
    #you don't have to remember to reassign the array. 
    #        array = ['dog', 'cat']
    #        array.push('mouse', 'fox')

# Given the Array `["Laura", "Fiona", "Tori"]`, how would you replace `"Fiona"` with `"Florence"` so that you end up with `["Laura", "Florence", "Tori"]`?

    # Arrays are ordered, so you can use thier indexes to change objects in an array
    # x = ["Laura", "Fiona", "Tori"]
    # x[1] = 'Florence'

# What do the methods `push`, `pop`, `shift`, and `unshift` do?

    # pop: removes the last element of the array, and returns (or outputs) it if you choose to print it
    # push: adds an element to the end of the array
    # shift: removes the first element of the array, and returns it, or outputs it if you choose to print it
    # unshift: adds an element to the beginning of an array 
    
# How do you determine how many elements are in an Array?

    #The length method will return the number of elements in an array

# How would you reverse the order of elements in an Array?
    
    # The reverse method will create a new array with the elements of a given array in reverse order.
    # There is also the reverse! method which will reverse the order of elements in an array,
    # without creating a new array.

# How would you convert a String `"Sumeet Jain"` into an Array `["Sumeet", "Jain"]`? How about to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`? How would you convert the Array back into a String?
    # You can use the split method to convert the string into either given arrays
    # "Sumeet Jain".split(" ")  #=> ["Sumeet", "Jain"]
    # "Sumeet Jain".split("")   #=> ["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]
    
    # To convert both arrays back into the orriginal string you would use the join
    # method. 
    # ["Sumeet", "Jain"].join("")
    # ["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"].join("")