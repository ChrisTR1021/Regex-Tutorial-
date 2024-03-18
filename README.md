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

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
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