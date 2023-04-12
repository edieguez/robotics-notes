# [Regular expressions](https://www.regular-expressions.info/tutorial.html)

> Is a sequence of characters that specifies a search pattern in text

## Literal characters

Just plain text with no special meaning for the regex engine

``` regex
This is a literal string
```

## Special characters

Special characters are characters that have a special meaning in a regular expression. They are used to define the search pattern. **You can scape them with a backslash `\`**

## Anchors

Anchors are characters that define the start and end of a string. They are used to match a pattern only at the beginning or end of a string. The following regex will match any string that starts with `invoice-`

``` regex
^invoice-
```

**Can be used within `[]` to negate the set**

## Dollar `$`

Matches the end of the string. The following example will match any string that ends with `.pdf`

``` regex
\.pdf$
```

## Character classes or sets

A character class is a set of characters that you wish to match. You can define a character class with square brackets `[ ]`. The following example will match `gray` and `grey`. The order of the characters in the class does not matter.

``` regex
gr[ae]y
```

You can also specify a range of characters by using a hyphen `-`. The following example will match any letter (upper and lowercase) and numbers from `0` to `9`

``` regex
[a-zA-Z0-9]
```

Adding a caret `^` inside the brackets will negate the character class. The following example will match any character that is **not a letter or a number**

``` regex
[^a-zA-Z0-9]
```

## Shorthand character classes

- `\d` Matches any digit. Equivalent to `[0-9]`
- `\D` Matches any non-digit character. Equivalent to `[^0-9]`
- `\w` Matches any word character (alphanumeric character plus underscore). Equivalent to `[a-zA-Z0-9_]`
- `\W` Matches any non-word character. Equivalent to `[^a-zA-Z0-9_]`
- `\s` Matches any whitespace character (includes tabs and line breaks). Equivalent to `[ \t\r\n\f]`
- `\S` Matches any non-whitespace character. Equivalent to `[^ \t\r\n\f]`

## Dot `.`

Matches any character except line breaks. **Use with caution: many times is better to use a set or set negation**

## Alternation

Alternation is a way to match one of several expressions. It is done with the pipe `|` character. The following example will match `cat` or `dog`

``` regex
cat|dog
```

## Quantifiers

Quantifiers are used to specify how many times a character, group or character class must be repeated in order to match. **Quantifiers are greedy by default**

- `?` Matches the preceding character or group zero or one time. Equivalent to `{0,1}`
- `*` Matches the preceding character or group zero or more times. Equivalent to `{0,}`
- `+` Matches the preceding character or group one or more times. Equivalent to `{1,}`
- `{n}` Matches the preceding character or group exactly `n` times
- `{n,}` Matches the preceding character or group `n` or more times
- `{n,m}` Matches the preceding character or group at least `n` times, but not more than `m` times

## Grouping

Grouping is done with parentheses `()`. The following example will match `gmail.com` or `hotmail.com`

``` regex
(gmail|hotmail)\.com
```
