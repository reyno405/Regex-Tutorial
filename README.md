# Regex-Tutorial

In this tutorial I will be discussing Regex. Regex is a set of characters that together make a pattern. They can by used inside of code or algorithms to locate, or even locate and replace if that's what you desire, specific patterns inside of a string. An example of this would be to validate a user's password, identify phone numbers, email addresses, URLs, and so much more.

## Summary

Today I will be covering and breaking down the components of a regular expression used to match Hex Values. Hex values are commonly used for color using the hexadecimal color code format. In the web we can use hex triplet (hex color code) to represent colors on a web page.

- \b[a-z0-9#$_-]+@[a-z0-9]+\.[a-z]{2,3}\b/gi.

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

Regular expressions can contain multiple components that help mold any search pattern you're working on.

Some of the more common components include: Character Classes, Groups, Quantifiers, Anchors, Lookarounds, etc

When used together the regular expression can become complicated, but also specific. You can find basically any string combination using certain components. Let's take a look, starting with Anchors.

### ⚓ Anchors

The Regex begins with \b, this is called an anchor and it's job is to define a "word boundary". By using this at the beginning/end we are forcing what's called a "whole word" search. So for example, if the Regex was \b867530\b, then only 867530 would match up but not 8675309.

Some other anchors are ^ and $:

- ^XXXXX will match any string that starts with ^XXXXX

- XXXXX$ will match any string that ends with XXXXX$

Anchors do not match any characters, but instead they match specific positions. As you just saw ^ matches the starting position right before the 1st character of the search string. On the other hand $ matches the end of the last character, and of course \b defines the entire boundary for the search string itself.

### Quantifiers

Quantifiers determine how many instances of a character, group, or character class must be present for a match to be found.

- + Could be any amount, but there has to be at least one.
- {2} we use these brackets to indicate a specific number, in this case 2.
- {2,} put a comma after and it becomes 2 or more.
- {2,6} now these have a range of 2-6.

### OR Operator

The "or" operator within a regular expression is defined using the | element. The or operator indicates that it could either of the components that we are separating with the |. For our hex value regular expression we have ([a-f0-9]{6}|[a-f0-9]{3}). Note the or operator separating these 2 components. This means that our hex value could either be 6 characters [a-f0-9]{6} or 3 characters [a-f0-9]{3}.

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

### 🏴  Flags

Flags are also called modifiers because they modify the output of a regular expression. These flags can be used in any order or combination, and are an integral part of the RegExp.

- i Case insensitive: Match will be case-insensitive.
- g Global Search: Match all instances, not just the first.
- m Multiline: Anchor meta characters work on each line.

### Grouping and Capturing

Grouping expressions allows us to keep things more organized and easier to exact the characters of a given group. This is used with parentheses "()".

### Bracket Expressions

- In regex we use [] to define define the character class. Any characters placed inside them will produce a match to the Regex pattern, unless the character(^) precedes the characters in the class. In the Regex example above [a-z] defines any character class that is within the alphabet.

### Greedy and Lazy Match

By default, a regex will perform a greedy match, which means the match will be as long as possible. We can use ? to match in a lazy way, which means the match should be as short as possible.

- "/(.*at)/" => The fat cat sat on the mat. 
- "/(.*?at)/" => THE FAT cat sat on the mat. 

### Boundaries

Matches on a word boundary, meaning one side is a word character (like \w) and the other side is not a word character (like a space character).

There are three separate positions to qualify as a word boundary:

- Before the initial character in the string, if the first character is a word character

- After the last character in a string, if the last character is a word character

- Between two characters within the string, where one is a word character while the other is not a word character

### Back-references

Backreferences match the same text as previously matched by a capturing group. Suppose you want to match a pair of opening and closing HTML tags, and the text in between. By putting the opening tag into a backreference, we can reuse the name of the tag for the closing tag. 

### Look-ahead and Look-behind

Lookaheads and lookbehinds forces the main expressions to be what you have defined it as. Without it being exactly what it is it will not be accepted as a valid input.

- (?=ABC) is a postive lookahead and it matches a group after the main expression without including it in the result.

- (?!ABC) is a negitive lookahead and it specifies a group that can not match after the main expression (if it matches, the result is discarded)

- (?<=ABC>) is a postive lookbehind and matches a group before the main expression without including it in the result.

- (?<!ABC) is a negitive lookbehind and Specifies a group that can not match before the main expression (if it matches, the result is discarded).

## Author

Kevin Reynolds

Kevin Renolds is a coding student at Michigan State Univerysity completing a certification in full-stack development.

GitHub: https://github.com/reyno405
