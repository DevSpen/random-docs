# Paginated Responses

Some commands may return paginated responses to evade invalid requests to discord due exceeding character limits in certain message fields, In this case Shirin will automatically add the following buttons in her message which will allow you to navigate through pages when clicked on:

![Goto First Button Preview](https://cdn.discordapp.com/emojis/857588155867463680.png?v=1&size=16 "Goto First") Jump to the first page\*

![Goto Previous Button Preview](https://cdn.discordapp.com/emojis/857588155858288670.png?v=1&size=16 "Goto Previous") Go to the previous page

![Goto Next Button Preview](https://cdn.discordapp.com/emojis/857588155851079690.png?v=1&size=16 "Goto Next") Go to the next page

![Goto Last Button Preview](https://cdn.discordapp.com/emojis/857588155817132052.png?v=1&size=16 "Goto Last") Jump to the last page\*

*Shirin will add these buttons if there are more than 2 pages, This is only sensical

Not to mention you only have so much time to interface with the paginated response before it times out and terminates, It's not going to await user action indefinitely. If possible Shirin will clear the buttons she added upon termination.