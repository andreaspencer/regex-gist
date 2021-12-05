# Regex Challenge 17

The purpose of this gist is to explain what a regular expression is and how to use them. Regular expression (regex) can be used to match a certain character combination to a string. This is great for pulling specific character combinations from a body of code as well as validating code.

## Summary
The regex I will be walking you through is used to match emails. The regex code is: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`. One use for this code is to validate emails and make sure that an email follows the correct format.

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
The anchor is what starts and ends the regular expression. For the matching email code the acnchors are the `^` and the `$`. This code is specifically saying that it is looking for a match that begins with: 

`^([a-z0-9_\.-]+)`

and ends with:

`.([a-z\.]{2,6})$.`

I will further explain everything within the paranthesis throughout the tutorial.
### Quantifiers 
Quantifiers are used to determine how many times a specific charcater or group of characters need to be present in order to have a match. For the matching email regex `^([a-z0-9_\.-]+)` you can see a quantifier is the `+` at the end of the square brackets. This quantifier means that the match must contain at least one of the following: any lowercase a-z, any number 0-9, an underscore, a period, or a dash.
### OR Operator 
The or operator is a simple `|` this is just used to say it must be one or the other. The email matching regex does not have an or operator.
### Charcater Classes
A charcteer class for matching email is the `/d` after the @ in the expression. For the example this character class is saying after the @ the following character must not be a digit but a letter a-z. There are several other character classes for example `/s` is used for a space.
### Flags
Flags are put into place to affect the search. Flags are optional and are used to flag certain parts of the regex. An example of this is an `i` that makes the regex case sensitive. The matching email regex does not have a flag.
### Grouping and Capturing
The first group to appear in the matching email regex is `([a-z0-9_\.-]+)`. The second group is `([\da-z\.-]+)`. The third group is `([a-z\.]{2,6})`. When looking for an email matching each grouping must pass before the the regex can move to the next group in the regex.

Capturing is what is being captured in the paranthesis. Whatever is inside these paranthesis will be cpatured by the regex for example the first part of tour regex must have a lowercase letter a-z, a digit 0-9, an underscore, a period, or a dash. The plus sign adds an at least one statement to this group.
### Bracketing
Within the paranthesis are brackets that hold the parameters for the match.

`[a-z0-9_\.-]`

For the first brackets the regex is looking for a match that has a lowercase letter a-z, a digit 0-9, an underscore, a period, or a dash.

`[\da-z\.-]`

For the second portion of the regex it is setting the match up to look for it to not start with a digit after the @ symbol but instead have a letter a-z, a period, or dash in it.

`[a-z\.]`

For the final brackets the regex is set up to have a lowercase a-z and a period. The curly brackets that follow these last brackets set up the character length `{2, 6}` of between 2 and 6 charcaters for the final portion of the regex.
### Greedy and Lazy Match
Greedy matches will ocnsume as much as possible, repeating as many times as it can while lazy matches or adding a `?` after a bracketed expression tells the code to search as few times as possible. The matching email regex does not use these macthing devices.
### Boundaries
Boundaries make assertions about what can be matched to the right and left of the current position. An example of this is `/G` that tells the regex to look at the position immediately following the last match. The email matching regex does not use a boundary.
### Back-references
Back-reference is used to reference a group that was previously used in a regex. An example of this is to add a `/1` which would repeat the existing first group instead of rewriting it all. The email matching regex does not use a back-reference.
### Look-ahead and look-behind
These are used to look for specific charcaters that are either followed by or before a specific character or sequence of characters to find a match. An example of this is to look for an $ followed by a number to match all prices on a page. The regex for email matching does not use a look-ahead or a look-behind.
## Author

I am Andrea, I am currently enrolled in a coding bootcamp through UCLA extensions. I am getting certified in full stack web development. I hope this regex gist for an email matcher helped you understand how regex are broken down to make your life easier while matching and validating your code.

Github: https://github.com/andreaspencer
