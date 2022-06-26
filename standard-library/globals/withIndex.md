# withIndex(values)

| Parameter | Type     | Description |
| --------- | -------- | ----------- |
| values    | Iterable |             |

## Returns

(List) A list containing a tuple for each item in the original container.
The first item of the tuple is the item from the original container, while the second item is the index of that item.

## Example

```rust
for item, i in values: echo("{i}: {item}")
```
