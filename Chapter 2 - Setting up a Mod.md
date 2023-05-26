# Introduction

This chapter goes over how to create a mod and enable the Debug Console.

>ℹ️ If you haven’t already, make sure that you have both Visual Studio Code and the Isaac Autocomplete extension installed.

# Creating a Mod

Creating a mod is rather straightforward

## Step 1 - Find the Mods Folder

The first step is looking for your mods folder.

If you own the game on Steam, you can find the mods folder by following these steps:

1. Open the library and search for The Binding of Isaac: Rebirth

2. Right-click on the game and select "Properties"<br> ![image](https://i.imgur.com/A9NUMk6.png)

3. Select the "Local Files" tab and click on "Browse"<br> ![image](https://i.imgur.com/CK82Wd2.png)

4. Inside, you should now see a folder called "mods". If it's not there, create it and make sure it's named "mods" in all lowercase.

## Step 2 - Create a Folder

Inside the mods folder, simply create a new folder. Once the folder is created, give it a name so you won’t forget it later.

## Step 3 - Restart Isaac

If the game is running, exit it out fully first as the game will only detect newly created & installed mods when launching it.

## Step 4 - Check for Your Created Mod

Launch the game again. Once the game loads, go to the Mods menu. In it, you should now see a newly created mod that has the same name as your folder.

Congratulations, you created your very first mod!

# Enabling the Debug Console

The debug console is extremely important for modding as it allows you to reload your mods, give yourself items, and much more.

You can see if it’s already enabled by starting a run and pressing the `~` key. If the debug console appears, you may skip this section. Otherwise, you can enable the debug console by following these steps:

## Step 1 - Close the Game

Make sure the game is completely closed, otherwise, the changes you make to the game's internal settings will be reverted upon launching the game.

## Step 2 - Open options.ini

The `options.ini` stores the game's settings. 

To find it, open file explorer and navigate to `C:\Users\%username%\Documents\My Games`. Then, open the `Binding of Isaac Repentance` folder. Inside, look for the file named `options.ini`.

## Step 3 - Enable Debug Console

Open the `options.ini` file. Inside, look for the line which says `EnableDebugConsole=0`. Change it to `EnableDebugConsole=1`.

After making the change, save your changes and launch the game. If you've done everything correctly, the debug console should now appear when pressing the `~` key in a run.

# Quiz

No questions for this chapter.


