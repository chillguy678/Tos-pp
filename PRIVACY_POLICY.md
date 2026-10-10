# Privacy Policy — Heaven

**Effective date:** 10 October 2026  
**Privacy contact:** [chillguyowns@proton.me](mailto:chillguyowns@proton.me)

## 1. What Heaven does

Heaven is a Discord bot that posts an alert in a server channel when a member is playing a game selected by that server's administrator. After the administrator configures a game and alert channel, Heaven posts a public notice explaining that alerts are enabled by default and how to opt out. Members are included by default unless they use `/presence opt-out`. They can use `/presence opt-in` to be included again, `/presence status` to check their setting, and `/presence privacy` to open this policy.

## 2. Information processed

When Discord sends Heaven a Presence update for a server, Heaven receives a Presence event. For members who have not opted out, Heaven checks the event for a current activity of type **Playing** and checks whether its name matches the administrator's configured game filter. It uses that result to decide whether to post an alert in the configured Discord channel.

Heaven does not use message text, online/idle/offline status, custom status, or device status for this feature. The alert message includes a mention of the member and the administrator-configured game filter.

Discord still delivers Presence event payloads to Heaven while Presence Intent is enabled. For members on the opt-out list, the bot's feature code returns before inspecting their activity list.

## 3. Information stored

Heaven's local settings file on the computer/server running the bot stores:

- Discord server ID;
- configured alert-channel ID;
- configured game-name filter;
- Discord user IDs of members who opted out; and
- whether the public notice has been posted.

Heaven does **not** write Presence status, activity names, or activity history to a database or file. Current activity information is processed in memory to decide whether to send a matching alert. A temporary in-memory set is used to avoid repeated alerts while a member remains in a matching activity; it is cleared when the bot process stops.

An opt-out user ID remains in the settings file until the member uses `/presence opt-in` or the bot operator removes the data. Because Heaven does not request the Server Members intent, an opt-out record may remain if the member leaves the server. They may contact the privacy address below to request deletion. Deleting the settings file also removes the server configuration and all saved opt-out choices.

## 4. How information is used and shared

Heaven uses Presence information only for the game-alert feature described above. This version does not use it for advertising, profiling, sale, or AI/ML model training. An alert is posted to the channel selected by the server administrator; members who can view that channel may see it.

The bot process runs on a computer/server operated or selected by the bot operator, outside Discord. Current activity information is processed there in memory when Discord sends a Presence event. This example does not add analytics, advertising, or AI/ML services. The bot operator is responsible for reviewing any additional service used to run or monitor the bot and updating this policy if the data handling changes.

Discord handles its own services under its policies and terms. Heaven does not control Discord's own collection or handling of data.

## 5. Opting out and data requests

- Run `/presence opt-out` in the server to stop Heaven's feature code from inspecting your activity details for alerts. Discord may still deliver Presence event payloads to the bot while Presence Intent is enabled.
- Run `/presence opt-in` to remove your opt-out preference and be included again.
- Run `/presence status` to check your setting.
- To request deletion of an opt-out record, contact [chillguyowns@proton.me](mailto:chillguyowns@proton.me) and identify the Discord server where Heaven is used. Do not send your account password or any bot token.

## 6. Security and changes

The bot operator should restrict access to the computer/server running Heaven and keep the Discord bot token secret. No internet-connected service can guarantee perfect security. This policy should be updated if Heaven's features, data handling, or use of additional services changes.

## 7. Contact

For questions or requests about this policy, email [chillguyowns@proton.me](mailto:chillguyowns@proton.me).
