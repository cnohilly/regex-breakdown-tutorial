# Title (replace with your title)

Introductory paragraph (replace this with your text)

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.
```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/gm
```
This Regex Expression is used to verify an email. This expression uses the anchors ^ and $ at the start and end of the expression, and has 3 groups that are seperated by an @ symbol and . (period). The expression is broken up in the following way: 


## Table of Contents

- [Regex Expression](#regex-expression)
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

## Regex Expression

```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/gm
```

The expression is broken up in the following manner:

* ```^```     
    * start of string/line anchor
* ```([a-z0-9_\.-]+) ```
    * Group 1 with a set matching lowercase letters, digits 0-9, _ (underscore), . (period), and - (hyphen). + (plus sign) indicating that there must be 1 or more matches for the set.
* ```@``` 
    * Require exactly to have the @ symbol
* ```([\da-z\.-]+) ```
    * Group 2 with a set matching lowercase letters, digits, . (period), and - (hyphen). + (plus sign) indicating that there must be 1 or more matches for the set.
* ``` \. ``` 
    * Require exactly to have a . (period).
* ```([a-z\.]{2,6}) ```
    * Group 3 with a set matching lowercase letters and . (period). Only allowing between 2 to 6 valid matches.
* ```$``` 
    * end of string/line anchor
* ```gm```
    * Global and Multiline flags

## Regex Components

### Anchors

* ^
    * Matches the beginning of the string (or beginning of a line if using the multi-line flag)
* $
    * Matches the end of the string (or end of a line if using the multi-line flag)

### Quantifiers

* { 2, 6 }
    * Quantifier in group 3 that indicates that the set should match 2 to 6 valid characters

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
