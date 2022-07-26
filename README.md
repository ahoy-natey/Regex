# Regex

Regex, short for 'Regular Expression', is a series of characters and symbols that make up a pattern. This pattern can be recognized by algoritms to determine their function. As an example, email@email.com can be recognized as an email address due to a couple of characteristics. We can use Regex to search and replace as well. We can find a certain word, or phrase in a string. Using various tools such as flags and quantifiers, we can narrow or broaden our search. This README will break down regular expressions and discuss each component of an expression. 

## Summary

Lets take a look at this expression:

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

This expression is used for matching a Hex Value. As you can see, there is a hashtag at the beginning of the character set. There is a range of numbers and characters, limited to 6 or 3



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
A regex expression follows some basic principles. It begins with a forward slash / and end with a forward slash /. At the end of the second /, a flag is planted. There aren't any flags here, but we could add a 'g' (global) at the end here. We will get to flags and the specifics later. Within the two //, we can put our specific criteria that will allow us to target the desired piece of information. 

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`
### Anchors
Certain characters, called anchors, affect the targeting of the query. ^ targets the beginning of the targeted string, and $ targets the end. 

### Quantifiers
Plus
Star
quantifier {1,3}
?
alternation |
### Grouping Constructs
Our grouping is done using a 'capture group', which is done with parathesis (). Inside this group, we are looking for the specific returns that will make up our hex code ([a-f0-9]{6}|[a-f0-9]{3}). Within these () are multiple character classes and expressions, which we will get to soon.


### Bracket Expressions
Within the capture group, there are square brackets being used as well []. These brackets allow us to create groups, but groups that are searchable through a range. Remember, '-' is used to return a range of something. As you can see, we are searching for a-f, and 0-9 values. What would improve this bracket is adding A-F as well, in order to capture uppercase as well. This could also be done by adding a flag that dealt with any kind of case senstivities.
{Talk about this curly brackets}

### Character Classes
As mentioned earlier, grouping with [] allows us to utilize certain functions. What is placed inside of the brackets is known as the 'character class', or set.
Character classes can also be used to match things that are not desired. To do this, we would filter by using a carrot ^ symbol. Lets say you felt very strongly about the spelling of gray vs grey. Our regex would look like gr[^e]y, and would return only gray.
Character classes also extend to integers and values. \d will allow us to target any digits. If I wanted to grab only digits from our hex values, I would simply write /\d/. If I wanted to target characters, I could use \w to target a specific word.

### The OR Operator
| key is used as an OR operator. In this instance, we 
### Flags
Flags are placed at the end of the expression after the last forward slash /. Flags allow us to place certain rules on the expression. For example 
### Character Escapes
\. backslash

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
