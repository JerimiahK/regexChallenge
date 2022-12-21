# Regex Tutorial

This tutorial is to explain what a Regular Expression, or regex for short is, and how the multiple components of regex's work. By the end of the tutorial, you will have a better understanding of what the components of a regex are, how the regex works, and why we use them.

## Summary

As mentioned above, a regex is short for Regular Expression, and is a sequence of characters that defines a specific search pattern. They are fequently used to validate inputs, and find certain patterns of characters within a string.
In this tutorial, we will be using a regex to match an email address. Below is an example of the regex.

Email: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

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

You may have looked at the above code and interpreted it as being some kind of alien language. At first glance, it absolutely looks that way, however if you know what you are looking for, and how it is broken down, understanding a regex is surprisingly simple and easy to do. Regex's are broken down into components that make it easier to understand, and below we will breakdown each component, and its purpose. First, we will start off noting that regex's are considered a literal, so they must be wrapped in the (/), which helps us check the beginning and ending slashes off of our list of unkowns.

### Anchors

The next thing you may notice, is the `(^)` caret symbol, which in tandem with the `($)` symbol at the end, are called "anchors". The caret symbol singnifies a string that begins with the characters that follow it, and the `($)` symbol signifies a string that ends with the cahra ters that precede it.

### Quantifiers

Next up we have Quantifiers, which set the limits of the string that your regex matches. Quantifiers typically include a the minimum and maximum number of characters that your regex is looking for. Quantifiers are represented in four different ways.
The first is the `(*)`, which matches the pattern zero or more times, meaning either none, or some of the characters have to match.
Second is `(+)`, which matches the pattern one or more times, meaning that a character has to match the pattern one or more times.
Third is the `(?)`, which specifically matches the pattern zero or one time.
Lastly we have the most custom option, which is the `{}` curly brackets. Curly brackets can provide three different ways to set limits for a match: `{n}` matches the pattern 'n' number of times, `{n, }` matches the patter AT LEAST 'n' amount of times, and finally `{n, x}` matches the pattern from a minimum 'n' to a maximum 'x' amount of times.

### Grouping Constructs

Grouping Constructs are intented to allow you to cehck multiple parts of a string to determine that different sections fulfill different requirements. This becomes very useful when the regex's start to grow into more complicated forms, and grouping constructs help break these sections up, making them easier to verify. They are broken by `()` and colons, for example `(abc):(123)`.

### Bracket Expressions

Bracket Expressions are represented by the `([])` square brackets, and contain the contain the values of the range of characters that we want to match. For example `[a-z]` would represent we want to look for all letters between a-z to match.

### Character Classes

In regex, a character class defines a set of characters, of which any of them can occur in an input string to fulfill the match. Some common character classes, and their uses are listed below.

`.` - Matches any character except the newline character (`\n`)

`\d` - Matches any Arabic numeral digit. This class is equivalent to the bracket expression `[0-9]`

`\w` - Matches any alphanumeric character from the basic Latin alphabet, including the underscore. This class is equivalent to the bracket expression `[A-Za-z0-9_]`

`\s` - Matches a single whitespace character, including tabs and line breaks.

### The OR Operator

The OR Operator is represented by `|`, similar to JavaScript. It is helpful when you don't need the expression to meet all of the requirements within the paranthesis. An example of an OR Operator is: `(abc):(xyx)` is the original expression and with the OR Operator becomes `(a|b|c):(x|y|z)`.

### Flags

When a regex is a literal, it must be wrapped in slash characters, however the one exception to that rule is when you use the Flags component. A Flag is placed at the end of a regex, after the second slash, and the Flag defines additional functionality or limits for the regex. Three common Flags you will most likely come across are:

`g` - Global search: the regex should be tested against all possible matches in a string.

`i` - Case-insensitive search: case should be ignored while attempting a match in a string.

`m` - Multi-line search: a multi-line input string should be treated as multiple lines.

### Character Escapes

Character Escapes play an important role in regex components. By utilizing the backslash `\`, the regex escapes a character that would otherwise be interpreted literally. For example, a `.` matches any character except the newline character, whereas `\.` represents a period, or dot. An important note is that all special characters, including the backslash, lose their special significance inside bracket expressions.

## Author

My name is Jerimiah Kripakov and I am a junior full stack developer located in Denver, Colorado. My developer journey began in October 2022, and has been short but full of success through hard work and putting in time out side of class. I am determined to become a very knowledgeable, and resourceful developer who thinks outside of the box and contributes new ideas, and refreshing, modern designs to the developer community.

GitHub Link: https://github.com/JerimiahK