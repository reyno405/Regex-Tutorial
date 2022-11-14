# Regex-Tutorial

In this tutorial I will be discussing Regex. Regex is a set of characters that together make a pattern. They can by used inside of code or algorithms to locate, or even locate and replace if that's what you desire, specific patterns inside of a string. An example of this would be to validate a user's password, identify phone numbers, email addresses, URLs, and so much more.

## Summary

\b[a-z0-9#$_-]+@[a-z0-9]+\.[a-z]{2,3}\b/gi.

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

### ⚓ Anchors

The Regex begins with \b, this is called an anchor and it's job is to define a "word boundary". By using this at the beginning/end we are forcing what's called a "whole word" search. So for example, if the Regex was \b867530\b, then only 867530 would match up but not 8675309.

Some other anchors are ^ and $:

^XXXXX will match any string that starts with ^XXXXX

XXXXX$ will match any string that ends with XXXXX$

Anchors do not match any characters, but instead they match specific positions. As you just saw ^ matches the starting position right before the 1st character of the search string. On the other hand $ matches the end of the last character, and of course \b defines the entire boundary for the search string itself.

### Quantifiers

### OR Operator

### Character Classes

Character classes in regex matches a character from a specific set. There are numbers of characters thatare predefined, also characters can be defined as your own set.

- [ABC] These characters inside the brackets will match any character in the set.
- [^abc] When adding a caret it will match any character that is not in the set.
- [A-z] When adding a dash inbetween two characters will select a range between the two.
- [\s\S] This is used in regex for character sets that can be used to match any character, including line breaks, without the dotall flag. 
- . Is like a wildcard that will not accept any input. This character will expect a linebreak that will match.
- \w Will match any character either alphanumeric & underscore. It will not match any o accented or non-roman characters.
- \d Matches any digit character (0-9)
- \p Matches a character in the specified unicode category.

### Flags

### Grouping and Capturing

Grouping expressions allows us to keep things more organized and easier to exact the characters of a given group. This is used with parentheses "()".

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
