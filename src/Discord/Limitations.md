# Limitations

Almost everything in the platform has a limit, when you exceed them sometimes you are informed about it with a user friendly message and sometimes not - but it's not impossible the figure out the error in which case but it's tad technical. (Hint: Developer Console)

| Entities | Limit |
| ----- | ----- |
| Servers\* | `100` |
| Relationships\*\* | `1,000` |
| Pins (per channel) | `50` |
| Recipients (per DM channel) | `10` |
| Server Roles | `250` |
| Webhooks (per channel) | `10` |
| (Static) Emojis\*\*\*  | `50` |
| Animated Emojis\*\*\*  | `50` |
| Emoji Reactions (per message) | `20` |
| Server Channels\*\*\*\*  | `500` |
| Attachments (per message)\*\*\*\*\*  | `10` |
| Invites (per server) | `1,000` |
| Server Members\*\*\*\*\*\*  | `250,000` |
| Server Discovery Categories | `5` |

\* `200` for nitro subscribers

\*\* Relationships include Friends, Blocked users, Incoming and Outgoing friend requests

\*\*\*  By default servers are limited to `100` emojis (animated emojis included) but servers are able to bump this limit by being [boosted](<https://support.discord.com/hc/en-us/articles/360028038352-Server-Boosting-FAQ->)

\*\*\*\*  This limitation covers *all* kinds of channels: text, voice, stage, announcement and even categories! (categories are considered *parent* channels) that being said, all of them combined must not exceed the said limit

\*\*\*\*\*  Currently this is only a concern in mobile apps, desktop client doesn't allow sending more than one attachment per message

\*\*\*\*\*\*  By default members are capped at `250,000`, servers owners would need to [contact discord](<https://support.discord.com/hc/en-us/articles/360052841734-Server-Member-Cap-Increases->) for member cap increase when they reach the said limit