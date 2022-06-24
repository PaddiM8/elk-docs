# Data Types

## Boolean

Booleans are expressed using the `true` and `false` keywords.

### Conversions

| Target type | Resulting value       |
| ----------- | --------------------- |
| String      | `"true"` or `"false"` |

## Dictionary

Dictionaries represent key-value pairs with unique keys. This can be expressed by putting comma-separated key-value pairs inside braces, such as `{ key1: value1, key2: value2 }`. Indexing is done with square brackets, eg. `dict["key1"]`.

```nim
let dict = {
    key1: "x",
    key2: "y",
}
assert(dict["key1"] == "x")
```

### Conversions

| Target type | Resulting value                                             |
| ----------- | ----------------------------------------------------------- |
| Boolean     | `true` if the dictionary is non-empty                       |
| String      | A string with comma-separated key-value pairs inside braces |

### Iteration

When a dictionary is iterated over, a tuple containing the key and the value is given.

```rust
for key, value in dict: echo("{key}: {value}")
```

## Error

The error type is used to represent errors and contains a string with an error message. An error message can be created using the `error` function, and the message can be retrieved by calling the `message` function.

```rust
let err = error("some error message")
if err | isType(Error): assert(message(err) == "some error message")
```

### Conversions



| Target type | Resulting value |
| ----------- | --------------- |
| Boolean     | `false`         |

## Float

Floats represent 64-bit floating point numbers and are created from number literals that contain decimals.

### Conversions

| Target type | Resulting value                    |
| ----------- | ---------------------------------- |
| Boolean     | `true`if the value is non-zero     |
| Integer     | The number as an Integer (floored) |
| String      | A string value                     |

## Integer

Integers represent 64-bit integer numbers and are created from number literals that do _not_ contain decimals.

### Conversions

| Target type | Resulting value                |
| ----------- | ------------------------------ |
| Boolean     | `true`if the value is non-zero |
| Float       | The number as a float          |
| String      | A string value                 |

## List

A list is a mutable dynamic data structure that can contain several values. Values are separated by commas. Indexing is done with square brackets and starts at zero. It is possible to index a list based on a range value in order to get a sub-list.

```rust
let items = [1, 2, 3]
assert(items[0] == 1)
items | add(4)
items | remove(0)

for item in items: echo(item)
```

### Conversions

| Target type | Resulting value                                                                                                    |
| ----------- | ------------------------------------------------------------------------------------------------------------------ |
| Boolean     | `true`if the list is non-empty                                                                                     |
| String      | A string containing the string representations of the values separated by commas and surrounded by square brackets |

## Nil

Nil values are represented by the `nil` keyword.

### Conversions

| Target type | Resulting value |
| ----------- | --------------- |
| Boolean     | `false`         |

## Range

A range expresses a numerical range between two values. The syntax for a regular range is `x..y` where `x` and `y`are any type of expressions. Both expressions are expected to be integer values. When the first value is excluded, eg. `..y`, the range will start at 0. When the last value is excluded, eg. `x..`, the range will not have a defined end.

Regular ranges are exclusive, meaning they don't include the value of the second expression. Iterating over the range `0..10` only yields the numbers 0 to 9. To instead make a range inclusive, an equal sign is added after the dots, eg. `0..=10`.

{% hint style="info" %}
It is sometimes necessary to place a range inside parentheses, such as `(1..)` to avoid expressions around it to be parsed as a part of the range.
{% endhint %}

```rust
for i in 0..10: echo(i)
let list = [1, 2, 3, 4, 5]
echo(list[1..3])
```

### Conversions

| Target type | Resulting value                                                                                 |
| ----------- | ----------------------------------------------------------------------------------------------- |
| Boolean     | `true`                                                                                          |
| List        | A list containing all the numbers of the range                                                  |
| String      | A string of the format `x..y` where `x` and `y`and the starting and ending values of the range. |

### Iteration

Iterating over a range yields every number in the range.

## String

Strings represent text values and are created by surrounding text with double quotes. Backslashes are used to escape characters. String operations are done immutably, but some standard library functions may result in mutation.

### Conversions

| Target type | Resulting value                                                                                                          |
| ----------- | ------------------------------------------------------------------------------------------------------------------------ |
| Boolean     | `true` for non-empty strings                                                                                             |
| Integer     | An integer value of the number represented in the string. A runtime error is thrown if the string is not a valid number. |
| Float       | A float value of the number represented in the string. A runtime error is thrown if the string is not a valid number.    |

### Escape Sequences

| Escape sequence | Symbol                       |
| --------------- | ---------------------------- |
| \b              | Backspace                    |
| \f              | Form feed                    |
| \n              | New line                     |
| \r              | Carriage return              |
| \t              | Horizontal tab               |
| \v              | Vertical tab                 |
| \0              | Null                         |
| \x...           | Unicode character, eg. \x1b  |

### Interpolation

String interpolation is done by surrounding code with braces in a string literal, for example `"Value: {x + 1}"`.

### Iteration

Iterating over a string yields each character in the string, one by one.

## Tuple

A tuple is an immutable data structure containing values. A tuple is created by surrounding comma-separated values with parentheses.

```rust
let a, b = (1, 2)
```

### Conversions

| Target type | Resulting value                                                                                                |
| ----------- | -------------------------------------------------------------------------------------------------------------- |
| Boolean     | `true`if the tuple is non-empty                                                                                |
| List        | A list containing the same values                                                                              |
| String      | A string containing the string representations of the values separated by commas and surrounded by parentheses |

## Type

A type in Elk is a static value that represents a data type. It is created by writing the name of the data type.

```rust
assert("some string" | isType(String))
let dataType = Integer;
```

### Conversions



| Target type | Resulting value             |
| ----------- | --------------------------- |
| Boolean     | `true`                      |
| String      | A string of the type's name |
