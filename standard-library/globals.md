# Globals
## abs(x)

| Parameter | Type           | Description |
| --------- | -------------- | ----------- |
| x         | Integer, Float |             |

### Returns

(*) The input number made positive.

## add(container, value1: *)<br>add(container, value1: *, value2: *)

| Parameter         | Type             | Description                             |
| ----------------- | ---------------- | --------------------------------------- |
| container         | List, Dictionary |                                         |
| value1            | *                | List: Value to add<br />Dictionary: Key |
| (optional) value2 | *                | Dictionary: Value to add                |

Adds the given value to the container.

### Returns

(*) The same container.

### Example

```rust
list | add(x)
dict | add("name", "John")
```

## append(content: String, path: String)

| Parameter | Type   | Description                             |
| --------- | ------ | --------------------------------------- |
| content   | String | Text that should be written to the file |
| path      | String | A file path                             |

Appends the provided text to a file.

### Returns

(nil)

## assert(boolean: Boolean)

| Parameter | Type    | Description |
| --------- | ------- | ----------- |
| boolean   | Boolean |             |

Throws a runtime error if the given boolean is false.

### Returns

(nil)

## bool(value: *)

| Parameter | Type | Description               |
| --------- | ---- | ------------------------- |
| value     | *    | Value that should be cast |

### Returns

(Boolean) 

## ceil(x)

| Parameter | Type           | Description |
| --------- | -------------- | ----------- |
| x         | Integer, Float |             |

### Returns

(Float) The input number rounded up.

## error(message: String)

| Parameter | Type   | Description   |
| --------- | ------ | ------------- |
| message   | String | Error message |

### Returns

(Error) An Error with the provided message.

## float(value: *)

| Parameter | Type | Description               |
| --------- | ---- | ------------------------- |
| value     | *    | Value that should be cast |

### Returns

(Float) 

## floor(x)

| Parameter | Type           | Description |
| --------- | -------------- | ----------- |
| x         | Integer, Float |             |

### Returns

(Float) The input number rounded down.

## input()<br>input(prompt: String)

| Parameter         | Type   | Description                                         |
| ----------------- | ------ | --------------------------------------------------- |
| (optional) prompt | String | Text that should be printed before the input prompt |

Reads the next line from the standard input stream. This is used to get input from the user in a terminal.

### Returns

(String) The value given by the user.

## insert(list: List, index: Integer, value: *)

| Parameter | Type    | Description                        |
| --------- | ------- | ---------------------------------- |
| list      | List    | List to act on                     |
| index     | Integer | Index the item should be placed at |
| value     | *       | Value to insert                    |

Inserts a value at the specified index in a list.

### Returns

(List) The same list.

## int(value: *)

| Parameter | Type | Description               |
| --------- | ---- | ------------------------- |
| value     | *    | Value that should be cast |

### Returns

(Integer) 

## isType(value: *, type: Type)

| Parameter | Type | Description |
| --------- | ---- | ----------- |
| value     | *    |             |
| type      | Type |             |

### Returns

(Boolean) Whether or not the given value is of a specific type.

## join(list: List)<br>join(list: List, separator: String)

| Parameter            | Type   | Description                                              |
| -------------------- | ------ | -------------------------------------------------------- |
| list                 | List   | A list of values that will be stringified                |
| (optional) separator | String | Character sequence that should be put between each value |

### Returns

(String) A new string of all the list values separated by the specified separator string.

## len(container)

| Parameter | Type                    | Description |
| --------- | ----------------------- | ----------- |
| container | Tuple, List, Dictionary |             |

### Returns

(Integer) The amount of items in the container.

## lines(input: String)

| Parameter | Type   | Description |
| --------- | ------ | ----------- |
| input     | String |             |

### Returns

(List) A list of all the lines in the given string.

## list(value: *)

| Parameter | Type | Description               |
| --------- | ---- | ------------------------- |
| value     | *    | Value that should be cast |

### Returns

(List) 

## max(x, y)

| Parameter | Type           | Description |
| --------- | -------------- | ----------- |
| x         | Integer, Float |             |
| y         | Integer, Float |             |

### Returns

(*) The highest of the two input numbers.

## message(err: Error)

| Parameter | Type  | Description |
| --------- | ----- | ----------- |
| err       | Error |             |

### Returns

(String) The message stored in the given error.

## min(x, y)

| Parameter | Type           | Description |
| --------- | -------------- | ----------- |
| x         | Integer, Float |             |
| y         | Integer, Float |             |

### Returns

(*) The lowest of the two input numbers.

## print(input: *)

| Parameter | Type | Description    |
| --------- | ---- | -------------- |
| input     | *    | Value to print |

Prints the given value to the terminal, without adding a new line to the end.
If the input value is of the type Error, the error message is forwarded to stderr instead of stdout.

### Returns

(nil)

## println(input: *)

| Parameter | Type | Description    |
| --------- | ---- | -------------- |
| input     | *    | Value to print |

Prints the given value to the terminal while also adding a new line to the end.
If the input value is of the type Error, the error message is forwarded to stderr instead of stdout.

### Returns

(nil)

## random(from: Integer, to: Integer)

| Parameter | Type    | Description |
| --------- | ------- | ----------- |
| from      | Integer |             |
| to        | Integer |             |

### Returns

(Float) A random integer between the two provided values.

## read(path: String)

| Parameter | Type   | Description |
| --------- | ------ | ----------- |
| path      | String | A file path |

### Returns

(String) Text content of the file at the provided path.

## remove(container, index: *)

| Parameter | Type             | Description                 |
| --------- | ---------------- | --------------------------- |
| container | List, Dictionary |                             |
| index     | *                | Index of the item to remove |

Removes the item at the given index.

### Returns

(*) The same container.

## split(input: String)<br>split(input: String, delimiter: String)

| Parameter            | Type   | Description                   |
| -------------------- | ------ | ----------------------------- |
| input                | String | String to split up into parts |
| (optional) delimiter | String | Where to split                |

### Returns

(List) A list of all the different parts as a result of splitting the string.

## sqrt(x)

| Parameter | Type           | Description |
| --------- | -------------- | ----------- |
| x         | Integer, Float |             |

### Returns

(Float) The square root of the input number

## stepBy(range: Range, step: Integer)

| Parameter | Type    | Description     |
| --------- | ------- | --------------- |
| range     | Range   | Range to modify |
| step      | Integer | Step size       |

Changes the step size of the given range. The step size determines how much the range value should increase by after each iteration.

### Returns

(Range) The same range.

### Example

```nim
# 0, 2, 4, 6, 8, 10
for i in 0..10 | stepBy(2): echo(i)
```

## str(value: *)

| Parameter | Type | Description               |
| --------- | ---- | ------------------------- |
| value     | *    | Value that should be cast |

### Returns

(String) 

## type(value: *)

| Parameter | Type | Description               |
| --------- | ---- | ------------------------- |
| value     | *    | Value that should be cast |

### Returns

(Type) 

## withIndex(values)

| Parameter | Type     | Description |
| --------- | -------- | ----------- |
| values    | Iterable |             |

### Returns

(List) A list containing a tuple for each item in the original container.
The first item of the tuple is the item from the original container, while the second item is the index of that item.

### Example

```rust
for item, i in values: echo("{i}: {item}")
```

## write(content: String, path: String)

| Parameter | Type   | Description                             |
| --------- | ------ | --------------------------------------- |
| content   | String | Text that should be written to the file |
| path      | String | A file path                             |

Writes the provided text to a file, overwriting any previous content.

### Returns

(nil)

