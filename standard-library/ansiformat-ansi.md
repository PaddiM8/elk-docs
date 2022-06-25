# AnsiFormat (ansi)
## color(input: String, colorName: String)

| Parameter | Type   | Description                                                                                                      |
| --------- | ------ | ---------------------------------------------------------------------------------------------------------------- |
| input     | String | Text that should be colored                                                                                      |
| colorName | String | Color name. One of: default, black, red, green, yellow, blue, magenta, cyan, white, brightBlack, brightRed, etc. |

### Returns

(String) A string containing ansi escape codes that result in colored text in the terminal.

## bold(input: String)

| Parameter | Type   | Description                   |
| --------- | ------ | ----------------------------- |
| input     | String | Text that should be made bold |

### Returns

(String) A string containing ansi escape codes that result in bold text in the terminal.

## italic(input: String)

| Parameter | Type   | Description                     |
| --------- | ------ | ------------------------------- |
| input     | String | Text that should be made italic |

### Returns

(String) A string containing ansi escape codes that result in italic text in the terminal.

## ansiReset()

### Returns

(String) A string containing the ansi escape code for resetting colors and other things to their default state.

