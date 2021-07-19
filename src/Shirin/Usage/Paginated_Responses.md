# Paginated Responses

Some commands may return paginated responses to evade invalid requests to discord due exceeding character limits in certain message fields, In this case Shirin will automatically add the following buttons in her message which will allow you to navigate through pages when clicked on:

![goto_first](https://cdn.discordapp.com/emojis/852651398742540333.png?v=1&size=16 "Goto First") Jump to the first page\*

![goto_prev](https://cdn.discordapp.com/emojis/852651399267352586.png?v=1&size=16 "Goto Previous") Go to the previous page

![goto_next](https://cdn.discordapp.com/emojis/852651399245856769.png?v=1&size=16 "Goto Next") Go to the next page

![goto_last](https://cdn.discordapp.com/emojis/852651402772742204.png?v=1&size=16 "Goto Last") Jump to the last page\*

*Shirin will add these buttons if there are more than 2 pages, This is only sensical

Not to mention you only have so much time to interface with the paginated response before it times out and terminates, It's not going to await user action indefinitely. If possible Shirin will clear the buttons she added upon termination.