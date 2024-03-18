# Regular Expression Email Tutorial 

A regular expression, commonly referred to as regex, is comprised of a series of characters instructed to recognize text patterns. These patterns extract constituted data like phone numbers, emails, and more from text based content. 

## Summary

In this tutorial, I'll delve into the regex necessary for matching an email address, which is /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/. This serves as a beneficial tool for validating email input across different implementations.

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

The anchor marks the beginning and end of the regular expression. In the provided email matching code,

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`
the anchors are identified by ^ at the beginning and $ at the end. Meaning the expression should start with 

^([a-z0-9_\.-]+)
The details of the parenthesis will be discussed later in the tutorial. Essentially, the anchor signals that any match must adhere to this criteria. Subsequently, it should conclude with


.([a-z\.]{2,6})$.

If a string doesn't meet the said criteria, its not a match. This ensures that the regex accurately captures the text pattern. 

## Quantifiers 

Quantifiers establish limits on the contents of a string, this enforces guidelines for the input.

In the context of the email regex:

/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/
Here's how the quantifiers operate:

+: This signals the string must contain  one or more character from the specified sequence. In this instance, it requires the user to select from either [a-z0-9_.-] or [\da-z.-] at least once.
{2,6}: These are called bracket quantifiers, setting a range for the number of times the user can select from the specified bracket [a-z\.]. It signals that the user's selection must include at least 2 characters and no more than 6.

## Grouping Constructs

In the email example, grouping is evident in ([\da-z\.-]+), where the character specifics are enclosed in brackets. This forms a group indicative of the string. Each group is stored in the program's memory. This identifies specific search parameters for particular components within the string. Grouping organizes and governs regex patterns efficiently, allowing for precise and targeted matching patterns

## Bracket Expressions

Bracket expressions are necessary in regular expressions, they specify the characters that can be matched. Enclosed within square brackets [ ], a bracket expression allows you to define characters and ranges of characters that you intend to match. [0-9] matches any digit from 0 to 9, while [a-z] will match any lowercase letter from 'a' to 'z'. These expressions provide flexibility and accuracy in defining the criteria for pattern matching.

## Character Classes

\d: This class represents any digit from 0 to 9. It's the shortcut for the range [0-9].

\b: The "word boundary" class is used to slot a position before or after a specific string in a word. 

\w: This class represents word characters, it includes uppercase and lowercase letters, digits, and the underscore character. It's  equivalent to the character set [a-zA-Z0-9_] and is used for matching alphanumeric characters and underscores.

## The OR Operator

^(0[1-9]|1[012])[-/.](0[1-9]|[12][0-9]|3[01])[-/.][0-9]{4}$
The first group, ^(0[1-9]|1[012]), demonstrates the use of the OR operator |. This allows for alternatives in regex pattern. In this specific case, it allows the user to select a month starting with either 0 or 1, followed by the specified sequence of numbers. This OR operator facilitates variation within the pattern, enabling flexibility in matching different variations of the input.

## Flags

i (insensitive casing): This flag allows the regex search to ignore character casing, enabling matches regardless of whether the characters are uppercase or lowercase.
g (global): This flag specifies that the regex search should find all occurrences of the pattern within the input string.
s (dot all): This flag enables the dot . character to match newline characters. Essentially treating any character as a valid match, including line breaks.
m (multiline): This flag changes the behavior of anchors such as ^ and $ to match the start and end of each line within a multi-line input string. 


## Character Escapes

In regular expressions, character escapes are used to interpret a special character as a literal character. For example, in the bracket expression [a-z0-9_\.-], the period . is treated as a literal rather than its given regex meaning. 

In [\da-z\.-] and [a-z\.], the period \. is used as an escape to match a period character. This ensures that the regex interprets the period as a dot character.

Character escapes are essential for specifying literal characters that would otherwise have special meanings in regular expressions, allowing for precise pattern matching in text.

## Author

My name is Chris, i hope this was informative and feel free to checkout my Github: [ChrisTR1021](https://github.com/ChrisTR1021/Regex-Tutorial-?tab=readme-ov-file#anchors)
