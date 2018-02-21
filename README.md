Track explosions (C4, Satchel Charges, and Rockets) in the event that an admin needs to investigate a raid for suspicious activity. Detailed reports include an on-screen drawing of arrows from where the explosive was thrown to the entity the explosive detonated on and the attacker's name.

Each explosion is colour coded to represent the attacker's name in chat and on screen for ease of reading. If the number of explosions exceeds the configured amount then X's will be drawn in place of the attacker's name to reduce clutter.

A config is available for server owners to setup the plugin to their liking. Includes support for Discord, DiscordMessages, Popup Notifications and Slack plugins.

## Dependencies

### Optional

- [Slack](http://oxidemod.org/plugins/slack.1952/)
- [Discord](http://oxidemod.org/plugins/discord.2149/)
- [DiscordMessages](https://umod.org/plugins/discordmessages)
- [Popup Notifications](http://oxidemod.org/plugins/popup-notifications.1252/)

## Chat Commands
An authLevel of 1 is required
- **/px** -- will show all explosions in range (default 50m)
- **/px [distance]** -- to show explosions from a further distance.
- **/px help** -- Help.

## Permissions
- `raidtracker.see` -- Players can see explosion broadcasts or popups if enabled.
- `raidtracker.use` -- Players with the permission cannot see their own explosions. Command: **/px**

## Configuration
```json
Additional Tracking:
    Track Beancan Grenades -> false
    Track F1 Grenades -> false

Discord:
    Send Notifications -> false -> Send explosion messages to configured channel in the Discord plugin

DiscordMessages:
    Message - Embed Color (DECIMAL): 3329330
    Message - Webhook URL -> https://support.discordapp.com/hc/en-us/articles/228383668-Intro-to-Webhooks

Players:
    Allow DDRAW -> false -> Facepunch removed access to DDRAW for players. This setting temporarily gives the player admin access to use DDRAW long enough to draw on their screen all explosions affecting the player by using the /px command.
    Command Name -> px -> The command players must use to access the plugin. This limits the amount of information sent to the player based on entities which they own, instead of all entities.
    Limit Command Once Every X Seconds -> 60 seconds -> The number in seconds a player must wait before using the command for DDRAW.
    Permission Name -> raidtracker.use -> Players must have this permission to use the /px command. This permission will not exist unless Allow DDRAW or Show Explosions is true.
    Show Explosions -> false -> Enables or disables players from using this plugin.
    Show Explosions Within X Meters -> 50.0

PopupNotifications:
    Duration -> 0.0 -> The duration in which popup's are shown. Setting this value to 0.0 will use the default value of 8 seconds from the PopupNotifications plugin.
    Use Popups -> false

Settings:
    Allow Manual Deletions and Wipe of Explosion Data -> true -> Allow command line access to alter or wipe the database.
    Apply Retroactive Deletion Dates When Days Before Delete Is Changed -> true
    Apply Retroactive Deletion Dates When Days To Delete Is Changed" -> true
    Apply Retroactive Deletion Dates When No Date Is Set -> true
    Auth Level -> 1 -> The required auth level for admins to use the plugin
    Authorized List": [] -> Only steam64 ID's in this list will be able to use this plugin if configured
    Automatically Delete Each Explosion X Days After Being Logged -> 7
    Color By Weapon Type Instead Of By Player Name -> false
    Delete Radius -> 50
    Draw Arrows -> true
    Explosions Command -> x -> Admin command to access plugin
    Max Explosion Messages To Player -> 10
    Max Names To Draw -> 25 -> The amount of names to draw on screen. Configuring a limit helps prevent names from overlapping one another.
    Output Detailed Explosion Messages To Client Console -> true -> Print additional information to the client's console
    Print Explosions To Server Console -> true - Show explosions in server console
    Print Milliseconds Taken To Track Explosives In Server Console -> false -> Show the amount of time taken to track each explosion
    Show Explosion Messages To Player -> true -> Allow players to see detailed explosion messages if Players -> Show Explosions is true
    Show Explosions Within X Meters -> 50
    Time In Seconds To Draw Explosions -> 60.0
    Wipe Data When Server Is Wiped (Recommended) -> true -> Wipe database when server is wiped

Slack:
    Channel -> general
    Message Style (FancyMessage, SimpleMessage, Message, TicketMessage) -> FancyMessage
    Send Notifications -> false -> Use Slack plugin
 
```

## Video
[![Raid Tracker](https://i.ytimg.com/vi/6Tf2rGWEemU/0.jpg)](http://www.youtube.com/watch?v=6Tf2rGWEemU)
