# Command Flags

Sometimes the normal ordered arguments are not enough or order of the arguments shouldn't really matter, Command flags are special kinds of arguments that don't really count as a part of the ordered arguments *provided* they mean something to the command used, Otherwise they are just normal arguments.

They are prefixed with two hyphens `--` and for the convenience of iOS mobile users `—` may be used as well (as `--` is coerced to `—`), You may also choose to prefix flags that are just one letter with one hyphen instead of two. (`-c` instead of `--c`)

All of the following are acceptable usages:
> @Shirin foo --bar baz

OR
> @Shirin foo --bar=baz

OR
> @Shirin --bar=baz foo

Things might not go as imagined if you approach like:
> @Shirin --bar baz foo
Here `baz foo` got consumed by the `--bar` flag, which is not our intent.

So to put simply, If we are looking to simply pass *one word* to our flag we can just do so via `=` no matter if it's before our first argument or last. With `=value` we make it explicit that our flag should only capture `value` and stop looking for more.

Otherwise if the value is not made explicit with `=` the flag is consumes everything after it until end of the message or encounterment of an another flag:
> @Shirin foo --bar baz wibble --wobble wubble

Here `baz wibble` is consumed by `--bar` and `wubble` by `--wobble`, So if we are looking to provide a flag that behaves as a simple toggle it's best that we provide it at the end of the message:
> @Shirin prunemembers 30 days --withcount

OR
> @Shirin prunemembers --withcount=true 30 days

Do note that flags are to be provided after command's name, So following **would not** work:
> @Shirin --withcount=true prunemembers 30 days