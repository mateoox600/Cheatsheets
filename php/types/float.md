# [<](index.md) - Float

## Syntax
---

```php
$a = 1.234;
$b = 1.2e3; // float(1200)
$b = 1.2E3; // float(1200)
$c = 7e-10; // float(0.0000000007)
$d = 1_234.567;
```

## Precision
---

Format: `IEEE754` <br>
Minimal precision error: `1.11e-16`

```php
floor((0.1 + 0.7) * 10) // float(7)
```

Some operations can result in a `Nan` value you can check it with the `is_nan()` function. <br>
`Nan` represents an undefined or non representable value while calculating with floats. <br>
`INF` represents a float too big to be represented.

## Conversion
---

Float conversion:
```php
(float) value;
floatval(value);
```

### string -> float
- "10" -> 10.0
- "-25" -> -25.0
- "10.25" -> 10.25
- "8th php version" -> 8.0
- "php version 8th" -> 0.0
- "php version" -> 0.0