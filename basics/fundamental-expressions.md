# Fundamental Expressions

## Arithmetic

| Operation      | Symbol |
| -------------- | ------ |
| Addition       | +      |
| Subtraction    | -      |
| Negation       | -      |
| Multiplication | \*     |
| Division       | /      |
| Power          | ^      |

## Boolean Operations

| Operation                       | Symbol |
| ------------------------------- | ------ |
| Logical and                     | and    |
| Logical or                      | or     |
| Logical not                     | not    |
| Non-redirecting and (bash-like) | &&     |
| Non-redirecting or (bash-like)  | \|\|   |

{% hint style="info" %}
The `and`/`or` keywords are used for logical operations on booleans, while the non-redirecting variants `(`&& and `||`) are used to chain program invocations.
{% endhint %}

```nim
cd dir1 && mkdir dir2
echo(x and y)
```

## Comparisons

| Operation        | Symbol |
| ---------------- | ------ |
| Equals           | ==     |
| Not equals       | !=     |
| Greater          | >      |
| Less             | <      |
| Greater or equal | >=     |
| Less or equal    | <=     |

## Blocks

A block is a single expression that can contain several other expressions that are evaluated consecutively. The value of a block is always the value of the last expression in that block.

```nim
let x = {
    "one"
    "two"
}

assert(x == "two")
```

## Pipes

Pipe expressions are written with the syntax value `| receiver` where `value` is the value that should be sent to the `receiver` function or program. The behaviour is different depending on whether the receiving side is a function call or a program invocation.

### With Function Calls

When the receiving side is a function call, the pipe expression's `value` is prepended to the call's argument list, meaning it becomes the first argument of the call.

```bash
"1,2,3" | split(",")
```

is equivalent to

```bash
split("1,2,3", ",")
```

### With Program Invocations

When the receiving side is a program invocation, the pipe expression's value is sent to the standard input of the process created by the invocation. This behaviour can be compared to how pipes work in Bash.

```bash
cat file.txt | grep line
```
