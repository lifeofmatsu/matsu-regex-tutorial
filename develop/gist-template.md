# Regex Tutorial: Demystifying Email Address Validation
#### by Jus Ferrell

In this tutorial guide, we expand on the topic of regular expressions (regex), focusing on a regex pattern used for email address validation. Grasping the email address validation regex will not only help you create signup, login, and other forms that require email with ease and confidence, but also further your knowledge of how regex is used to parse and match complex patterns when manipulating strings.

## Summary

By the end of this tutorial, you will understand the regex pattern `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`, most commonly known for its use in email address validation. Together, we will break down, and piece together again each component of the regex pattern to better understand how it ensures each user's entry follows standard email format.

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
Anchors are regex signifiers denoting the beginning and end of a line. They are, in fact, special characters that match position within the string rather than content. In email validation regex, the `^` anchor designates the start of a line, whereas the `$` designates the end. Effectively, these two anchors ensure that the match begins at the start of the string, and ends with the pattern we define, preventing any extra characters before or after the email address.

Example:
- `^[a-z]`: Matches a string that starts with a lowercase letter.
- `[a-z]$`: Matches a string that ends with a lowercase letter.


### Quantifiers
Quantifiers describe the number of instances an individual or group of characters must appear in the string for a successful match. For example, in the regex `[a-z0-9_\.-]+`, the `+` quantifier means "one or more of the preceding element", indicating that one or more of the characters in `[a-z0-9_\.-]` MUST be present before the `@` symbol of the email.

Example:
- `a+`: Matches one or more consecutive 'a' characters.


### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)