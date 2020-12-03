# Regex Cheat Sheet

| Character(s) | What it does |
|--------------|--------------|
. | A period. Matches any single character except the newline character.
^ | A caret. Matches a pattern at the start of the string.
\A| Uppercase A. Matches only at the start of the string.
$ | Dollar sign. Matches the end of the string.
\Z| Uppercase Z. Matches only at the end of the string.
[ ]| Matches the set of characters you specify within it.
\ | If the character following the backslash is a recognized escape character, then the special meaning of the term is taken. ---> Else the backslash () is treated like any other character and passed through. ---> It can be used in front of all the metacharacters to remove their special meaning.
\w | Lowercase w. Matches any single letter, digit, or underscore.
\W | Uppercase W. Matches any character not part of \w (lowercase w).
\s | Lowercase s. Matches a single whitespace character like: space, newline, tab, return.
\S | Uppercase S. Matches any character not part of \s (lowercase s).
\d | Lowercase d. Matches decimal digit 0-9.
\D | Uppercase D. Matches any character that is not a decimal digit.
\t | Lowercase t. Matches tab.
\n | Lowercase n. Matches newline.
\r | Lowercase r. Matches return.
\b | Lowercase b. Matches only the beginning or end of the word.
+ | Checks if the preceding character appears one or more times.
* | Checks if the preceding character appears zero or more times.
? |∙ Checks if the preceding character appears exactly zero or one time ∙ Specifies a non-greedy version of +, *
{ } | Checks for an explicit number of times.
( ) | Creates a group when performing matches.
< > | Creates a named group when performing matches.
