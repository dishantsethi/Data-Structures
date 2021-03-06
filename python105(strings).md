# Strings in Python

Strings are immutable. Once a string is defined, it cannot be changed
>
    a = 'Dishant'
    a[2] = 'E' // Gives error
But,
>
    a = 'Dishant'
    print(a)  // Dishant
    a = a + 'Sethi'
    print(a) // DishantSethi    

In the second program, interpreter makes a copy of the original string and modifies it. So the expression a = a +’for’ doesn't change string but reassigns the variable **a** to the new string generated by the result and drops down the previous string.

## Slicing of String

we can obtain the required character of a string using syntax, **string_name[index_position]**
>
    a = 'Dishant'
    print(a[2]) // s  (because the count starts from 0, character at 2nd index is 's')

- To extract substring from the whole string then we use the syntax like

  ```string_name[beginning:end:step]```  

  - beginning represents the starting index of string
  - end denotes the end index of string which is not inclusive 
  - steps denotes the distance between the two words. (steps are optional)

  >
        a = 'Dishant'
        print(a[2:7]) // shant

## Strings in-built functions
- **find("string",big,end)**: This function is used to find the position of the substring within a string.
  - returns "-1 " if string is not found in given range.
  - returns first occurrence of string if found.

- **rfind("string",beg,end)**: This function has the similar working as find(), but it returns the position of the last occurrence of string.
    >
        str = "geeksforgeeks is for geeks"
        str1 = "geeks"
        print(str.find(str1,0))  // 0
        print(str.find(str1,4))  // 8
        print(str.find(str1,10)) // 21
        print(str.rfind(str1,0)) // 21
        print(str.rfind(str1,4)) // 21
- **startswith("string",beg,end)**: The purpose of this function is to return true if the function begins with mentioned string else return false.
- **endswith("string",beg,end)**: The purpose of this function is to return true if the function ends with mentioned string else return false.
    >
        str = "geeksforgeeks is for geeks"
        str1 = "geeks"
        print(str.startswith(str1)) // True
        print(str.startswith(str1,4)) // False
        print(str.endswith(str1)) // True
        print(str.endswith(str1,4)) // True

- **islower()**: This function returns true if all the letters in the string are lower cased, otherwise false.
- **isupper()**: This function returns true if all the letters in the string are upper cased, otherwise false.
    >
        str = "Dishant"
        str1 = "sethi"
        print(str.islower()) // False
        print(str1.islower()) // True
        print(str.isupper()) // False
        print(str1.isupper()) // False
- **lower()**: This function returns the new string with all the letters converted into its lower case.
- **upper()**: This function returns the new string with all the letters converted into its upper case.
    >
        str = "Dishant"
        str1 = str.lower()
        print(str1) // dishant 
        str1 = str.upper()
        print(str1) // DISHANT   
- **swapcase()**: This function is used to swap the cases of string i.e upper case is converted to lower case and vice versa.
- **title()**: This function converts the string to its title case i.e the first letter of every word of string is upper cased and else all are lower cased.
    >
        str = "Dishant sethi"
        str1 = str.swapcase()
        print(str1) // dISHANT SETHI
        str1 = str.title() // Dishant Sethi
- **len("string")**: This function returns the length of the string
- **count("string",beg,end)**: This function counts the occurrence of mentioned substring in whole string.
    >
        str = "geeksforgeeks is for geeks"
        print(len(str)) // 26
        print(str.count("geeks")) // 3
        print(str.count("Geeks")) // 0
        
- **center(length,"string/charcater")**: This function is used to surround the string with a character repeated both sides of string multiple times. Takes 2 arguments, length of string and the character.
- **ljust(length,"string/charcater")**: This function returns the original string shifted to left that has a character at its right. It also takes two arguments, length of string and the character.
- **rjust(length,"string/charcater")**: This function returns the original string shifted to right that has a character at its left.
    >
        str = "dishant"
        print(str.center(15,'-')) // ----dishant----
        print(str.ljust(15,'-')) // dishant--------
        print(str.rjust(15,'-')) // --------dishant
- **isaplha()**: This function returns true when all the characters in the string are alphabets else returns false.
- **isalnum()**: This function returns true when all the characters in the string are combination of numbers and/or alphabets else returns false.
- **isspace()**: This function returns true when all the characters in the string are spaces else returns false.
    >
        str = "Dishant123"
        print(str.isalpha()) // False
        print(str.isalnum()) // True
        print(str.isspace()) // False

- **join()**: This function is used to join a sequence of strings mentioned in its arguments with the string.
    >
        str = "_"
        str1 = ("Dishant","Sethi")
        print(str.join(str1)) // Dishant_Sethi
- **strip("str/character")**: This method is used to delete all the leading and trailing characters mentioned in its argument.
- **lstrip("str/character")**: This method is used to delete all the leading characters(left side) mentioned in its argument.
- **rstrip("str/character")**: This method is used to delete all the trailing characters(right side) mentioned in its argument.
    >
        str = "----Dishant----"
        print(str.strip('-'))  // Dishant
        print(str.lstrip('-')) // Dishant----
        print(str.rstrip('-')) // ----Dishant

- **min("string)**: This function returns the minimum value alphabet from string.
- **max("string")**: This function returns the maximum value alphabet from string.
    >
        str = "Dishant"
        print(min(str)) // D
        print(max(str)) // t
    Note: A-Z have smaller ASCII numerical value than a-z. Therefore, 'D' will be smaller than 'a'    
- **replace(string to replace, new string which will replace, num of replacements default is unlimited)**: This function is used to replace the substring with a new substring in the string.
    >
        str = "geeksforgeeks if for geeks"
        str1 = "geeks"
        str2 = "nerds"
        print(str.replace(str1,str2,2))
        // nerdsfornerds if for geeks

### Convert String to a List

The split() method is used to split the strings and store them in the list.
>
    str = "Dishant Sethi"
    li = list(str.split(" "))
    print(li) // ['Dishant','Sethi']

### Regular Expressions

