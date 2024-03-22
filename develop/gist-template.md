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

**Example:**
- `^[a-z]`: Matches a string that starts with a lowercase letter.
- `[a-z]$`: Matches a string that ends with a lowercase letter.


### Quantifiers
Quantifiers describe the number of instances an individual or group of characters must appear in the string for a successful match. For example, in the regex `[a-z0-9_\.-]+`, the `+` quantifier means "one or more of the preceding element", indicating that one or more of the characters in `[a-z0-9_\.-]` MUST be present before the `@` symbol of the email.

**Example:**
- `a+`: Matches one or more consecutive 'a' characters.


### OR Operator
_While the regex for this tutorial does not use the OR operator (`|`) explicitly, it is good to be aware of its use as it is seen often in other contexts._

The `|` operator facilitates alternation, giving the regex engine two or more match options/alternatives at a specific point in the regex. Colloquially, this is like saying "Match either the pattern on the left side of the `|` or the pattern on the right side." While our email regex does not use the OR operator, it's invaluable in situations where multiple patterns are considered valid.

**Example:**
- `cat|dog`: Matches either 'cat' or 'dog'.
- `(blue|green|red) car`: Matches 'blue car', 'green car', or 'red car'.

The `|` operator is notably advantageous within more complex regex patterns, significantly enhancing flexibility by accommodating multiple possible matches.


### Character Classes
Character classes enable matching for any one of several characters, defined within square `[]` brackets. For instance, `[a-z]` matches any lowercase letter. In the context of our email regex, `[a-z0-9_\.-]` matches any lowercase letter, digit, underscore, period, or dash, which are nigh-ubiquitous characters in the username segment of an email address.

**Example:**
- `[aeiou]`: Matches any one lowercase vowel.


### Flags
Flags modify the behavior of a regex by altering how the regex search is performed. Common flags include `g` for global search, `i` for case-insensitive matching, or `m` for multiline matching. Our tutorial email regex is not composed of flags, but they can be added as needed if you need to change its function.

**Example:**
- `/abc/i`: Matches the set 'abc' in a case-insensitive manner.


### Grouping and Capturing
Parentheses `()` are characters designated for grouping and capturing. They specify a regex segment to group together, letting us apply quantifiers to the group altogether. They  capture the content matched by that part of the regex for later use. In our example, the character group `([a-z0-9_\.-]+)` captures the username component of an email address.

**Example:**
- `(abc)+`: Matches one or more occurrences of the sequence 'abc'.


### Bracket Expressions
Bracket expressions (`[]`) define a set of characters where any one of the characters may be matched at that point of the regex. Characters placed inside square brackets are like instructions for the regex engine to match any one of those characters. This proves useful when matching characters from a specific set.

- `[abc]`: Matches either 'a', 'b', or 'c'. It will match 'a' in "anchor", 'b' in "bracket", and 'c' in "capturing".
- `[a-z]`: Matches any lowercase letter from 'a' to 'z'. Note that the range notation `-` is shorthand for delineating every character in that range.
- `[0-9]`: Matches any digit from '0' to '9'.
- `[^a-z]`: A caret `^` can be used at the beginning, inside square brackets, to "negate" a set of characters. This means matching any character that is NOT in the intended range or set. For example, `[^a-z]` will match any character that is not a lowercase letter.

**Examples:**
- `[aeiou]`: Matches any individual lowercase vowel. It will match 'e' in "regular" and 'a' in "flags".
- `[1-3]`: Matches any of the integers '1', '2', or '3'. It would match '2' in "vitaminB12@gmail.com".

Bracket expressions are essential for constructing patterns that require specific character matches, providing regex patterns both flexibility and precision.

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)