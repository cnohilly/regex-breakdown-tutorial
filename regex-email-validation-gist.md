# Regex Tutorial - E-Mail Verification

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.
```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/gm
```
This expression is used to verify an email. This expression uses the anchors ^ and $ at the start and end of the expression, and has 3 groups that are separated by an @ symbol and . (period). Using the global and multi-line flags, this expression allows for multiple matches and can verify several emails by placing each on a new line. This expression will only accept lowercase letters and uppercase letters would be considered invalid. Other than lowercase letters and standard numbers, the email username accepts underscore, hyphen and period as valid characters, the email domain name accepts periods and hyphens, and the email domain type only accepts lowercase letters and periods.

## Table of Contents

- [Regular Expression](#regular-expression)
- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regular Expression

```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/gm
```

The expression is broken up in the following manner:

* ` ^ `
    * start of string/line anchor
* ` ([a-z0-9_\.-]+) `
    * Group 1 with a set matching lowercase letters, digits 0-9, _ (underscore), . (period), and - (hyphen). + (plus sign) indicating that there must be 1 or more matches for the set.
* ` @ `
    * Require exactly to have the @ symbol
* ` ([\da-z\.-]+) `
    * Group 2 with a set matching lowercase letters, digits, . (period), and - (hyphen). + (plus sign) indicating that there must be 1 or more matches for the set.
* ` \. `
    * Require exactly to have a . (period).
* ` ([a-z\.]{2,6}) `
    * Group 3 with a set matching lowercase letters and . (period). Only allowing between 2 to 6 valid matches.
* ` $ `
    * end of string/line anchor
* ` gm `
    * Global and Multiline flags

## Regex Components

### Anchors

Matches a position in a string (or line with multi-line flag).

* ` ^ `
    * Matches the beginning of the string (or beginning of a line if using the multi-line flag)
* ` $ `
    * Matches the end of the string (or end of a line if using the multi-line flag)

### Quantifiers

Quantifiers are used to indicate the number of times a token preceding the quantifier should be matched. The expression used here only utilizes two quantifier types, the first being the ` + ` sign and the second being ` { 2 , 6 } `.

* ` + `
    * Matches 1 or more of the token
* ` { 2 , 6 } `
    * Quantifier in group 3 that indicates that the set should match 2 to 6 valid characters

### Character Classes

Matches a character from a specified set. In the example expression we use several ranges and specify a few characters.

* ` a-z `
    * Range of characters, all lowercase characters from a to z
* ` 0-9 `
    * Range of characters, all numbers from 0 to 9
* ` \d `
    * Predefined character class to match any digit character (0-9)
* ` _\.- `
    * Matches the specific characters for underscore, hyphen and period.

### Flags

Expression flags can change how the expression is interpreted.

* ` /g `
    * Global flag indicating that it should find all matches in the string rather than just the first match
* ` /m `
    * Multi-line flag enables the anchors ` ^ ` and ` $ ` to match the start and end of a line rather than just the start and end of a string

Since we're using the multi-line and global flags, we can get multiple matches by having each email address be its own line.

```
exampleemail@gmail.com
another@aol.com
```

### Grouping and Capturing

Grouping allows you to wrap a series of tokens in `( )` parenthesis and operate on them together. In the example expression, there are 3 groups.

* ` ([a-z0-9_\.-]+) `
    * Group 1 used for the email name
    * Matches lowercase letters, digits, underscore, period and hyphen
    * Valid matches: c-t-nohilly, example_email01, another.email
    * Invalid matches: CTNohilly, example#email, another?email
* ` ([\da-z\.-]+) `
    * Group 2 used for the first portion of the domain (name before the period)
    * Matches lowercase letters, digits, period and hyphen
    * Valid matches: bank2000, bank.2000, bank-2000
    * Invalid matches: BANK2000, bank_2000
* ` ([a-z\.]{2,6}) `
    * Group 3 used for the second portion of the domain (.com,.edu, etc after the period)
    * Matches lowercase letters and period.
    * Valid matches: com, edu, au.co
    * Invalid matches: 200, au-co, au_co

### Greedy and Lazy Match

The expression used does not have an example of lazy matching, but it does use the ` + ` sign and bracket quantifier `{ 2 , 6 }` which are both greedy by default and will find as many matches as possible.

## Author

My name is Chris Nohilly and I am a full-stack developer. 

You can find other examples of my work on my github: [cnohilly](https://github.com/cnohilly)