# stepBy(range: Range, step: Integer)

| Parameter | Type    | Description     |
| --------- | ------- | --------------- |
| range     | Range   | Range to modify |
| step      | Integer | Step size       |

Changes the step size of the given range. The step size determines how much the range value should increase by after each iteration.

## Returns

(Range) The same range.

## Example

```nim
# 0, 2, 4, 6, 8, 10
for i in 0..10 | stepBy(2): echo(i)
```
