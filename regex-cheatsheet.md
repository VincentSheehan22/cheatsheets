# Regex Cheatsheet

## Basics
* `\^`: Matches at start of line (^[string]).
* `\^`: Matches negated ([^string]).
* `\.`
* `\*`
* `\$`
* `\?`
* `\+`
* `\\`: Escape.
* `\|`: Logical OR.
* `()`
* `{}`: Quantifiers.
* `[]`
* `[a-z]`
* `[A-Z]`
* `[0-9]`

## Character Classes
* `\d`: Digit, i.e., [0-9]. \D: Negated, i.e., [^0-9].
* `\w`: Character, i.e., [a-zA-Z0-9_]. \W: Negated.
* `\s`: Whitespace, i.e., [ \t\n\r\f\v]. \S: Negated.
* `\b`: Word boundary.
* `\n`: Newline.
* `\r`: Return.
* `\t`: Tab.

## IP Addresses
* `^\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}`

## MAC Addreses
* `[^\n0-9a-fA-F:.-]`
* `([0-9a-fA-F]{2})([0-9a-fA-F]{2})([0-9a-fA-F]{2})([0-9a-fA-F]{2})([0-9a-fA-F]{2})([0-9a-fA-F]{2})`, `\1:\2:\3:\4:\5:\6`
* `([0-9a-fA-F]{4})([0-9a-fA-F]{4})([0-9a-fA-F]{4})`, `\1.\2.\3`
* `([0-9a-fA-F]{2})([0-9a-fA-F]{2})([0-9a-fA-F]{2})([0-9a-fA-F]{2})([0-9a-fA-F]{2})([0-9a-fA-F]{2})`, `\1-\2-\3-\4-\5-\6`

## Python `re` Module
* compile()
* match()
* search()
* findall()
* finditer()
* sub()
* subn()
* split()
* group()
