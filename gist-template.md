# Title (replace with your title)

Hello all, and welcome to my regex tutorial!  This tutorial was created with the idea of helping all who run across it understand regular expressions (Regex).  A Regex is a sequence a character that describe a certain search pattern.  We use regular expression with code to help us find patterns in a string, or to find and replace certain charcters with a string.  Lastly they are also used to be able to validate input data.

## Summary

Today I will be breaking down the Regex on validating an email input.  We will be breaking down the code in the order of individual Regex items and briefly explain what that certain code does.

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

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

### Anchors

The anchors on regular expressions belong to the family of regex tokens that do not match any characters.  Anchors act as either starting or stopping positions in the string we are looking at. 

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

The caret ^ above symbolizes the beginning of the string & the $ symbol symbolizes the end of the string. 

### Quantifiers

Quantifiers in regular expressions specify how many instances of a character, group, or character class must be present in the input for a match to be found.

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,7})$/

In our expression above the + will match one or more of the preceding token. In this case it will attempt to match [a-z0-9_\.-]. Two numbers with curly brackets {2,7} will match from two to seven from the previous token. In this case it will match [a-z\.]. As further examples: {2} would match exactly two, and {2,} would match two or more.

### OR Operator

You can use the | operator (logical OR) to match characters or expression of either the left or right of the | operator. For example the (t|T) will match either t or T from the input string.

We unfortunatly do not have any OR Operators in our expression.

### Character Classes

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,7})$/

Regular expressions contain special character classes that match types of characters.

In our expression, \d is used to match any digit character.

We must use the backslash here because it is necessary in order to differentiate between the digit class and a plain letter d.

Although we only have one character class in the expression, the behavior-changing function of a backslash is helpful in understanding another frequently used part of the expression, ".".

Unlike the other character classes, \d, \w (matching a word character) and \s (matching a whitespace character), the character class ".", which matches any character, does not require a backslash.

Because of the unique behavior of ".", the backslash must be used to negate its use as a character class and interpret it as the character ".".

### Flags

Flags are optional parameters that we can add to a plain expression to make it search in a different way. Each flag is denoted by a single alphabetic character, and serves different purposes in modifying the expression's searching behavior.

### Grouping and Capturing

Capturing groups are a way to treat multiple characters as a single unit. They are created by placing the characters to be grouped inside a set of parentheses. For example, the regular expression (dog) creates a single group containing the letters "d" "o" and "g". The portion of the input string that matches the capturing group will be saved in memory for later recall via backreferences

### Bracket Expressions

A bracket expression (an expression enclosed in square brackets, "[]" ) is a regular expression that shall match a specific set of single characters, and may match a specific set of multi-character collating elements, based on the non-empty set of list expressions contained in the bracket expression.

### Greedy and Lazy Match

### Boundaries

### Back-references

Backreferences match the same text as previously matched by a capturing group. Suppose you want to match a pair of opening and closing HTML tags, and the text in between. By putting the opening tag into a backreference, we can reuse the name of the tag for the closing tag.

### Look-ahead and Look-behind

## Author

Once again my name is Mario Gallardo if you would like to checkout further projects of mine you can visit my GitHub page down below! 

My GitHub [github] https://github.com/mgall13