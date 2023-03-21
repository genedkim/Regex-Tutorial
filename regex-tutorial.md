# Regex Tutorial - Matching Email

Regular expressions are combinations of characters used to define the rules for matching a pattern. Some uses for regex include find and replace functions, matching patterns in strings, and input validation. The regex that will be discussed today is used to match email addresses. Most applications that require user registration use email address for verification. When building such applications, in order to make sure any given value is in the format of a valid email address, regular expressions can be used to match the given value to a pattern.

## Summary

In this tutorial, I will discuss the following regular expression used to match email addresses:

```md
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

This regular expression is used to verify that a given email address is in the correct format. This tutorial will break down this regular expression into its individual components and explain what each does.

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

### Anchors
Anchors are characters in the regex that will match the position of the string. In the case of our regex:
```md
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```
The anchor tags will be `^` which is used to match the beginning of a string, and `$` used to match the end of the string.

### Quantifiers
Quantifiers are characters in the regex that take the token preceding it and defines how many times that token should be matched.
In our regex the quantifiers used are `+` and `{2,6}`.

`+` is used to match one or more of the preceding token. It is used twice in our regex; once to make sure there's at least one character matching `[a-z0-9_\.-]` and again to make sure the same for the following `[\da-z\.-]`

`{x,y}` is used to match a range between x and y number of characters to the preceding token. So in our regex `{2,6}` is used to make sure the input consists of between 2-6 characters matching `[a-z\.]`

### Grouping Constructs
Grouping constructs are used to group parts of a regular expression together. In our regex we use `()` to group the username `([a-z0-9_\.-]+)` and two different parts of the domain name `([\da-z\.-]+)` `([a-z\.]{2,6})` together.

### Bracket Expressions
Bracket expressions are used to match the characters from a given string to the values given defined within a set of brackets `[]`. In our regex the following bracket expressions are used:

`[a-z0-9_\.-]` is used to make sure each character in the email username is a letter between a-z, digit between 0-9, underscore, period, or hyphen.

`[\da-z\.-]` is used to make sure each character in the domain name is a digit, letter, period, or hyphen.

`[a-z\.]` is used to make sure each character in the domain extension is either a letter or period.

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
