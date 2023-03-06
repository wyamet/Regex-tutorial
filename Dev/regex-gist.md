# Regex pattern to validate email addresses

Email validation is a crucial aspect of web development as it helps ensure that the user-provided email addresses are formatted correctly and avoid errors when communicating with the user. One of the most efficient and widely used methods of email validation is through regular expressions, which allows for precise matching of patterns in text strings. In this gist, we'll describe an effective regex pattern that can be used to validate email addresses in JavaScript applications. This pattern ensures that the email address is formated correctly and contains a valid domain name, and that it can be easily customized to suit specific validation requirements.

## Summary

The regex pattern we'll be describing is `/^[^\s@]+@[^\s@]+\.[^\s@]+$/` This pattern matches any string that contains an @ symbol followed by a valid domain name, and no whitespace characters before or after the email address. The regex pattern checks for a valid domain name by looking for the presence of a period (.) character immediately after the @ symbol. The domain name is then validated by matching one or more characters after the period character.

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

Regex anchors are used to specify where we match a regular expression. In this case
the regex pattern starts and ends with the `^` and `$` anchors, which indicate that the pattern must match the entire string.

### Quantifiers

regex quantifiers are used to specify how often we match a preceding regular expression.
In this case
The `+` quantifier is used to match one or more of the preceding character class or group. In this case, we're using it to match one or more non-whitespace characters (`\S`) before and after the @ symbol.

### OR Operator

In regular expressions, the OR operator allows you to match one of several possible patterns in a single expression. It is denoted by the pipe character `|`, which represents a logical OR.

There are no OR operator used in this pattern.

### Character Classes

We are using several character classes in this pattern:

- `[]` - A character class that matches any character within the brackets. In this pattern, we're using it to match any character that is not whitespace or the @ symbol.
- `+` - A quantifier that matches one or more of the preceding characters or groups.
- `.` - A period character that matches any single character.

### Flags

Flags in regular expressions are special options that can be added to the end of a regular expression to modify its behavior. They are denoted by a single letter after the last forward slash in the regular expression.

There are no flags in this pattern.

### Grouping and Capturing

Grouping and capturing in regular expressions refer to the ability to group multiple expressions together and capture the matched substring as a separate entity.

We do not use Grouping and Capturing in this expression.

### Bracket Expressions

bracket expressions (also known as character classes) allow you to specify a set of characters that can match a single character in the input string. Bracket expressions are enclosed in square brackets `[ ]` and contain a list of characters or character ranges that can be matched.
For example, the regular expression `/[aeiou]/` matches any single vowel in the input string.

We're using a bracket expression to match any character that is not whitespace or the @ symbol. The expression `[^...]` matches any character that is not in the specified set.

### Greedy and Lazy Match

greedy and lazy matching refer to the way in which the engine matches repeated patterns.
By default, regular expressions use greedy matching, which means that the engine tries to match as much of the input string as possible while still satisfying the pattern.
However, sometimes you may want to use lazy matching instead, which matches as little of the input string as possible while still satisfying the pattern. You can use the ? modifier to make a quantifier lazy.

there are no restrictions in this regex pattern.

### Boundaries

In regular expressions, boundaries are used to match the positions between characters in a string, rather than the characters themselves. Boundaries are useful when you want to match specific patterns in a string without matching other similar patterns that may be part of larger words or phrases.

There are two types of boundaries:

1. Word boundaries: Word boundaries match the position between a word character (as defined by the `\w` metacharacter) and a non-word character (as defined by the `\W` metacharacter). They are represented by the `\b` metacharacter. For example, the regular expression \bcat\b matches the word "cat" but not "catapult" or "scattered".

2. Line boundaries: Line boundaries match the position at the beginning or end of a line of text. They are represented by the `^` and `$` metacharacters, respectively. For example, the regular expression `^Hello` matches the word "Hello" only at the beginning of a line, while `World$` matches the word "World" only at the end of a line.

In this expression used to match emails, the `^` and `$` anchors serve as boundaries for the entire pattern.

### Back-references

back-references are regular expression commands which refer to a previous part of the matched regular expression.

There are no back-references used in this pattern.

### Look-ahead and Look-behind

Lookahead allows to add a condition for “what follows”. Lookbehind is similar, but it looks behind.

There are no look-ahead or look-behind assertions used in this pattern.

## Author

My name is Wyatt Domanski, I am a full stack bootcamp student at the University of Oregon.
[link](https://github.com/wyamet "Github").
