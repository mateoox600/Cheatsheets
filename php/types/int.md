# [<](index.md) - Int


## Syntax
---

```php
$a = 1234; // decimal
$a = -1234; // decimal
$a = 1_234_567; // decimal, _ used to separate sections of numbers (3 digits spacing is not imposed)
$a = 0123; // octal, the leading 0 makes it octal (string "0123" will be interpreted as decimal and not octal)
$a = 0o123; // octal
$a = 0xABC; // hexadecimal
$a = 0b10011; // binaty
```

## Max size
---

Mostly 32 bits (-2147483648 to 2147483647) but can be 64 bits, `PHP_INT_SIZE` contains integer size.

Size overflow (ex adding 5 to the max int size) will result in a int -> float conversion since float can be much bigger.

Integer division:
```php
var_dump(25/7);         // float(3.5714285714286) 
var_dump((int) (25/7)); // int(3)
var_dump(round(25/7));  // float(4) 
```

## Conversion
---
Int conversion:
```php
(int) value;
(integer) value;
intval(value);
```

### boolean -> int
- true      -> 1
- false     -> 0

### float -> int
- 10.7    -> 10
- 10.0    -> 10
- float > max int size -> 0

Warning: Do not convert unknown fraction to an int as it can give unwanted results
```php
echo (int) ( (0.1+0.7) * 10 ); // Echoes 7 !
```

### string -> int
- "10" -> 10
- "-25" -> -25
- "8th php version" -> 8
- "php version 8th" -> 0
- "php version" -> 0

### NULL -> 0

