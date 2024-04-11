# Regex Cheatsheet

## Basics
* `^`: Matches at start of line (`^[string]`).
* `^`: Matches negated (`[^string]`).
* `.`: Match any charaacter.
* `*`: Match any amount.
* `+`: Match at least once.
* `$`: End of string.
* `?<=`: Look behind.
* `?=`: Lookahead.
* `\`: Escape.
* `|`: Logical OR.
* `()`: Grouping.
* `{}`: Quantifiers.
* `[]`: Character set.
* `[a-z]`: Match a to z.
* `[A-Z]`: Match A to Z.
* `[0-9]`: Match 0 to 9.

## Character Classes
* `\d`: Digit, i.e., `[0-9]`.
* `\D`: Negated digit, i.e., `[^0-9]`.
* `\w`: Character, i.e., `[a-zA-Z0-9_]`.
* `\W`: Negated character, i.e., `[^a-zA-Z0-9_]`.
* `\s`: Whitespace, i.e., `[ \t\n\r\f\v]`.
* `\S`: Negated whitespace, i.e., `[^ \t\n\r\f\v]`.
* `\b`: Word boundary.
* `\n`: Newline.
* `\r`: Return.
* `\t`: Tab.

## IP Addresses
* `^\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}`

## MAC Addreses
### Line Starting with xx:
* `[^\n0-9a-fA-F:.-]`

### xx:xx:xx:xx:xx:xx
* `([0-9a-fA-F]{2})([0-9a-fA-F]{2})([0-9a-fA-F]{2})([0-9a-fA-F]{2})([0-9a-fA-F]{2})([0-9a-fA-F]{2})`, `\1:\2:\3:\4:\5:\6`

### xxx.xxx.xxx
* `([0-9a-fA-F]{4})([0-9a-fA-F]{4})([0-9a-fA-F]{4})`, `\1.\2.\3`

### xx-xx-xx-xx-xx-xx
* `([0-9a-fA-F]{2})([0-9a-fA-F]{2})([0-9a-fA-F]{2})([0-9a-fA-F]{2})([0-9a-fA-F]{2})([0-9a-fA-F]{2})`, `\1-\2-\3-\4-\5-\6`

## String between Strings
* `?<=first string(second string)?=third string`, `\1`

## Python `re` Module
* `compile()`
* `match()`
* `search()`
* `findall()`
* `finditer()`
* `sub()`
* `subn()`
* `split()`
* `group()`
