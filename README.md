# Debug Menu Unlocker mod for Security Breach
This is all the code for the Debug Menu Unlocker mod I made for Five Nights At Freddy's: Security Breach

This code needs the Unreal Mod Unlocker for Security Breach, located on the [Discord Server](https://discord.gg/ZpYy823wtB)

If you need any help just ask on the discord server

# Folder layout
`/Content/Mods/DebugMenu` is the main folder where the mod is located. Any work for the mod is done here.

`/Content/Blueprints` is just a shadow folder. We do not package this into the mod as it's only for mimicing the real Blueprints folder located in the game pak file.

# Files
`/Content/Mods/DebugMenu/ModActor` is our main mod entry file. The entire mod is basically right here in one blueprint as the mod is really simple

`/Content/Blueprints/Player/MainGamePC` is nothing more than a player controller to mimic the real player controller used by the game. It contains the function we need to call to open the debug menu, thats it.

# Building
Make sure you have `Allow ChunkID Assignments` turned on in Edit > Editor Preferences > User Interface

Now all you have to do is make sure the files in `/Content/Mods/DebugMenu/` are assigned to a chunk by selecting, right clicking then going to Asset Actions > Assign to Chunk. Make sure the chunk number is greater than 0

Finally just do File > Package Project > Windows (64 Bit)

Just save it to any output folder you want. I just save it in a folder called `PackagedMod` inside of the root of the project

Our output file is `{Folder You Chose}/WindowsNoEditor/fnaf9/Content/Paks/pakchunk1-WindowsNoEditor.pak`

# Installing to the game
Take the output file for the mod then drag and drop it into `{Security Breach Root}/fnaf9/Content/Paks/LogicMods` then rename the file to `DebugMenu.pak` as that is what our folder in `Content/Mods/` is called