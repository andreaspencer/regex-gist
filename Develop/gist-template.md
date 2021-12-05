# Regex Challenge 17

The purpose of this gist is to explain what a regular expression is and how to use them. Regular expression (regex) can be used to match a certain character combination to a string. This is great for pulling specific character combination from a body of code as well as being used for validation. 

## Summary

The regex I will be walking you through is used to match emails. The regex code is: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/. One use for this code is to validate emails and making sure that an email follows the correct format.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors
The anchor is what starts and ends the regular expression. For the matching email code the anchors are the ^ and the $. This code is specifically saying that we are looking for a match that begins with 
^([a-z0-9_\.-]+) 
and ends with 
.([a-z\.]{2,6})$. 
I will explain what everything in the parathensis means throughout the tutorial. 
### Quantifiers
Quanitifiers are used to determine how many times a specific charcater or group of characters need to be present in order to have a match. For the matching email regex ^([a-z0-9_\.-]+) you can see a quanitifier is the + at the end of the square brackets. This means it must contain at least one of the following in order to match: any lowercase letter a-z, any number 0-9, an underscore, period, or dash.
### OR Operator
This operator is a simple | this is just put in a regex to say it can be one or the other. The email matching regex does not have this operator.
### Character Classes
A character class for the matching email is the /d after the @ in our expression. For our explain this charcater class is saying after the @ the charcater must be a letter not a digit (/d) or special charcater. There are several other charcater classes for example /s for a space. 
### Flags
Flags are put into place to affect the search, flags are optional in a regex. Flags flag a certain part of the regex. An example of this is an i that makes the regex case sensitive. The matching email regex does not have a flag.
### Grouping and Capturing
The first group to appear in the matching email code is ([a-z0-9_\.-]+). This first group must be true to move on to the next part of the regex which is ([\da-z\.-]+). The third and final group in the matching email regex is ([a-z\.]{2,6}). When looking for an email match each grouping must be true before the regex can move on to the next.

Capturing is what is being captured in each paranthesis grouping. Whatever is inside these paranthesis will be captured by the regex for example the first part of our regex must have a lowercase letter a-z, a digit 0-9, an underscore, period, or a dash. The plus sign tells the entire first grouping that it must have at least one of these.
### Bracket Expressions
Wihtin the parathensis are brackets that hold the parameters for the match. 
[a-z0-9_\.-]
For the first portion of the regex it is setting the match up to have a lowercase letter a-z, a digit 0-9, an underscore, period, or a dash. The plus sign after the brackets add to this to say it must have one.
[\da-z\.-]
For this second portion of the regex it is setting the match up to not start with a digit but have a lowercase letter a-z, period, and a dash. The plus sign after the brackets add to this to say it must have one.
[a-z\.]
The third portion of the regex is setting the match up to have a lowercase letter a-z and a period. The curly brackets {2,6} at the ending portion of our match tell the match it must have between 2-6 characters within that third portion of the regex. 
### Greedy and Lazy Match
Greedy matches will consume as much as possible repeating as many times as it can. Lazy matches or adding a ? after a bracketed expression tells the code to search as few times as possible. The matching email code does not use these matching devices.
### Boundaries
Boundaries make assertions about what can be matched to the right and left of the current position. The matching email code does not use a boundary an example of this is /G that tells the regex to look at the position immediately following the last match.
### Back-references
Back-reference is used to reference a group that was previously used in the regex. The matching email does not use this but for an example /1 would repeat the first group of the regex instead of rewriting it.
### Look-ahead and Look-behind
These are used to look for specific characters that are either followed by or before a specific character or sequence of characters to find a match. An example of this is to look for an $ followed by a number to match all prices on a page. The code for email matching does not use a look-ahead or a look-behind.
## Author

I am Andrea, I am currently enrolled in a coding bootcamp through UCLA extensions. I am getting certified in full stack web develop and hoped this helped you understand how regex are broken down to make your life easier while matching and validating your code.
Github: https://github.com/andreaspencer
