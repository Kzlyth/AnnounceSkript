# Announce Skript

Ultimate Announce is a Skript for your Server, to Announce things to everyone at the Server. | Dont use it on Bungee Cord
Made with [SkBee](https://modrinth.com/plugin/skbee)

## 1. How to set it up?
1. Go to your Plugins folder
2. Search for the folder called "Skript"
3. Go to the "scripts" folder
4. Download the .sk file from this Github repo
5. Place it in the "scripts" folder
6. Go to your game and write "/sk reload scripts"

## 2. What about the Commands?
1. The command is /announce <color> <message> <bold?> [message2] || NOTE: when you put in the 2nd message, you can use Color Codes. In the other you cannot
2. The permission is: announce.send

## 3. How to add colors?
In the Code you will find two important Code blocks:
```
set {_color} to ""
        if arg 1 is "Blue":
            set {_color} to "<##4287f5>"
        else if arg 1 is "Green":
            set {_color} to "<##42f56c>"
        else if arg 1 is "Red":
            set {_color} to "<##cc1439>"
        else if arg 1 is "White":
            set {_color} to "<##FFFFFF>"
        else:
            send "&cPlease select a given color: Blue, Green oder Red"
            stop
```

and:
```
on tab complete of "/announce":
    set tab completions for position 1 to "Blue" and "Green" and "Red" and "White"
    set tab completions for position 3 to "true" and "false"
```

If you want to add a color you will have to add 2 Lines in the First Block. So if you wanted to add for example "Yellow" you will need to add:
```
else if arg 1 is "Yellow":
            set {_color} to "<##e6c910>"
```
The color must be formatted like this: <#{hexcode}> | So it does have 2 Hashtags!

**IMPORTANT** is that the following part comes at last:
```
          else:
            send "&cPlease select a given color: Blue, Green oder Red"
            stop
```

To add the Color to the **Tab Completion** you will add it to the **2nd Codeblock**. To be exact you will only modify this line:
```
set tab completions for position 1 to "Blue" and "Green" and "Red" and "White"
```

the only thing you will have to do is put an "and {color}" at the End. For example if you called your Color "Yellow" as I did above, your Line would look like this:
```
set tab completions for position 1 to "Blue" and "Green" and "Red" and "White" and "Yellow"
```


You can get support here: https://discord.gg/jyrjcrGMkw
Check out my Portfolio: https://kzlyth.netlify.app
