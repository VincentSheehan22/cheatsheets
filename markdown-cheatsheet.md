# Markdown Cheatsheet

## Table of Contents
```
* [Headings](#heading)
* [Unordered Lists](#unordered-lists)
* [Ordered Lists](#ordered-lists)
* [Tables](#tables)
* [Checkboxes](#checkboxes)
* [Block Quotes](#block-quotes)
* [Code](#code)
* [Code Blocks](#code-blocks)
* [Slides](#slides)
```

> * [Headings](#heading)
> * [Unordered Lists](#unordered-lists)
> * [Ordered Lists](#ordered-lists)
> * [Tables](#tables)
> * [Checkboxes](#checkboxes)
> * [Block Quotes](#block-quotes)
> * [Code](#code)
> * [Code Blocks](#code-blocks)
> * [Slides](#slides)

## Headings
```
# Heading 1
## Heading 2
### Heading 3
```

> # Heading 1
> ## Heading 2
> ### Heading 3

## Unordered Lists
```
* Item 1
* Item 2
    * Sub-Item 1
- Item 3
- Item 4
    - Sub-Item 1
```

> * Item 1
> * Item 2
>     * Sub-Item 1
> - Item 3
> - Item 4
>     - Sub-Item 1

## Ordered Lists
```
1. Item 1
2. Item 2
    1. Sub-Item 1
3. Item 3
4. Item 4
    1. Sub-Item 1
```

> 1. Item 1
> 2. Item 2
>     1. Sub-Item 1
> 3. Item 3
> 4. Item 4
>     1. Sub-Item 1

## Tables
```
Heading 1    | Heading 2       | Heading 3
:---         | :---:           | ---:
left-aligned | centre-aligned  | right-aligned
1            | 1               | 1
2            | 2               | 2
3            | 3               | 3
```

> Heading 1    | Heading 2       | Heading 3
> :---         | :---:           | ---:
> left-aligned | centre-aligned  | right-aligned
> 1            | 1               | 1
> 2            | 2               | 2
> 3            | 3               | 3

## Checkboxes
```
* [ ] Unticked
* [x] Ticked
```

> * [ ] Unticked
> * [x] Ticked

## Block Quotes
```
> quote
```

> > quote

## Code
```
`string`
```

> `string`

## Code Blocks
### Fenced
#### Plaintext    
```
    ```
    Plaintext string.
    ```
```

> ```
> Plaintext string.
> ```

#### Python
Apply 'Python' header for syntax highlighting.

```
    ```Python
    print("Python string")
    ```
```

> ```Python
> print("Python string")
> ```

#### JSON
Apply 'JSON' header for syntax highlighting.

```
    ```JSON
    { "Host ID": "0000FJZ23220Z6F", "License Version": "00.000", "Validation Key": "83A8199E4340530A7F871F5E0E12B815"}
    ```
```

> ```JSON
> { "Host ID": "0000FJZ23220Z6F", "License Version": "00.000", "Validation Key": "83A8199E4340530A7F871F5E0E12B815"}
> ```

### Tabs
```
    code
```

>    code

## Slides
```
---
marp: true
---

# Slide 1
Slide contents

---

# Slide 2

---

# Slide 3

```
