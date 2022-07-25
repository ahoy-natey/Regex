# Regex

Regex, short for 'Regular Expression', is a series of characters and symbols that make up a pattern. This pattern can be recognized by algoritms to determine their function. As an example, email@email.com can be recognized as an email address due to a couple of characteristics. We can use Regex to search and replace as well. We can find a certain word, or phrase in a string. Using various tools such as flags and quantifiers, we can narrow or broaden our search. This README will break down regular expressions and discuss each component of an expression. 

## Summary

Lets take a look at this string.

"I went to the store. But I only had 3 dollars! This would not let me buy much. I should have had three more. I could go home and get more, but I didn't want to. The sky is gray now, and when it is grey it will probably rain."

Depending on what we are trying to filter for, we can write a regular expression to sort the information that we are trying to obtain. 



## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components
A regex expression follows some basic principles. It begins with a forward slash / and end with a forward slash /. At the end of the second /, a flag is planted. We get to flags and specifics later. Within the two //, we can put our specific criteria that will allow us to target the desired piece of information. 
### Anchors

### Quantifiers

### Grouping Constructs
Grouping can be done by using square brackets []. Lets say I wanted to find a word that ended with 'ould'. This could represent Could, Should, Would. Lets say I only wanted to return 'could' and 'would', but reject 'should'. We would write /[cw]ould/g.  If I wanted to return capital letters, I would write [CW]. We will get to flags later that will help us with case sensitivity.
Grouping can also utilize '-' to find a range of characters. Lets say I wanted to return a value between 1 and 10. This would be written as [1-10]. Grouping allows us to not only be very specific in what we are returning, but also allows us to sort through a huge range of possiblities.
Grouping can also be done by using parenthesis (). This grouping is called a capture group. It works similarly to using square brackets, but is much more explicit. If we tried a range using (1-10), we would not get a range, but instead, return '1-10'. We will get to OR operators, but while [] can be used to capture a range, () must include an | to return mulitple possiblities, eg (1|2|3|4|5|6|7|8|9|10).



### Bracket Expressions
/\w{4,5}/g will bring any word between four to five
[]
### Character Classes
As mentioned earlier, grouping with [] allows us to utilize certain functions. What is placed inside of the brackets is known as the character class, or set. If we take our expression, we want to find all occurances of the color gray. However, gray can be spelled two different ways. We will use this character class [ae] inside of gr[ae]y to increase accuracy. 
Character classes can also be used to match things that are not desired. Lets say we only wanted to find the 'gray', we would filter by using a carrot ^ symbol. Our regex would look like gr[^e]y, and would return only gray.
Character classes also extend to integers and values. \d will allow us to target any digits. If I wanted to grab the '3' from our above sentance, I would simply write /\d/. If I wanted to target 'three', I could use \w to target a specific word.
Dot . is another class, this matches any character but ignores line brakes. There are many classes that can all be used to meet a certain goal. 
### The OR Operator
|
### Flags
Flags are placed at the end of the expression after the last forward slash /. Flags allow us to place certain rules on the expression. For example 
### Character Escapes
\. backslash

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
