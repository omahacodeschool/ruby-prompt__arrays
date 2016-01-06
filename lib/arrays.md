---
title: Arrays
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is an Array?

An ordered list of objects. List objects can be integers, strings, floats, hashes, symbols, and other arrays.
Each object in the array has an associated index with the first object's index being 0.

# What are some examples of information that would be Arrays as opposed to some other data type?

A list a cat's favorite things. All 12 months. The alphabet. Dinosaur types. Prime numbers. 

# What is one way, using Ruby, to retrieve the 6th element in an Array? How about the 8th element? What happens if you try to retrieve the value of the _9999th_ element (or some element that doesn't exist in the array)?
Same concept as in strings. the first element in an array is in the 0 position, second is in the 1 position and so on.

    prime = [2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31, 37, 41, 43, 47]
    prime[6]
     will return 17
    prime[8]
     will return 23
    prime[99]
     will return 'nil' because it does not exist


# The previous question asks about finding, for example, the 6th element in an Array. Is it possible to find the **-6th** (Notice the negative symbol!) element in an Array? What does that even mean?

Same concept as in strings. Last element in array will be in the -1 position, second to last will be in the -2 position, and so on.

    prime[-6]
     will return 29
    
# How would you perform an operation on every element inside an Array?

    prime.each do |x|
     puts x+=1
    end
    
This would add 1 to each element in the array

# How do you add elements to an Array?

You can insert something in a specific location:

    prime.insert(-1, 53)
     inserts 53 in the -1 position of the array
    prime << 53
     puts 53 at the last positon of the array
    prime.push(53).push(59)
     pushes the new elements to the end of the array. Able to chain multiple pushes together

# Given the Array `["Laura", "Fiona", "Tori"]`, how would you replace `"Fiona"` with `"Florence"` so that you end up with `["Laura", "Florence", "Tori"]`?
The .map method creates a new array based on the original array, but changes the elements based on your block.

    arr = ["Laura", "Fiona", "Tori"]
    arr.map! { |element|
       if(element == "Fiona")
           "Florence"
       else
           element
       end
    }

    => ["Laura", "Florence", "Tori"]

# What do the methods `push`, `pop`, `shift`, and `unshift` do?

Push adds one or more new elements to the end of an array.
Pop removes the last element of an array and returns it.
Shift removes the first element of an array and returns it.
Unshift will add a new item to the beginning of an array.

# How do you determine how many elements are in an Array?

Use the count operation:

    prime.count
        => 17

# How would you reverse the order of elements in an Array?

    arr = ["Laura", "Florence", "Tori"]
    arr.reverse_each { |x| puts x }

# How would you convert a String `"Sumeet Jain"` into an Array `["Sumeet", "Jain"]`? How about to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`? How would you convert the Array back into a String?

    "Sumeet Jain".split
        => ["Sumeet", "Jain"]
        
    "Sumeet Jain".split(//)
        => `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]
        
    ["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"].join("")
        =>s "Sumeet Jain"