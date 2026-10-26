# EaglerModpack 1.12.2

### A Modern Implementation Of The Forge Modloader In Eaglercraft 1.12.2 Accompanied By Some Ported Mods

Created By @radmanplays, With Support From The Community

> [!WARNING]
> This Project Is Not Affiliated With LAX1DUDE's Eaglercraft 1.6.4 Modpack. EaglerModpack 1.12.2 Is A Separate Project Targeting Minecraft 1.12.2.

## Technical Features

- **Full Forge Modloader Ported To 1.12.2**
- **Key Mixins Built Into The Modloader (No Need For MixinBooter Or Other Projects)**
- **Advanced Crash Logs For Better Bug Fixing**
- **Native Singleplayer And Relay Support To Make Deticated Servers Optional**
- **Lots Of Built-In Toggleable Mods Using The EaglerXOpts**

## Included Mods (as of 10/21/26)

- **Create Legacy [link To Project Here](https://www.curseforge.com/minecraft/mc-mods/create-legacy)**
- **JEI (Just Enough Items) [Link To Project Here](https://www.curseforge.com/minecraft/mc-mods/jei)**
- **HWYLA (Here's What You're Looking At) [Link To Project Here](https://www.curseforge.com/minecraft/mc-mods/hwyla)**

## Downloads
Visit The [Releases](https://github.com/radmanplays/Eaglermodpack/releases) Page To Download The Latest WASM Build. Updates Are Released Periodically And Do Not Follow A Fixed Schedule.

## How To Enable/Disable Mods?
You can add a EaglercraftXOpt array at the start of the html named "mods" and put the modid of the mod(s) you'd like to be loaded:

```javascript
window.eaglercraftXOpts = {
    container: "game_frame",
    worldsDB: "worlds",
    relays: [
        { addr: "wss://relay.deev.is/", comment: "lax1dude relay #1", primary: relayId == 0 },
        { addr: "wss://relay.lax1dude.net/", comment: "lax1dude relay #2", primary: relayId == 1 },
        { addr: "wss://relay.shhnowisnottheti.me/", comment: "ayunami relay #1", primary: relayId == 2 }
    ],
    mods: ["melonlib", "create", "jei", "waila"]
};
```
if the array does not exist(which it doesn't by default) the game will automatically loads every mod

## Dedicated Server Setup
EaglerModpack 1.12.2 Is One Of The Few Eaglercraft FML (Forge) Implementations To Have Full Server Support
Using Compatible Programs And Mods Such As Minecraft FML (Forge) Server, Velocity, EaglerXServer, And Appropriate EaglerBridge JAR Mods

### Required Prerequisites
- **Velocity JAR**
- **Minecraft FML (Forge) Server**
- **EaglerXServer**
- **Appropriate EaglerBridge JAR Mods**

### First Step, Make A Minecraft FML (Forge) Server
- **Download And Make A 1.12.2 Minecraft Minecraft FML (Forge) Server [Link To Best Fit Here](https://files.minecraftforge.net/net/minecraftforge/forge/index_1.12.2.html).**
- **Set Server To Offline Mode**
- **Add Desired Mods Enabled On Client (EaglerXOpts) (Ex. Create Legacy, JEI) (Incompat Ex. HWYLA)**
- **Add eaglerbridge-forge-2.0.0.jar (Located In EaglerBridge Folder) In Your Forge Mod List**
- **Change Port To Something Different From 25565 (Ex. 25566)**

### Step 2, Make A Velocity Proxy
- **Download The Latest Velocity Server [Link To Downloads Page Here](https://papermc.io/downloads/velocity)**
- **Add EaglerXServer [Link To That Here](https://github.com/lax1dude/eaglerxserver) And Add The Base Mod To Your Mods Folder (You Can Add Optional Mods)**
- **Add eaglerbridge-velocity-2.0.0.jar (Located In EaglerBridge Folder) To Enable EaglerModpack 1.12.2 FML Protocol Transfer Support**
- **Go Inside The Main Toml And Make Sure 25566 Is a Primary Lobby Server So Velocity Connects**
- **Make Velocity Offline Mode**

<!--
### Recommended Mods For Forge Server
- **AuthMeReloaded** (Login Manager To Prevent People Who Want To Sign In To Accounts They Dont Own
- **LuckPerms** (Permissions Manager)
- **EssentialsX** (Lots Of Server Management Features)
-->

> [!IMPORTANT]
> If You Want MelonLib In Your Server For Create Legacy Support You Need A Companion Mod In Velocity Called **eaglerbridge-melonlib-2.0.0.jar** (Located In EaglerBridge Folder) To Allow MelonLib Translation

> [!CAUTION]
> It Is Not Reccomended To Use The Older EaglerXBungee Or EaglerXVelocity Server Implementation Methods As They Break Some Mechanics And Are Deprecated And Abandoned
>
> Offline Mode Servers Are Not Secured Please Respond To That Accordingly

## Where To Report Bugs?
### Fallen And Can't Get Up? <:

Please report it in the #bug-reports channel on our Discord server rather than opening an issue in this GitHub repository. This repository is not actively monitored for bug reports.
https://discord.gg/TwEUqtQQnF

### When Reporting A Bug, Please Include:

What Happened And What You Expected To Happen.
Steps To Reproduce The Issue.
Your EaglerModpack Version (Ex. R0).
Any Relevant Crash Logs Or Error Messages From The Wasm Interpreter.

## Want To Join Our Community?
Head To https://discord.gg/TwEUqtQQnF
- **For General Channels**
- **Mod Suggestions**
- **Bug Reports**
- **Other Clients Using This New FML (Forge) Project And Much More!**

## Credits

### Gson
This Project Uses A Modified Gson Build Built Specificly To Work In The EaglercraftX Workspace, A Java Library For Working With JSON.

- Original project: Google Gson
- Original authors: Google and Gson contributors
- Porter: LAX1DUDE
- Source code: Eagler-dev-kit Gson directory [Link To That Here](https://github.com/radmanplays/Eagler-dev-kit/tree/main/com/google/gson)
- Gson is used for JSON parsing and serialization.

Please refer to the original project's license for copyright and redistribution terms.

## Other Information
This Project Is Not Open Source Just Yet.

BungeeCord Is Neither Recommended Nor Supported

Thank You @BendieGames For Making The FML Server Compatibility Mods

just play you eagler <:
