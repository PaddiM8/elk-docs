# add(container, value1)<br>dd(container, value1, value2)

| Parameter         | Type             | Description                             |
| ----------------- | ---------------- | --------------------------------------- |
| container         | List, Dictionary |                                         |
| value1            | *                | List: Value to add<br />Dictionary: Key |
| (optional) value2 | *                | Dictionary: Value to add                |

Adds the given value to the container.

## Returns

(*) The same container.

## Example

```rust
list | add(x)
dict | add("name", "John")
```
