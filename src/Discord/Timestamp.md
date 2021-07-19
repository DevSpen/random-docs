# How to use the timestamp markdown

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