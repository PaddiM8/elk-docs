# Shell Customisation

### Init File

Elk looks for the init file in `~/.config/elk/init.elk`, and runs it when starting a new shell session if it exists. The init file can be compared to the `.bashrc` file used in bash.

### Custom Prompt

Elk generates the prompt by calling a function called `elkPrompt`. This function can be re-defined in the init file in order to customise the prompt. The default implementation of the `elkPrompt` function is the following:

{% code title="~/.config/elk/init.elk" %}
```rust
fn elkPrompt() {
    print((env::prettyPwd | ansi::color blue) + " ❯ ")
}
```
{% endcode %}
