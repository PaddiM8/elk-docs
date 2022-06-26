# remove(index: Integer)

| Parameter | Type    | Description |
| --------- | ------- | ----------- |
| index     | Integer |             |

Removes the path of the given index from $PATH and ~/.config/elk/path.txt. The index can be found with the help of the path::list function.

## Returns

(*) (nil or Error) An error if the index is out of range.
