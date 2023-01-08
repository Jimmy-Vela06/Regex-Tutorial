# Regex Tutorial

## Summary

Regex is an abbreviation of the term "regular expressions". A regular expression is a series of special characters and/ or text that help locate, match and manage text. These expressions can be extremely helpful in searching and pulling information or data such as emails, URL’s, and phone numbers.

To most people regex can seem like gibberish and just random characters. This is a tutorial to help a person better understand regex and what the characters in the string of text in an expression mean.

Below is a regex example that locates emails:

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

In Regex "anchor" is a term which defines the start and end of the regular expression.

In the example regex below the highlightd are examples of regex "anchors":

/`^`([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})`$`/

In the expression above the "anchors" used are the special characters `^` and `$`. The caret `^` matches the position at the start of the line. Similarly, `$` matches the position at the end of the line. Indicateting the start and end of the regular expresion.

### Quantifiers

A "quantifier" is used to identify how many characters are expected in the input. They are used to indicate how many instances of a character, group, or character class are present in the expression.

In the example regex below the highlightd are examples of regex "quantifiers":

/^([a-z0-9_\.-]`+`)@([\da-z\.-]`+`)\.([a-z\.]`{2,6}`)\$/

In our match email regex example above the "quantifier's" being used are `+` and `{ }`. The `+` indicates that there is at least one or more "characters, groups, or character classes" within the `[a-z0-9_\.-]`. The `{2,6}` indicates that ther will at lest `2` but no more that `6` charcters with the specifications within the `[a-z\.]`.

### Grouping Constructs

"Grouping construncts" in regex are used to group together part of a regular expression so that it can be treated as a unit. The main grouping format is using`( )`.

In the example regex below the highlightd are examples of regex "grouping constructs" using `( )`:

/^`([a-z0-9_\.-]+)`@`([\da-z\.-]+)`\.`([a-z\.]{2,6})`\$/

Each highlighted section indicates a group within the the expression.

### Bracket Expressions

"Bracket Expressions" use `[ ]` to set character/s or character ranges that you want to match.

In the example regex below the highlightd are examples of regex "bracket expressions" using `[ ]`:

/^(`[a-z0-9_\.-]`+)@(`[\da-z\.-]`+)\.(`[a-z\.]`{2,6})\$/

The `[]` in the example contain the character specifications the regex is looking to match.

### Character Classes

In a regex "character classes" are often used to specify which characters you want to match in a search pattern.

In the example regex below the highlightd are examples of regex "character classes":

/^([`a-z0-9_\.-`]+)@([`\da-z\.-`]+)\.([`a-z\.`]{2,6})\$/

In the higlighted `a-z0-9_\.-` within the 1st bracket expresion `a-z` indicates any lower case alphabetic character. `0-9` indicates any number character. The `_` and `-` matches with underscores and hyphens. `.\` will match with a period.

In the 2nd bracket expression you will see a `\d` this indicates any matches with any number character. Another way to write `0-9`. Similarly you can use `\w` to indicate any character that is `a-z`.

### The OR Operator

The "OR operator" within a regular expression is defined using `|` . It indicates it could match with either of the components that are seperated with the `|`.

We do not have an example of a "OR operator" in our regex match email for but for example....

`Jimmy | Vela` will search for `Jimmy` if not found then the example will search for `Vela`. Hence the "OR"

### Flags

"Flags" are optional parameters that can be added to an expression to make it search in different way.

We do not have an example in our regex match email for example....

- `g` makes the regular expression global, meaning that it will search for all matches in the input string, rather than stopping after the first match. Example of g would be /HolaWorld/`g` : this will search for all occurrences of the phrase `HolaWorld`

- `i` makes the regular expression case-insensitive. So if use /HolaWorld/`i` in the search it can match with `HoLaWoRlD`.

### Character Escapes

"Character escapes" use a backslash `\` followed by a character that represents a special meaning.

Here are a common character escapes and there meanings:

- `\d` any digit `0-9`
- `\s` any whitespace character `space, tab, newline`
- `\w` any word character `a-z, A-Z, 0-9, and underscores`

In the regex example to search for an email we use `\d` in the 2nd group within the bracket expression to search any digit character.

/^([a-z0-9_\.-]+)@([`\d`a-z\.-]+)\.([a-z\.]{2,6})\$/

## Author

I hope you found this Javascript Regex tutorial helpful. If you wish to contact me my Link to my github profile below.
https://github.com/Jimmy-Vela06
