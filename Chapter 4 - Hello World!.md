# Introduction

This chapter goes over how to print text to the debug console and reloading mods.

# Introduction

Lua is a lightweight programming language that the Isaac modding API uses. Fortunately, compared to many coding languages out there, Lua is considered to be one of the easiest to learn.

# Creating the Lua File

Inside your mod folder, create a file and name it `main.lua`.

A Lua file is where all of the coding magic happens. `main.lua` is, as the name implies, the main Lua file for the mod and is ran when the game starts. Every mod that requires coding will need a `main.lua` file as giving it any other name will cause it to not run.

# Opening the Mod in an IDE

After creating `main.lua`, you will need to open the mod's folder in your IDE. If you selected Visual Studio Code, you can open the mod by doing the following steps:

1. Go to the top left corner of the window and click on "File"
2. Click on "Open Folder"
3. Look for the folder of your mod and select it
4. Click on "Select Folder"

Afterwards, you should see something like this

![](https://i.imgur.com/EAwGyj1.png)

>ℹ️ You might see other files created such as `.vscode` and `.luarc.json` (if you have the Autofill extension). You can ignore them for now.

Select the `main.lua` file on the side and the IDE will open it. You can now get started with coding!

# Hello World!

It's time to write our first snippet of code. Paste the following snippet inside of the file:

```lua
print("Hello World!")
```

Do not worry if you do not understand what this does yet, we will go over it shortly.

After pasting it in, save the file by pressing the `ctrl` and `s` keys at the same time or by going to `File > Save`.

# Testing It

To test if it works, launch the game and start a new run. Open the debug console and you should see the following

![image](https://github.com/4grabs/Isaac-Modding-Tutorial/assets/88222543/41167f8e-ac0c-4d3a-a2ac-91d85b0ff580)

Congratulations, you ran your first piece of code!

>ℹ️ If you do not see the text, make sure that you saved the changes you made on `main.lua`. If there is a lot of text being printed out by other mods you have enabled, you can scroll through the console by pressing the `Pg Up` and `Pg Down` keys. If you still can't see the text, make sure you named your Lua file `main`.

# A Look at Print

`print` is one of the many built-in functions that Lua offers. As its name implies, `print` simply prints out text to the debug console, which can be quite useful when debugging your mods. You can use this function to print out almost anything.

# Changing your Lua Script & Reloading your Mod

When you add or change a resource such as sprites, you need to restart the game so it can be detected. Fortunately, this is not the case with Lua files.

To demonstrate this, open `main.lua` back up and change the "Hello World!" text to anything of your liking.

>⚠️ Make sure you keep in the two quotation marks! If you remove them or put your text outside of them, your mod will error. We will go over why this is required in a later chapter.

Once you make these changes, save your file and then open up the debug console. Inside, type `luamod` followed by the name of your mod's folder. For example, if you named the folder "Tutorial Mod", you would need to type in `luamod Tutorial Mod`. After running the command, you will see the new text appear in the debug console.

`luamod` is a very useful command when coding your mod as it reloads your mod and allows your Lua files to run once again.

# How Code is Ran

When the game runs your code, it will start running it from top to bottom. For example, if your code looked like this:

```lua
print("Hello World!")
print("Goodbye World!")
```

It would print out "Hello World!" first and then "Goodbye World!"

# Conclusion

Congratulations, you learned how to print text to the console. The next few chapters will go over all of the important stuff that Lua offers. After that, we can finally get into modding new content for the game.

# Quiz

Edit `main.lua` so that it prints out the phrases in order:

1. "Repentogon sweep begins now"
2. "I am a pro modder"

<details>
  <summary>Solution</summary>
  
  ```lua
  print("Repentogon sweep begins now")
  print("I am pro modder")
  ```
  
</details>
