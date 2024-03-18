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