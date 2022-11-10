# Php build-in type list

| name | value | conversion | size |
|---|---|---|---|
| NULL | NULL; can be assigned, or is default if no initialisation of variable | null == [] |  |
| bool | true / false | false == 0, 0.0, -0.0, "", "0", [], NULL |  |
| int | décimal 1234, -1234, 1_684_259; octal 0123, 0o123; hex 0x1A, 0xABC; binaire: 0b10001 | 0 == false, NULL; 1 == true;<br>n = leading number in string if none 0 | > limit system (32 bits, 64 bits) auto conversion en float |
| float | normal 1.234, -1.234, 1_684.259_351; scientific 1.2e4, 3.4e-6; error NaN (division by 0 for exemple) | All int conversion works with float | IEE 754 (~14 digits precision) |
| string | simple 'simple quotes', 'escaping simple quotes\' ';<br>double "double quotes", "escaping double quotes\" ", "inline formating $variable {$variable} no spaces ! { $variable}"; | "" = false, "1" == true | ~ 2 Go |
| array | function array( key => value, key1 => value1 ), array( value, value1 );<br>squared brackets [ key => value, key1 => value1 ], [ value, value1 ]; access on array $array[key];<br>array push $array[] = value2 |  |  |
|  	|  	|  	|  	|