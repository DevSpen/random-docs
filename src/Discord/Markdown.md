# Markdown

## Basics

| How to | Result |
| ----- | ----- |
| \*italics\* OR \_italics\_ | *italics* |
| \*\*bold\*\* | **bold** |
| \_\_underline\_\_ | <ins>underline</ins> |
| \~\~strikethrough\~\~ | ~~strikethrough~~ |

## Combinations Example

| How to | Result |
| ----- | ----- |
| \*\*\*italic bold\*\*\* | ***italic bold*** |
| \*\*\~\~strikethrough bold\~\~\*\* | **~~strikethrough bold~~** |
| \_\_\*\*\*underline bold italics\*\*\*\_\_ | <ins>***underline bold italics***</ins> |

---

## Code Blocks

| How to | Result |
| ----- | ----- |
| \`inline block\` | `inline block` |

### Multiline Code Blocks

#### How to

\`\`\`text\`\`\`

#### Result

```text```

### Multiline Code Blocks with Syntax Highlighting

\`\`\`\<block language\> \
text \
\`\`\`

#### Example

\`\`\`py \
""" \
green text \
""" \
\`\`\`

#### Result

![Code Block with syntax highlighting preview](https://cdn.discordapp.com/attachments/652544869314854934/868241690215981136/block.png)

Refer to <https://highlightjs.org/static/demo/> for a list of available block languages.

---

## Block Quotes

#### How to

\> single line quote

#### Result

> single line quote

### Multiline Block Quotes

#### How to

\>\>\> multi \
line \
quote

#### Result

![Multiline Quote Preview](https://cdn.discordapp.com/attachments/652544869314854934/868242564929708122/quote.png)

---

## Spoilers

#### How to

\|\|spoilered message\|\|

#### Result

![Spoilered Message Preview](https://cdn.discordapp.com/attachments/652544869314854934/868243296785428510/spoiler.gif)

---

## Timestamp

Timestamp markdown is a rather "internationalized" way of displaying date and time where the information is rendered according to timezone and locale of the user. which is what timestamp field of [embed objects](https://discord.com/developers/docs/resources/channel#embed-object) does. (for those of you who are familiar with structure of embeds)

Just use a tool [like this](https://www.epochconverter.com/) to retrieve the unix epoch time and insert it in the markdown.

Either of the following notations are acceptable:

`<t:EPOCH_SECONDS>` → e.g <t:1472750028>

![Styleless timestamp preview](https://cdn.discordapp.com/attachments/652544869314854934/862699749652430868/timestamp_1.png)

`<t:EPOCH_SECONDS:STYLE>` → e.g <t:1472750028:R>

![Relative style timestamp preview](https://cdn.discordapp.com/attachments/652544869314854934/862699751602651156/timestamp_2.png)

Here is a list of available styles from [discord documentation](https://discord.com/developers/docs/reference#message-formatting-timestamp-styles).

| Style | Example Output               | Description     |
| ----- | ---------------------------- | --------------- |
| t     | 16:20                        | Short Time      |
| T     | 16:20:30                     | Long Time       |
| d     | 20/04/2021                   | Short Date      |
| D     | 20 April 2021                | Long Date       |
| f    | 20 April 2021 16:20          | Short Date/Time |
| F     | Tuesday, 20 April 2021 16:20 | Long Date/Time  |
| R     | 2 months ago                 | Relative Time   |

If you're a bot developer, here are couple methods for retrieving epoch seconds programmatically, to give you an idea.

JavaScript:
```js
let seconds = Math.floor(Date.now() / 1000);

msg.channel.createMessage(`<t:${seconds}>`);
// or styled
msg.channel.createMessage(`<t:${seconds}:F>`);
```

Python:
```py
from datetime import datetime
seconds = int(datetime.now().timestamp())

msg.channel.create_message(f"<t:{seconds}>")
# or styled
msg.channel.create_message(f"<t:{seconds}:F>")
```

---

## Escaping

If you are looking to display the characters in a literal manner, you're gonna have to escape them by prepending them with backslash.

For example: \\\`inline block\\\` would result in \`inline block\`, \\\~\\\~strikethrough\\\~\\\~ in \~\~strikethrough\~\~ and so on.