# Title The regex for a Matching a URL!



According to MDN, "Regular expressions are patterns used to match character combinations in strings. In JavaScript, regular expressions are also objects. These patterns are used with the exec() and test() methods of RegExp, and with the match(), matchAll(), replace(), replaceAll(), search(), and split() methods of String." The concept of a regular expression is to assist users in sorting and finding important sets of strings that they may need for whatever reason. They may be collecting telephone numbers for a database, or sorting web URL's. Regular expressions are often referred to as regex. This regex /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/ matches a URL.

## Summary
The URL matching regex ```/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/ ``` is used

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors
The Anchors of a regular expression are  the symbols at the beginning and end of the string. The opening anchor is the symbol ^ and the end is the symbol is $. 
  ^ is the anchor that matches the beginning of input.
    $ matches the end of the input string.
The code inside the opening and closing anchors is where the action is. This code is what does the matching of the URL.

### Quantifiers

Quantifiers communicate to the regex engine that it must match the quantity of the character or expression to its left. These are the quatifiers that are used in regex:
  ?, +, *, {n}, {n, }, {n,m}
  In the URL matching regex they are used in the following places:
    https?          Matches 'https', 'http'
    [\da-z\.-]+     Matches a single digit, group of letters (a-z), dot (.) or hyphen (-) 1 or more times
    [a-z\.]{2,6}    Matches 2 to 6 copies of the sequence [a-z\.]
    [\/\w \.-]*     Matches '/', '.', '-', 'www', '//'
  

### Character Classes
Character Classes ensure that a given sequence of characters matches a larger set of characters.

    [a-z]          Matches lowercase alphabetic characters between a and z
    \w             Matches a word
    \d             Matches a single character that is a digit
    .              Matches any character


### Grouping and Capturing
The use of grouping expressions is to allow for the extraction of the characters of a given group for validation. The text between paranthesis is a group.
    (https?:\/\/)       Matches: ' ', 'https://', 'http://'
    ([\da-z\.-]+)       Matches: 'ab.c-7', 'ab'
    ([a-z\.]{2,6})      Matches: 'ab.', '.ca'
    ([\/\w \.-]*)       Matches: '/', '/ab.'

### Bracket Expressions
Bracket expressions are used between brackets. In this example, we have the following Bracket Expressions.
    [\da-z\.-]
    [a-z\.]
    [\/\w \.-]

### Greedy and Lazy Match
These are my favorite named elements of a regular expression. Greedy and Lazy match. Are you kidding? What a country! These qualifiers allow you to find the "greedy" (longest) and "lazy" (shortest) match.

    ([\da-z\.-]+)       "+" operator is greedy as it allows character matching from one to an infinite amount of times.



## Author

Stephen Peña
penaone@gmail.com
https://gist.github.com/penaone/80f920d38f55e552ce1063e890a2050b
https://github.com/penaone