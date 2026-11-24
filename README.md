# Privacy policy for Alerto

Last updated: 2026-11-23

Alerto is a browser add-on. The store name is Alerto - Facebook Marketplace Alerts. It looks at one Facebook Marketplace results page in a minimized window in the account's own browser, after the account presses Start. It never asks for the Facebook password, and it never copies the Facebook login.

Watches stay on the device. A billing service only tells Free from a paid Fast month. Contact: kizyakov.d@proton.me

## What stays on the device

The add-on stores these on the device, in the browser's local storage:

- Watches the account saves, including the item line, city segment, prices, and exclude words.
- Seen listing ids for those watches.
- Logs, if the account turned Logs on.
- The Telegram bot token the account pastes. Pages in the add-on are not given that token.
- The Telegram chat id that accepted the test message.
- The 6-digit start code, which is also in the bot name.
- The Discord webhook id and token, after the account picks a channel. Pages in the add-on are not given that token.
- A billing install id, used only to read whether a Fast month is still paid.
- A billing key that stays on the device. It is sent only with that install id, so the install id alone cannot cancel the month.
- Whether the Fast month is still paid, and the date it ends. That record stays on the device. A failed read does not drop Fast before that date.

Uninstalling the add-on removes that store with the browser's normal removal of the add-on. There is no login on our server. A Fast month also has a Stripe customer, keyed by the install id. That customer is not removed by uninstall. Email kizyakov.d@proton.me to delete it.

## What leaves the device

Four places only.

Facebook. The check opens a Marketplace results page in a minimized window, using the login already in that browser. The page is read for listing fields: title, price text, location line, listing id, and posted time. The document is not kept. A listing's own page is not opened. Images and media in that check window are blocked. Typing a city uses that same minimized window. It asks Facebook for matching cities and keeps the city id and the line Facebook showed. That ask reads the token Facebook already placed on the page and sends it back to Facebook. The token is not stored. It does not read a tab the account is looking at.

Telegram. After the account creates a bot and the test message is accepted, a match is sent by that bot to the chat that locked. The message is the watch name, the title, the price text, the location line, and a link built from the listing id. The bot token is sent only to `api.telegram.org` so that bot can answer.

Discord. After the account picks a server and a channel, a match is posted to that channel. The same five lines. The webhook token is sent only to `discord.com` so that channel can receive it. There is no client secret in the add-on.

Billing. Upgrade opens Stripe for the $12.75 Fast month. The add-on sends the install id and the billing key to `alerto-billing.vercel.app` and reads back whether that month is paid and when it ends. That answer is kept on the device until that date. A failed read does not erase it. The card number is not sent by the add-on and is not stored. Stripe holds the customer for that install id.

No other party receives the watches, the token, the chat id, the webhook token, or the listing fields.

## What this add-on does not do

- It does not ask for the Facebook password.
- It does not copy the Facebook login into its store.
- It does not sell data.
- It does not run ads.
- It does not load code from a server.
- It does not read a Marketplace tab the account is looking at.

## One browser on a network

Run this add-on in one browser on a network. A second copy on the same network can make Facebook stop the account.

## Questions

Email kizyakov.d@proton.me with questions or suggestions.
