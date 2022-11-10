# [<](index.md) - String

## Syntax
---

```php
'single quote string';
'you can have
multiple line in strings';
'you need to escape single quote \' to use them in single quote str';

"double quote string";
"Same as
\"Above\"";
```

## Formating
---

Double quotes can be used to format string with variables

```
$var = "World";

echo "Hello $var";
echo "Hello {$var}";
```

You can use braces to do more complex computation before formating the string. Spaces between braces and there content make the formating fail.

## Escaped sequence
---

Escaping sequense are reserved to double quotes

- `\n` - Linefeed
- `\r` - Carriage return
- `\t` - Horizontal tab
- `\v` - Vertical tab
- `\e` - Escape character
- `\f` - Form feed
- `\\` - Backslash
- `\"` - Double or simple quote

## Conversion
---

All scalar types (bool, int, float and string) can be converted to string. <br>
Other built-in types like array require the use of functions like `var_dump()` or `print_r()` to transform there value to text.