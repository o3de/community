# Discord Tips, Tricks and Troubleshooting

- [Two-Factor Authentication (2FA)](#two-factor-authentication-2fa)
- [Screen Sharing](#screen-sharing)
- [Change Username on Discord](#change-username-on-discord)
- [Custom Discord Rich Presence](#custom-discord-rich-presence)
- [Text Formatting](#text-formatting)
- [Color Codes](#color-codes)
- [Privacy and Notifications](#privacy-and-notifications)
- [Privacy](#privacy)
    - [Desktop Privacy Settings:](#desktop-privacy-settings)
    - [Mobile Privacy Settings:](#mobile-privacy-settings)
- [Notifications](#notifications)
    - [Desktop Notification Settings:](#desktop-notification-settings)
    - [Mobile Notification Settings:](#mobile-notification-settings)
- [Error messages](#error-messages)


## Two-Factor Authentication (2FA)

 Discord has updated their policies to require users to have 2FA enabled in order to perform certain actions on servers. These actions include creating server events, performing moderation actions, managing server settings, and other elevated actions. This policy update is designed to improve server security and prevent unauthorized access to Discord servers. 

If you want to create events or perform moderation actions on a Discord server, you will need to have 2FA enabled on your account. The process for enabling 2FA is outlined in the previous responses. Once you have 2FA enabled, you should be able to access the server permissions you need.

Please note that the exact permissions required for each server can vary, as server owners have the ability to customize permissions for their own servers. So if you're having trouble accessing certain permissions even after enabling 2FA, you may need to contact the server owner or server admins for further assistance.

Enabling two-factor authentication (2FA) on Discord can help increase the security of your account by requiring an additional verification step beyond your password. Here are the steps to enable 2FA on Discord: 


1. Open Discord and log in to your account.
2. Click on the gear icon in the bottom left corner of the Discord window to open User Settings.
3. Click on the "My Account" tab on the left-hand side of the User Settings window.
4. Scroll down until you see the "Two-Factor Authentication" section, and click the "Enable Two-Factor Authentication" button.
5. You will then be prompted to choose a verification method: either using an authentication app or receiving a text message with a verification code. If you choose an authentication app, you will need to download an authenticator app (such as Google Authenticator or Authy) on your mobile device and scan the QR code displayed on the screen. If you choose to receive a text message, you will need to enter your phone number and wait for the code to be sent to you.
6. After verifying your account with either the authentication app or the text message, Discord will generate backup codes that you can use to access your account in case you lose access to your verification method. Be sure to store these codes in a safe place!

That's it! Your account should now be protected with two-factor authentication. From now on, when you log in to Discord on a new device or browser, you will need to enter a verification code from your authentication app or from a text message before gaining access to your account.

https://support.discord.com/hc/en-us/articles/219576828-Setting-up-Two-Factor-Authentication

## Screen Sharing

To enable streaming on Discord, you will need to follow these steps:

1. Open Discord on your Mac and log in to your account.
2. Click on the gear icon in the bottom left corner of the Discord window to open User Settings.
3. In User Settings, click on the "Voice & Video" tab on the left-hand side of the window.
4. Scroll down until you see the "Video Settings" section. You should see a "Go Live" option here. If this option is not available, make sure that your Discord client is up to date and that your account is not currently banned or restricted from streaming.
5. Click on the "Go Live" button. This will open the Go Live menu.
6. In the Go Live menu, select the screen or application you want to share with your viewers. You can choose to share your entire screen or a specific application.
7. Once you have selected the screen or application you want to share, click the "Go Live" button at the bottom of the menu. This will start the stream.
8. To end the stream, click the "Stop Streaming" button in the bottom right corner of the Discord window.

That's it! You should now be able to stream your screen or application to your Discord channel. Keep in mind that streaming may cause your computer to slow down, so it's a good idea to close any unnecessary applications before starting a stream.

## Change Username on Discord

To help maintain an organized and consistent member list, please apply the following format if you want to include a title or organization in your username:

*  Option A) If you prefer to use your name: First Name [Organization]
*  Option B) If you prefer not to use your name: Gamertag [Organization]
*  Option C) If you want to show your name or Gamertag but hide your work: First Name/Gamertag

For example, if your current username is AMZN_AmyFinch and you want to change it to adhere to Option A, you would change it to "Amy [Amazon]". If you want to use Option B, you could change it to "Finchy [Developer]". If you want to use Option C, you could change it to "Amy".

Here are the step-by-step instructions to change your username:

1.  Open the Discord app or website and log in to your account.
2.  On the left-hand side, click on the server where you want to change your username.
3.  Find your username in the member list or the chat window, and click on it.
4.  Click on the three dots on the right side of your username, then select "Change Nickname."
5.  Type in your new username according to the guidelines provided above.
6.  Click "Save" to update your username.

Please note that some servers may have specific guidelines for usernames, including limitations on the number of characters or how often you can change your username. Be sure to check the server guidelines or contact an administrator if you have any questions or issues.

For reference, here are some examples of usernames that adhere to the recommended format:

*  Royal OBrien [LF]
*  Finchy [Finch Studio]
*  OBWANDO [Developer]
*  Finchy

For more information, refer to Discord's articles, [How do I change my Username?](https://support.discord.com/hc/en-us/articles/213480948-How-do-I-change-my-Username-) and [Server Nicknames](https://support.discord.com/hc/en-us/articles/219070107-Server-Nicknames).

##  Custom Discord Rich Presence 

Discord-CustomRP is a simple custom Rich Presence manager that allows users to set their own custom "Playing" status on Discord. With this tool, users can set a custom status message and details, including the game they are playing, the current song they are listening to, and much more. The tool is designed to be easy to use, with a simple interface that allows users to quickly customize their status.

Someone would use Discord-CustomRP if they want to customize their Discord status to better reflect their current activity or to add a personal touch to their profile. It's perfect for gamers who want to show off what game they're currently playing or for music lovers who want to share what they're listening to. Additionally, it's a great tool for streamers who want to display their stream information or schedule on their Discord profile. With Discord-CustomRP, users can create a unique and personalized status that showcases their personality and interests.

**Installation:**

1. Make sure you have Node.js installed on your computer.
1. Download or clone the repository from GitHub: https://github.com/custom-rp/customrp.
1. Open the command prompt or terminal and navigate to the downloaded folder.
1. Run npm install to install the required packages.

**Configuration:**

1. Rename the config.example.json file to config.json.
1. Open the config.json file and replace the placeholders with your Discord application's client ID and the custom status message and details you want to display.
1. To get your Discord application's client ID, go to the Discord Developer Portal (https://discord.com/developers/applications) and create a new application or select an existing one. Go to the "General Information" section and copy the client ID.
1. Customize the status message and details in the config.json file. You can use the placeholders provided or enter your own text.
1. Save the config.json file.

**Running the script:**

1. Open the command prompt or terminal and navigate to the downloaded folder.
1. Run node index.js to start the script.
1. Your custom Discord status should now be displayed on your profile.

Note: Keep the command prompt or terminal open while you want the status to be displayed. If you close it, the status will disappear. Also, make sure to update the config.json file whenever you want to change your status message or details.

Alternativly, visit:
https://docs.customrp.xyz/setting-up

## Text Formatting

Here's a comprehensive list of all the formatting options available in Discord:

1. **Bold text**: To make text bold, surround it with two asterisks on both sides like this:<br>
    `**Bold Text**`
2. *Italicized text*: To italicize text, surround it with a single asterisk on both sides like this:<br>
    `*italicized text*`
3. ***Italicized Bold text***: To italicize bold text, surround it with three asterisk on both sides like this:<br> 
    `***italicized bold text***`
4. Underlined text: To underline text, surround it with two underscores on both sides like this:<br>
    `_Underlined Text_`
5. *_Underlined and Italicized Text:_ *To underline and italicize text, add two underscores along with an asterisk on both sides like this:<br>
    `__*Underlined and Italicized Text*__`
6. **_Underlined and bold text_**: To underline and bold text, add two underscores along with two asterisks on both sides like this:<br>
    `__**Underlined and bold text**__`
7. ***_Underlined, italicize and bold text_***: To underline and bold text, add two underscores along with three asterisks on both sides like this:<br>
    `__***Underlined, italicize and bold text***__`
8. __***I want this to be shown in its full glory!***___
    In case you actually *want* to see your underscores or asterisks in a message (like in an emoji, for example), you can use the backslash `\` key to skip markdown formatting and show the text just like it is:<br> 
    `\_\_\*\*\*I want this to be shown in its full glory!\*\*\*\_\_\_`
10. Strikethrough text: To add a strikethrough to text, surround it with two tildes on either side, like this: 
    `~~Strikethrough Text~~`
11. Formatting on International Keyboard Layouts
   - **German:** Shift+[+] (key right of Ü)
   - **Spanish:** Shift+[+] (key right of `^ (Spain) or ´¨ (Latin America))
   - **French (France):** * (key right of ù%)
   - **French (Belgium):** Shift+$ (key right of ^¨)
   - **French (Switzerland):** Shift+3
   - **Italian:** Shift+[+] (key right of èé)
   - **Swedish:** Shift+’ (key right of Ä) 
12. if you want to hide a message you are showing then spoiler would be the way. This could be a way to avoid giving away the main point or a spoiler of a show someone has not seen. You can create spoiler text like so:<br> 
    `|| Spoiler Text ||`
13. For quoting something, there’s a simple “quote/blockquote” tag implemented in Discord. 
     You can do this by simply adding the right-carat character ‘>’:<br> 
    `> text here`<br>
     You can also quote multiple lines by using the triple right-carat ‘>>>’, or by typing out a line with a single quote ‘>’ and then holding SHIFT+ENTER to create a new line within the same quote block. 
14. This is an example of a single line code block: When displaying a line of code, file address or anything that needs a section of code or to stand out and is a single line, add a single backtick on both sides<br>
    `This is an example of a single line code block`
15. To extend this further, if you want to represent multiple lines, then you will add three backticks:
````
```
Stuff
Goes
Here
```
````

## Color Codes

At present, the use of color codes is quite restricted. Although there are workarounds available, they only function properly when viewed on a PC; mobile devices are unable to display colors. The example below shows how the content would appear with and without markdown:

![image](https://user-images.githubusercontent.com/80487462/225159263-55039fe2-3cf7-4575-9ea0-2774c6515076.png)

````
```diff
- Here's some red colored text!
+ Here's some green colored text!
```
```ini
[Here's some blue highlighted text]
```
```fix
Everything is yellow in fix --
No matter the line! Or is this a lie and really Red or maybe its Blue. No one will ever know!
```
```bash
"Here's some nice, light Blue text"
```
````

## Privacy and Notifications

### Privacy

Discord offers a range of privacy settings to help you control who can see your activity and access your personal information on the platform. In the User Settings section, you can adjust your privacy settings to control who can add you as a friend, message you, or view your online status. You can also control who can see your activity status, including whether you're currently online, idle, or offline. Additionally, Discord allows you to control your server privacy settings, including who can view and participate in the server, and who can access specific channels or roles. By customizing your privacy settings on Discord, you can ensure that your personal information remains secure and that you have control over who can see and interact with you on the platform.

#### Desktop Privacy Settings:

1. Open Discord and click on the gear icon next to your username to access User Settings.
1. Navigate to the Privacy & Safety section on the left-hand side of the screen.
1. Here you can customize various privacy settings such as:
      1. Who can add you as a friend: You can choose to allow anyone to add you as a friend, or limit it to just users who share servers with you.
      1. Who can message you: You can choose to allow anyone to message you, or limit it to just friends or server members.
      1. Who can see your online status: You can choose to show your online status to everyone, or limit it to just friends or server members.
      1. Server Privacy Settings: You can choose who can access and participate in the servers you're a member of, and who can access specific channels or roles.
1. Once you've adjusted your settings, be sure to click on the Save Changes button at the bottom of the screen.

#### Mobile Privacy Settings:

1. Open the Discord app on your mobile device.
1. Tap on your profile picture in the bottom-right corner of the screen to access User Settings.
1. Scroll down and tap on the Privacy & Safety option.
1. Here you can customize various privacy settings such as:
      1. Who can add you as a friend: You can choose to allow anyone to add you as a friend, or limit it to just users who share servers with you.
      1. Who can message you: You can choose to allow anyone to message you, or limit it to just friends or server members.
      1. Who can see your online status: You can choose to show your online status to everyone, or limit it to just friends or server members.
      1. Server Privacy Settings: You can choose who can access and participate in the servers you're a member of, and who can access specific channels or roles.
1. Once you've adjusted your settings, be sure to tap on the Save button in the top-right corner of the screen.

By customizing your privacy settings on both desktop and mobile versions of Discord, you can ensure that your personal information remains secure and that you have control over who can see and interact with you on the platform.

### Notifications

Notifications are an essential part of the platform that keeps you up to date with new messages, mentions, and updates in the servers you're a member of. With customizable notification settings for both desktop and mobile versions of Discord, you can choose which notifications you want to receive and how you want to receive them. By adjusting your notification settings, you can ensure that you only receive notifications for the messages and mentions that are most important to you, and that you receive them in a way that's convenient for you. Whether you want to receive notifications for every message or only for direct messages and mentions, Discord's notification settings can help you stay on top of your conversations without being overwhelmed by notifications.

#### Desktop Notification Settings:

1. Open Discord and click on the gear icon next to your username to access User Settings.
1. Navigate to the Notifications section on the left-hand side of the screen.
1. Here you can customize various notification settings such as:
      1. Enable Desktop Notifications: This will allow you to receive notifications from Discord when you're not actively using it. You can choose to receive notifications for all messages or only for direct messages and mentions.
      1. Sound and Vibration: You can choose the sound that plays when you receive a notification, as well as whether or not your device vibrates when you receive a notification.
      1. Server Notification Settings: You can choose which notifications you want to receive for each server you're a member of, such as @mentions, direct messages, or server updates.
      1. Mobile Push Notifications: If you have the Discord app on your mobile device, you can choose to receive push notifications for new messages and mentions. You can also choose how frequently you want to receive push notifications.
1. Once you've adjusted your settings, be sure to click on the Save Changes button at the bottom of the screen.

#### Mobile Notification Settings:

1. Open the Discord app on your mobile device.
1. Tap on your profile picture in the bottom-right corner of the screen to access User Settings.
1. Scroll down and tap on the Notifications option.
1. Here you can customize various notification settings such as:
      1. Push Notifications: You can choose to receive push notifications for new messages and mentions. You can also choose how frequently you want to receive push notifications.
      1. In-App Notifications: You can choose whether or not to receive notifications for new messages and mentions while you're actively using the app.
      1. Sound and Vibration: You can choose the sound that plays when you receive a notification, as well as whether or not your device vibrates when you receive a notification.
      1. Server Notification Settings: You can choose which notifications you want to receive for each server you're a member of, such as @mentions, direct messages, or server updates.
1. Once you've adjusted your settings, be sure to tap on the Save button in the top-right corner of the screen.

By customizing your notification settings on both desktop and mobile versions of Discord, you can ensure that you only receive notifications for the messages and mentions that are most important to you, and that you receive them in a way that's convenient for you.

## Error messages

1. When Creating an event on Discord and shown with "Missing Permissions", ensure that you have 2FA enabled. 

2. If you message a member on Discord and represented with a message saying it could not be sent like so:
```
Your message could not be delivered. This is usually because you don't share a server with the recipient or the recipient is only accepting direct messages from friends. You can see the full list of reasons here:
``` 
This means that you have not added them as a friend. This is normally a setting that's enabled on the other users end to prevent spam. 



Note, if you have any issues or further questions, refer to the [Discord Help Center](https://support.discord.com/hc/en-us).
