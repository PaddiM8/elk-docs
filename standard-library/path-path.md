# Path (path)
## add(path: String)

| Parameter | Type   | Description |
| --------- | ------ | ----------- |
| path      | String | Path to add |

Adds the provided path to $PATH and ~/.config/elk/path.txt.
Paths in path.txt are automatically added to $PATH each Elk session.

### Returns

(nil)

## all()

### Returns

(List) A list of all the paths in ~/.config/elk/path.txt.

## list()

### Returns

(String) A string displaying all the paths in ~/.config/elk/path.txt together with their index.

## remove(index: Integer)

| Parameter | Type    | Description |
| --------- | ------- | ----------- |
| index     | Integer |             |

Removes the path of the given index from $PATH and ~/.config/elk/path.txt. The index can be found with the help of the path::list function.

### Returns

(nil)

