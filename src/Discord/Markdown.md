# Markdown

## Basics

| How to | Result |
| ----- | ----- |
| \*italics\* OR \_italics\_ | *italics* |
| \*\*bold\*\* | **bold** |
| \_\_underline\_\_ | __underline__ |
| \~\~strikethrough\~\~ | ~~strikethrough~~ |

## Combinations Example

| How to | Result |
| ----- | ----- |
| \*\*\*italic bold\*\*\* | ***italic bold*** |
| \*\*\~\~strikethrough bold\~\~\*\* | **~~strikethrough bold~~** |
| \_\_\*\*\*underline bold italics\*\*\*\_\_ | __***underline bold italics***__ |

## Code Blocks

| How to | Result |
| ----- | ----- |
| \`inline block\` | `inline block` |

### Multiline Blocks

\`\`\`text\`\`\`

will result in:

```text```

---

\`\`\`\<block language\>
text
\`\`\`

For example:

\`\`\`py
"""
green text
"""
\`\`\`

will result in:

![Code Block with syntax highlighting preview](https://cdn.discordapp.com/attachments/652544869314854934/868241690215981136/block.png)

Refer to <https://highlightjs.org/static/demo/> for a list of available block languages.

## Block Quotes

\> single line quote

will result in:

> single line quote

---

\>\>\> multi
line
quote

will result in:

![Multiline Quote Preview](https://cdn.discordapp.com/attachments/652544869314854934/868242564929708122/quote.png)

## Spoilers

\|\|spoilered message\|\|

will result in:

![Spoilered Message Preview](https://cdn.discordapp.com/attachments/652544869314854934/868243296785428510/spoiler.gif)

## Timestamp

Refer to [Timestamp](Timestamp.md).

## Escaping

If you are looking to display the characters in a literal manner, you're gonna have to escape them by prepending them with backslash.

For example: \\\`inline block\\\` would result in \`inline block\`, \\\~\\\~strikethrough\\\~\\\~ in \~\~strikethrough\~\~ and so on.