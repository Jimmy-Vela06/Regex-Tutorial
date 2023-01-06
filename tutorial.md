# Regex Tutorial

## Summary

Regex is an abbreviation of the term "regular expressions". A regular expression is a series of special characters and/ or text that help locate, match and manage text. These expressions can be extremely helpful in extracting information or data such as emails, URL’s, and phone numbers.

To most people regex can seem like gibberish and just random characters. This is a tutorial to help a person better understand regex and what the characters in the string of text in an expression mean.

Regex example that locates emails:

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

We will use the regex example above and break it down to better understand what each of these characters are achieving and all the regex components involved.

## Table of Contents

- [Regex Tutorial](#regex-tutorial)
  - [Summary](#summary)
  - [Table of Contents](#table-of-contents)
  - [Regex Components](#regex-components)
    - [Anchors](#anchors)
    - [Quantifiers](#quantifiers)
    - [Grouping Constructs](#grouping-constructs)
    - [Bracket Expressions](#bracket-expressions)
    - [Character Classes](#character-classes)
    - [The OR Operator](#the-or-operator)
    - [Flags](#flags)
    - [Character Escapes](#character-escapes)
  - [Author](#author)

## Regex Components

### Anchors

In Regex "anchor" is a term which defines the start and end of the "regular expression". They can be used to “anchor” the regex match at a certain position.

Anchor characters:

- `^` matches the beginning of a line
- `$` matches the end of a line
- `\A` matches the beginning of the input
- `\Z` matches the end of the input, or the end of the input plus a newline character, depending on the options passed to the regex engine -`\b` matches a word boundary -`\B` matches a position that is not a word boundary

In the example regex below the highlightd are examples of regex "anchors":

/`^`([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})`$`/

In the expression above the "anchors" used are the special characters `^` and `$`. The caret `^` matches the position at the start of the line. Similarly, `$` matches the position at the end of the line.

### Quantifiers

A "quantifier" is used to communicate how many characters are expected in the input. They are used to indicate how many instances of a character, group, or character class are present in the expression.

Quantifiers characters:

- `?` The preceding character or group is optional and will be matched at most once.
- `*` The preceding character or group will be matched zero or more times.
- `+` The preceding character or group will be matched one or more times.
- `{n}` The preceding character or group will be matched with exactly that qauntity provided within `{}`
  - Examples of how to write `{}`:
    - `{n}` The preceding character or group will be matched exactly n times.
    - `{n,}` The preceding character or group will be matched n or more times.
    - `{n,m}` The preceding character or group will be matched at least n times, but no more than m times.

In the example regex below the highlightd are examples of regex "quantifiers":

/^([a-z0-9_\.-]`+`)@([\da-z\.-]`+`)\.([a-z\.]`{2,6}`)\$/

In our match email regex example above the "quantifier's" being used are `+` and `{ }`. The `+` indicates that there is at least one or more characters with the the specifications within the `[a-z0-9_\.-]`. The `{2,6}` indicates that ther will at lest `2` but no more that `6` charcters with the specifications within the `[a-z\.]`.

### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
