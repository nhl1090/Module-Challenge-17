# Regex Tutorial - Matching Hex Values

Regular expression, also known as regex, is a web developing tool that can be used to validate data. This tutorial will specifically focus on hex values and the regex code that's used to validate them.

See [Regex-Tutorial gist here](https://gist.github.com/nhl1090/f6dd45562de0d90ce97385606e75d7f9).

## Summary

The regex used for matching hex values is: ^#?([a-f0-9]{6}|[a-f0-9]{3})$

This regex is designed to match a hex value, which is a shorter way of saying hexadecimal color value. A hex value is used in programming to define colors. The regex typically starts with the # symbol, followed by either a 6-digit (e.g., #ffffff) or 3-digit (e.g., #fff) hex value.

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

### Anchors

This regex uses **anchors** to specify the position of the search pattern relative to the input string.

- ^: dictates where the hex value should begin
- $: dictates where the hex value should end

### Quantifiers

In the hex regex, **quantifiers** specify how many times the preceding element has to appear for a match.

- {6}: exactly 6 characters are matched when capturing the full hex code (e.g., #ffffff).
- {3}: exactly 3 characters are matched when capturing the shorthand hex code (e.g., #fff).

### OR Operator

The **OR operator** is used to provide alternative patterns to match.

- |: allows either 6-digit or 3-digit hex values to match.

### Character Classes

**Character classes** match any character that is within the brackets, ensuring the characters in the hex value are valid.

- [a-f0-9]: allows any lowercase letter from a to f and any digit from 0 to 9


### Flags

The regex for hex values does not have any flags. These are typically used to midufy the behavior of the regex in different ways.

### Grouping and Capturing

In the hex value regex, **grouping and capturing** is used to group parts of the regex and capture matched sub-expressions. The parentheses around the pattern allow the regex to treat the two parts as one.

- ([a-f0-9]{6}|[a-f0-9]{3}): captures either a 6-character OR (there's that OR operator again) a 3-character hex value, depending on the input.

### Bracket Expressions

Much like the character class mentioned above, **bracket expressions** are used to define a set of characters that can match in the pattern. 

- [a-f0-9]: only hexadecimal digits are allowed


### Greedy and Lazy Match

**Greedy and Lazy Match** refers to how the regex processes the input. In this regex, no lazy quantifiers are used. Instead it defaults to a greedy match, where the engine _tries_ to match as many characters as possible.

### Boundaries

This regex doesn't use **boundaries** but the anchors mentioned above serve a similar purpose!

## Author

My name is Neil and I am grateful for your attention.

[nhl1090](https://github.com/nhl1090)