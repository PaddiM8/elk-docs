# Functions

## Declaration

Functions are declared with the syntax `fn functionName(param1, param2) {}` or `fn functionName(param1, param2): expression` where there can be an arbitrary amount of parameters. With the former, the return value is either the value of the block or a value passed to a `return` expression. With the latter, the return value is simply the value of the expression after the colon.

```rust
fn add(x, y) {
    x + y
}
```

is equivalent to

```rust
fn add(x, y) {
    return x + y
}
```

and

```rust
fn add(x, y): x + y
```

## Usage

There are two different ways to express a function call: parenthesised and shell-style.

### Parenthesised

The syntax for parenthesised function calls is similar to that of general-purpose languages like Python. Arguments can be of any data type.

```rust
someFunction("hello", 3/2)
```

### Shell-style

Shell-style function calls take _text_ arguments separated by white-space, similar to shell languages. Anything after the function name up until the end of the function call is parsed as a string value. Double quotes for arguments are optional.

```ruby
someFunction hello world # equivalent to someFunction("hello", "world")
```

The end of a shell-style function call is detected upon reaching one of the following tokens:

* `)`
* `{`
* `}`
* `|`
* `&&`
* `||`
* `;`
* New line
* &#x20;`->` (incl. surrounding spaces)

```rust
let line = read file | len
let fileContents = read file
(someFunction a b) + "c"
```
