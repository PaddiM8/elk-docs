# Environment (env)
## prettyPwd()

### Returns

(String) A string containing a modified version of the path to the current directory (the value of $PWD). The names of all the directories in the path except for the last one are replaced with their first letter, and '/home/user' is replaced with a tilde.

### Example

```rust
assert(prettyPwd() == "~/P/e/src")
```

