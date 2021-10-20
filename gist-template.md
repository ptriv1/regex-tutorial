# Regex Tutorial: Matching an Email

Many websites require using an email and password to log in.  Since website owners need to confirm the email is real, programmers can add code to verify email addresses entered are in a certain format.  A relatively simple way to do this in JavaScript is to use a regular expression.

## Summary

In this gist I will describe a regular expression that allows verification of an email entered as a string.  The name of the regex is Matching an Email, and my regex is `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`.  

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

Regular expressions use forward slashes (/) to enclose the expression. Since a regex is a literal, a regular expression needs to use these forward slashes.  

The regular expression covered in this tutorial is `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`.

### Anchors
Anchor characters are used in regular expressions.  In this regex, the anchors are ^ and $.  In regular expressions, ^ is the character that begins the string in the expression, and $ is the character that ends the string in the expression.  In the Matching an Email regex, everything between the ^ and $ is included in the email string that is entered.  

### Quantifiers
A quantifier limits a string or a section of a string.  Brackets like {} enclose the quantifiers.  In the Matching an Email regex, since 2,6 is between the {} brackets, the domain of the email needs to be between 2 and 6 characters.


### Grouping Constructs
Regular expressions use parentheses to create subexpressions, or sections of strings.  In the Matching an Email regex, parentheses are used so that the characters entered before the @ are considered a section, the characters entered after the @ are considered a section, and the characters entered after the . are considered a section.  These sections relate to the common email format name@organization.domain.

### Bracket Expressions
Regular expressions often use bracket expressions to indicate ranges of characters that we want to search.  In the Matching an Email regular expression, the name section of the email can include the alphabet, numeric characters, and special characters ., -, and _.  In the section of the email before the domain, we can validate alphabet characters.  The domain section of the email string allows us to validate alphabet characters, numeric characters, and the . character.

### Character Classes
The Matching an Email regular expression allows using \d to match numbers using the 0-9 digits.

### Character Escapes
In the Matching an Email regular expression, the '\.' is an escape character that matches all characters except \n.

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
