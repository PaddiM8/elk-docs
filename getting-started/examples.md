# Examples

## Hello World

There are a few ways to write a hello world program:

```nim
# using the 'echo' program
echo hello world
echo "hello world"
echo("hello world")

# using the built-in 'println' function
println hello world
println "hello world"
println("hello world")
```

## Pipes

```rust
let hidLines = dmesg | grep HID | lines
for line in hidLines: echo(line | ansi::color blue)
```

## String Interpolation

```nim
let kernel = uname()
echo("Kernel: {kernel}")
```
