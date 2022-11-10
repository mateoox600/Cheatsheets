# [<](index.md) - Array

## Syntax
---

```php
$array = array(             // $array = array
    "string_key" => 25,     // $array["string_key"] = 25
    24 => "string value",   // $array[24] = "string value"
    "inner_array" => array( // $array["inner_array"] = array
        "key" => "value",   // $array["inner_array"]["key"] = "value"
        "index zero",       // When no key is provided it will use the array index starting at zero for empty array, starting at last key + 1 if the last key is a number
        "one",
        24 => "twenty-four",
        "twenty-five"
    )
);
```

The key of an array can only be a `string` or an `int`. <br>
While the value can be any type.

```php
// can be represented with squared braces too
$array = [
    "key" => "value"
];
```

`float` keys will be rounded to `int` so that `8.7 -> 8`. <br>
`bool` keys will be converted to `int`. <br>
`NULL` key will be converted to an empty string. <br>
If you try to use any other type as a key, an `Illegal offset type.` error will be returned.

```php
$array[] = "value"; // pushes the value to the array
```

```php
[ $one, $two, $three, , $five ] = array("one", "two", "three", "four", "five"); // destructuring array to get each value

[ "one" => $one, "three" => $three ] = array("one" => 1, "two" => 2, "three" => 3) // destructuring associative array
```