# Command Arguments

Arguments are user input which are delivered to the bot for processing whatever it needs to be processed depending on purpose of the invoked command.
A command may or may not have required arguments, Not providing sufficient or appropriate arguments or providing arguments to commands that don't take any at all will result in termination of the command execution and an error message being presented to you.

`<prefix><command> [1st argument] [2nd argument] [3rd argument] ... [Nth argument]`

For example, The `help` command takes a single optional argument that would show the extended help for a particular command:
> @Shirin help hex

A command-specific help exposes some details a `help` command invocation without argument wouldn't as it's simply a list of commands, Such as a description about the command (if any, there usually is), the flags (more on that later) and arguments command accepts, an optional argument is notated via square brackets `[]` surrounded around them and required ones via angle brackets `<>`.

Not providing an optional argument typically defaults to a pre-defined behavior, For example:
> @Shirin hex

This command would return preview of a random color, `hex` also takes an optional argument which would preview a particular color by it's hexadecimal representation:
> @Shirin hex 0xff9966