# Discord Permission Guide 

- [Discord Permission Guide](#discord-permission-guide)
    + [@Everyone Tag](#everyone-tag)
    + [Reward Tiers](#reward-tiers)
    + [Bots](#bots)
    + [Novelty Roles](#novelty-roles)
      - [How to Create a Novelty Role](#how-to-create-a-novelty-role)
      - [Add a Novelty Role to channels](#add-a-novelty-role-to-channels)
    + [Punishment Roles](#punishment-roles)
    + [Emoji on Roles](#emoji-on-roles)

This manual will establish a set of guidelines for best practices when configuring a server that members can adhere to. It encompasses determining access privileges, defining standard roles and their naming conventions.

It is crucial for new members who join the discord server to understand these roles and who holds them, as they are typically the first things they encounter. Here are some general guidelines:


* **Create separate roles for different levels of access:
    **It's a good idea to create different roles with varying levels of permissions based on the responsibilities of different members. For example, you may want to have a role for moderators who have the ability to manage channels, kick/ban members, and mute other users. You may also want to have a role for regular members who have limited permissions.
* **Assign roles based on responsibilities:
    **Once you have created roles, it's important to assign them to members based on their responsibilities. This will ensure that members have the appropriate permissions to carry out their tasks. You can assign roles by going to Server Settings > Roles.
* **Use channel-specific permissions:
    **You can also set channel-specific permissions to give members access to specific channels. For example, you may want to create a channel for moderators where only members with the moderator role have access.
* **Use the "@everyone" role sparingly:
    **The "@everyone" role gives all members of the server the same permissions. It's best to use this role sparingly and only give it the minimum necessary permissions. This will prevent members from accidentally or intentionally abusing their permissions.
* **Regularly review and update permissions:
    **It's important to regularly review and update permissions to ensure that members have the appropriate level of access. For example, you may want to remove a member's moderator role if they are no longer actively moderating the server.


The recommended permission structure for a Discord server is one that is well-organized, clearly defined, and regularly reviewed and updated to ensure the smooth operation of the server.

* **Owner:
    **The server owner, who has complete control over the server's settings and permissions, is typically the person who created the server. However, it's important to note that it's recommended to not show the owner role to everyone and to share the responsibilities with another trusted member who has the "Administrator" role on the server. This helps to prevent a single individual from having complete control of the server in case something happens to the owner. 
* **Admin: 
    **Administrators are tasked with overseeing the server and enforcing its regulations. They are granted broad permissions, including the authority to supervise channels, remove/ban members, and silence other users.
* **Moderator:
    **Moderators are in charge of ensuring that the server rules are followed and that chat activity is monitored. They are given permissions to remove messages, eject members, and silence other users. 
* **Helper:
    **Helpers are present to offer assistance to members with common inquiries, guide individuals to appropriate resources, and contribute to general discussions. They often serve as intermediaries between the server's leadership and the rest of the community, forwarding relevant information to the appropriate parties.
* **Member:
    **Members are the default role for all users who have joined the server. They have restricted permissions and are unable to perform any administrative functions. 
* **Bot:
    **If you have any bots on your server, you may want to create a specific role for them. This will allow you to give them the necessary permissions to perform their functions without giving them access to sensitive server settings.


Remember, these roles are just suggestions, and the specific roles and permissions needed for your server will depend on its purpose and size. It's important to regularly review and adjust your roles and permissions to ensure that they are appropriate for your server's needs.
 
In the member list, it's recommended to distinguish Admins, Moderators, and Helpers from the rest of the community by assigning them a unique color. Additionally, you can further customize this by assigning an emoji that represents each specific role. This makes it easier for members to identify who they can turn to for help or support within the community. 

Here is a table based on the standard permissions for the roles listed above:

|Permission	|Owner	|Admin	|Moderator	|Helper	|Member	|Bot	|
|---	|---	|---	|---	|---	|---	|---	|
|Manage server	|✔️	|✔️	|	|	|	|	|
|---	|---	|---	|---	|---	|---	|---	|
|Manage roles	|✔️	|✔️	|	|	|	|	|
|Manage channels	|✔️	|✔️	|✔️	|	|	|	|
|Kick members	|✔️	|✔️	|✔️	|	|	|	|
|Ban members	|✔️	|✔️	|✔️	|	|	|	|
|Mute members	|✔️	|✔️	|✔️	|	|	|	|
|Remove messages	|✔️	|✔️	|✔️	|	|	|	|
|Manage emojis	|✔️	|✔️	|	|	|	|	|
|Manage webhooks	|✔️	|✔️	|	|	|	|	|
|View audit log	|✔️	|✔️	|✔️	|	|	|	|
|View server insights	|✔️	|✔️	|	|	|	|	|
|Manage server boosts	|✔️	|✔️	|	|	|	|	|
|Create instant invite	|✔️	|✔️	|✔️	|	|	|	|
|Change nickname	|✔️	|✔️	|✔️	|✔️	|✔️	|	|
|Manage nicknames	|✔️	|✔️	|✔️	|	|	|	|
|Manage emojis	|✔️	|✔️	|	|	|	|	|
|Mention everyone	|✔️	|✔️	|✔️	|	|	|	|
|Use external emojis	|✔️	|✔️	|✔️	|	|	|	|
|View channels	|✔️	|✔️	|✔️	|✔️	|✔️	|✔️	|
|Send messages	|✔️	|✔️	|✔️	|✔️	|✔️	|✔️	|
|Embed links	|✔️	|✔️	|✔️	|✔️	|✔️	|✔️	|
|Attach files	|✔️	|✔️	|✔️	|✔️	|✔️	|✔️	|
|Read message history	|✔️	|✔️	|✔️	|✔️	|✔️	|✔️	|
|Mention roles	|✔️	|✔️	|✔️	|✔️	|✔️	|✔️	|
|Add reactions	|✔️	|✔️	|✔️	|✔️	|✔️	|✔️	|
|Connect to voice	|✔️	|✔️	|✔️	|✔️	|✔️	|✔️	|
|Speak in voice	|✔️	|✔️	|✔️	|✔️	|✔️	|✔️	|
|Video in voice	|✔️	|✔️	|✔️	|✔️	|✔️	|✔️	|
|Move members	|✔️	|✔️	|✔️	|	|	|	|

*Note: This table is a general guideline and specific permission settings may vary depending on the needs and requirements of each individual server.
Note: Some Bots will require additional permissions to handle some of the moderation of the server.* 

### @Everyone Tag

Tagging @everyone in a Discord server can be useful for making important announcements that need to be seen by all members. However, it can also lead to spam and unnecessary pings, especially if misused. That's why it's recommended to restrict the ability to tag @everyone to only the Admin role, as they are typically responsible for server management and can ensure that the feature is used appropriately.

To restrict the ability to tag @everyone, you can edit the server's roles and permissions settings. Under the "Server Settings" menu, select the "Roles" tab, and then click on the role you want to modify (excluding the Admin role in this case). From there, you can toggle the "Mention @everyone, @here, and All Roles" permission off to prevent members with that role from using the feature.

It's important to note that while limiting the ability to tag @everyone can help reduce spam, it can also make it more difficult to communicate important information to all members of the server. As such, it's important to strike a balance between ensuring effective communication and preventing unnecessary pings.

### Reward Tiers

Rewards tiers in Discord can be structured in various ways depending on the server's purpose and goals. The concept typically involves dividing members into different levels or tiers based on their level of engagement, activity, or contribution to the community. These tiers are then used to determine what rewards or perks members receive.

It's important to note that the specific rewards and criteria for each tier may vary depending on the server. However, here are some general examples of how Discord reward tiers can be structured:

1. Tier 1: Beginner - This tier typically includes new or inactive members. They may have limited access to certain channels and features, and may not be able to participate in certain events or activities.
2. Tier 2: Regular - This tier includes members who are more active and engaged in the community. They may have access to additional channels, features, or roles, and may be eligible for rewards such as custom emotes or badges.
3. Tier 3: Elite - This tier includes the most active and dedicated members of the community. They may have access to exclusive channels or events, receive special roles or titles, and may be eligible for rewards such as giveaways or access to premium features.

It's important to ensure that the criteria for each tier is clear and achievable, and that the rewards offered are meaningful and valuable to the community. Additionally, it's important to regularly review and adjust the reward tiers as the community evolves and grows.

### Bots

Having too many bots on a Discord server can lead to clutter and confusion. Each bot typically has its own set of commands and functions, which can overlap or conflict with other bots. Additionally, bots can generate spam messages that can make it harder for users to find important information or engage in meaningful conversations.

To avoid these issues, it's recommended to carefully consider the number and type of bots that are added to the server. Look for bots that offer the most useful commands and features needed for the server's purpose and goals. For example, if the server is focused on gaming, a bot that provides a leveling system or game-related commands may be useful.

Popular bots like Mee6 and StatBot can offer a wide range of functionality, including moderation tools, custom commands, and more. However, it's important to assess whether each feature is necessary for the server and whether it will be used by members. Adding too many features or commands can be overwhelming and confusing for members, and can also contribute to spam.

In general, it's a good idea to limit the number of bots on the server to just a few essential ones. This can help keep the server clean and organized, reduce conflicts or spam, and improve the overall user experience.

### Novelty Roles

Novelty roles can be a valuable addition to a Discord server, as they allow members to showcase their interests and skills in a fun and interactive way. By enabling members to self-assign these roles, it can also create a sense of ownership and engagement with the server.

Novelty roles can be used to represent a wide range of interests, including favorite TV shows, movies, music genres, hobbies, and more. They can also be used to identify different skill levels or areas of expertise, such as programming languages, design tools, or operating systems.

In addition to adding a badge or color to a user's profile, novelty roles can also be used to provide access to specific channels or features within the server. For example, a role based on a particular game may grant access to a channel dedicated to discussing that game, while a role related to a certain skill may allow members to participate in a workshop or training session.

While novelty roles can be a fun and engaging way for members to express themselves, it's important to ensure that they do not detract from the overall purpose and functionality of the server. It's also important to moderate the use of these roles to prevent excessive or inappropriate use. For example, server owners may want to limit the number of novelty roles available, or restrict them to specific categories or topics. They may also want to review and approve each new role before it is added to the server.

Overall, novelty roles can be a valuable tool for creating a more engaging and interactive Discord server, as long as they are used thoughtfully and in moderation.


#### How to Create a Novelty Role

Creating a novelty role in Discord is a simple process that can be done in a few easy steps:

1. Open your Discord server and navigate to the "Roles" section in the Server Settings.
2. Click on the "Create Role" button to create a new role.
3. Name the role based on the category or interest that it represents. For example, if you want to create a role for gamers, you could name it "Gamer" or "Gaming Enthusiast."
4. Choose a color for the role by selecting one of the available options, or by inputting a custom HEX color code.
5. Under the "Permissions" tab, you can customize the permissions for the role based on the specific features and channels that you want to grant access to. For novelty roles, you may want to limit the permissions to basic chat and voice features, without granting administrative or moderation privileges.
6. Under the "Members" tab, you can assign the role to individual members, or allow them to self-assign the role by enabling the "Self-Assignable" option.
7. Save the role and make sure it is positioned appropriately in the hierarchy of roles in your server. This will determine the order of the role's appearance in the member list and the permissions hierarchy.

Once the novelty role has been created and positioned, members can easily self-assign the role by right-clicking on their name in the member list and selecting "Roles." From there, they can select the appropriate novelty role based on their interests or skills.

#### Add a Novelty Role to channels

Adding channels to a novelty role in Discord is a great way to provide members with specific channels for their interests or skills. Here's how to do it:

1. Open your Discord server and navigate to the "Roles" section in the Server Settings.
2. Click on the "Create Role" button to create a new role, or select an existing role that you want to add channels to.
3. Under the "Permissions" tab, scroll down to the "Channel Permissions" section and click the "+" button to add a new channel.
4. Select the channel that you want to add to the role from the drop-down menu.
5. Customize the permissions for the channel by toggling the permissions on or off. For example, you may want to allow members with the novelty role to send messages and attach files, but not to manage messages or channels.
6. Repeat the process for each channel that you want to add to the role.
7. Save the changes and make sure that the novelty role is positioned correctly in the hierarchy of roles. This will determine the order of the role's appearance in the member list and the permissions hierarchy.

Once the channels have been added to the novelty role, members with that role will be able to access those channels and participate in conversations with other members who share their interests or skills. You can also use the "Manage Channels" permission to create new channels specifically for the novelty role, and to adjust the permissions for existing channels as needed.

### Punishment Roles

Punishment roles can be useful in Discord servers where members frequently violate server rules or engage in behavior that is disruptive to the community. Rather than simply banning or kicking members, punishment roles allow them to continue to participate in the server while their behavior is being monitored or restricted.

For example, a punishment role may limit a member's ability to post messages or participate in voice chats, or it may restrict their access to certain channels or features of the server. The exact limitations and duration of the punishment can vary depending on the severity of the offense and the server's policies.

One benefit of using punishment roles is that they allow the server moderators to have more control over member behavior without completely removing members from the community. This can be especially helpful in cases where a member has made a mistake or is in the process of correcting their behavior, but still needs some guidance or monitoring.

It's important to note, however, that punishment roles should be used judiciously and fairly, and should always be accompanied by clear communication with the member about why the punishment is being imposed and how long it will last. Additionally, it's important to consider the potential impact that punishment roles can have on the member's experience in the server, as well as the potential impact on the overall community dynamics.

To create a punishment role in Discord, you will first need to have the appropriate permissions. Typically, this would be the server owner or a role with the "Manage Roles" permission. Here's how to create a punishment role:

1. Go to the server settings by clicking on the server name in the top left corner of the Discord window.
2. Click on the "Roles" tab in the server settings.
3. Click the "+" button to add a new role.
4. Name the role something like "Punished" or "Muted."
5. Configure the role's permissions by toggling the appropriate options on or off. For example, you may want to remove the member's ability to post messages, join voice channels, or send direct messages.
6. Once you have configured the role to your satisfaction, click "Save Changes" to create the role.

To use the punishment role, you will need to assign it to the member who has violated server rules or engaged in disruptive behavior. Here's how to do that:

1. Right-click on the member's name in the server.
2. Click "Roles" in the menu that appears.
3. Find the punishment role you created and click on it to assign it to the member.

Once the punishment role has been assigned, the member's permissions will be restricted according to the settings you configured when you created the role. You can remove the punishment role when the member's punishment period has ended by following the same steps and unassigning the role from the member. In some cases a Bot can help automate this process. It's important to communicate clearly with the member about why the punishment is being imposed and how long it will last. Additionally, be sure to follow your server's policies and guidelines when using punishment roles.


### Emoji on Roles

By adding an emoji to a role in Discord, you can make it easier to distinguish staff members from other users on the server. Typically, servers use badges that are related to moderators or staff members. However, you can add any emoji you like to a role. Here are the steps to follow in order to add an emoji to a role in Discord:


1. Open Discord and navigate to the server you want to modify.
2. Click on the server name to open the drop-down menu and select "Server Settings."
3. In the "Server Settings" menu, click on the "Roles" option located in the left-hand side panel.
4. Find the role to which you want to add an emoji and click on it to edit the role's settings.
5. Scroll down to the "Emoji" section of the role settings.
6. Click on the plus sign (+) next to the "Emoji" section to add a new emoji to the role.
7. Choose the desired emoji from the list or upload a new one.
8. Click on "Save Changes" to apply the new emoji to the role.


Once you've completed these steps, the chosen emoji will be associated with the selected role and will appear next to the role's name in the server member list.


#### Updated March 2023
