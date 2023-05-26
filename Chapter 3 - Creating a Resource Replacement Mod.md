# Introduction

This chapter goes over how to create a resource replacement mod.

A resource replacement mod is a mod that replaces one of the game's assets. 

# Replacing a Sprite

The process of replacing one of the game's sprites is very simple. In this example, we will go over how to replace the collectible sprite for the Sad Onion.

## Step 1 - Create your Sprite

The first step is quite obvious: Create your sprite.

If you don't sprite or don't want to, you can simply download an [already made sprite](https://i.imgur.com/S3jHjdt.png), made by Bajongo.

>⚠️ When saving your sprite, you **MUST** save it as a `.png` file with a bit-depth of 32 bits. If you don't do this, your sprite will not properly display in-game.

## Step 2 - Find the Original Sprite Path

The next step is to find the path of the original Sad Onion sprite.

To find the path, you need to first open the game's directory.

>ℹ️ If you forgot how to open the game's directory, refer back to [Chapter 2](https://github.com/4grabs/Isaac-Modding-Tutorial/blob/main/Chapter%202%20-%20Setting%20up%20a%20Mod.md)

Inside, you will see two folders named "resources" and "resources-dlc3" respectively. These folders contain all the game's sprites, animations, sound effects, and music. 

Assets under the "resources" folder are for content that was made before Repentance was released, while assets under the "resources-dlc3" folder contain assets made for Repentance. Since the Sad Onion was made before Repentance, it is found inside the "resources" folder.

To find the location of the Sad Onion, navigate to `/resources/gfx/items/collectibles/` 

Inside, you will see the sprite for Sad Onion, which should be named "collectibles_001_thesadonion.png". Keep note of the location of the sprite and its name.

## Step 3 - Mirror the Path in your Mod

The next step is to mirror the path of the Sad Onion sprite in your mod.

First, open up your mod folder. You will then need to create a series of folders that exactly match the structure of the folders in the game's directory. This means:

1. Create a folder and name it "resources"
2. Inside the "resources" folder, create a folder named "gfx"
3. Inside the "gfx" folder, create a folder named "items"
4. Inside the "items" folder, create a folder named "collectibles"
5. Place your created sprite inside of the new "collectibles" folder and name the sprite "collectibles_001_thesadonion.png"

As you may have noticed, the folders you created exactly matches up with the game's folders and the location and name of the new Sad Onion sprite match up with the game's. 

## Step 4 - Test It

If the game is running, exit it out fully and restart it. You can also go to the mods menu to disable and reenable the mod, although it tends to be unstable and results in the game crashing.

Start a new run and open up the debug console. From there, type in `spawn 5.100.1` and press enter. You should see your brand-new sprite.

>ℹ️ If you do not see your new sprite, double-check to see if the folders you created in your mod match up with the game's as well as the location of your sprite. Make sure everything is also spelled correctly (do note that it's case-sensitive). If you did everything right, another mod may be overriding your sprite, so you may need to disable other mods.

# Conclusion

Congratulations, you learned how to replace sprites! If you want to replace sprites other than collectibles, the process is going to be the exact same. Just make sure that the folders you create in your mod match up with the game's folders, including the name of your new sprite.

?The process of replacing music and sound effects is also mostly the same, although there are a few differences:

* Sound effects need to be saved with a `.wav` format and need to be 32-bit just like images. If it's not 32-bit, the sound will sound like loud static in-game which will definitely blow out your ears!
* Music needs to be saved with a `.ogg` format.

# Quiz

This is more of an exercise rather than a quiz. Using the exact same sprite (or a new one if you want), try to replace the C Section collectible sprite. To test to see if it works, you can spawn it by typing `spawn 5.100.678` in the debug console.

<details>
  <summary>Hint #1</summary>
    C Section was added in Repentance, so you will need to look in the "resources-dlc3" folder and create one with the same name in your mod.
</details>
