# Introduction

This chapter goes over the following:

* The motivation behind the guidebook 
* An overview of what the guidebook covers
* Legend
* Required Tools
* Frequently Asked Questions
* Useful Resources

# Motivation

Unlike a lot of games, getting into Isaac modding is quite difficult. However, the difficulty doesn’t come from the coding aspect but rather the lack of resources geared towards those who wants to get into modding.

Most modding tutorials were made prior to Repentance coming out. While the core concepts of said tutorials do remain the same for the most part, the code and practices taught hold up poorly due to the numerous changes made to the modding API with the release of the Repentance DLC. As a result of this, there are very few tutorials for Repentance modding. 

With this guidebook, the goal is to teach you how to mod the game in the simplest yet effective way. By the end of this, you should (hopefully) be able to start creating mods on your own!

# Overview

This guidebook goes over almost everything pertaining to Isaac modding. This includes replacing sprites, coding items, coding enemies, and much more.

Contrary to the name, this guidebook is more of a technical one. It does not teach you how to sprite or how to animate. If you were planning on doing them only, this guidebook is not for you. The guidebook is split into multiple different chapters, with each chapter split into multiple different sections.

At the end of each chapter is a short quiz to test your knowledge. If you miss a question on the quiz, reread the chapter to figure out how you answered incorrectly so you can learn from your mistake.

# Legend

> ⚠️ This is a warning

> ℹ️ This is an information

> ✨ This is a recommendation

# Required Tools

To get started with modding, you only need two things:

* A copy of [The Binding of Isaac: Repentance](https://store.steampowered.com/app/1426300/The_Binding_of_Isaac_Repentance/)
   * You can't mod the game beyond resource replacements if you own the game on a console (i.e: Switch, PS4) 
   * If you own Afterbirth+, some of the topics covered in this guide may not work due to the changes Repentance made to the modding API
   * If you do not own Afterbirth+ or Repentance, you can not mod the game as there is no modding API 
* An **Integrated Development Environment** (**IDE**) of your Choice. Some options include:
   * ✨ [Visual Studio Code](https://code.visualstudio.com/)
   * [ZeroBrane Studio](https://studio.zerobrane.com/)
   * [Notepad++](https://notepad-plus-plus.org/downloads/)

> ✨ It is highly reccomended to go with Visual Studio Code due to its powerful tooling as well as powerful extensions which can make your job with coding easier. This guidebook will assume you are using Visual Studio Code, although it still possible to follow along if you go with another IDE.

# ✨ Recommended Visual Studio Code extensions

If you are using Microsoft's Visual Studio Code, here are some extensions I would recommend:

* [Binding of Isaac Lua API](https://marketplace.visualstudio.com/items?itemName=Filloax.isaac-lua-api-vscode) - Provides autocomplete support for the API. It also installs Sumneko's Lua LSP which provides (linting)[https://www.perforce.com/blog/qac/what-lint-code-and-what-linting-and-why-linting-important] and type annotation support.
* [StyLua](https://marketplace.visualstudio.com/items?itemName=JohnnyMorganz.stylua) - An opinionated code formatter for Lua which enforces a consistent code style.
* [XML](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-xml) - Adds XML support to Visual Studio Code and allows you to use (Wofsauge's XML Validator)[https://pypi.org/project/isaac-xml-validator/]

# Frequently Asked Questions

Coming soon

# Useful Resources

* [Learn Visual Studio Code in 7min](https://www.youtube.com/watch?v=B-s71n0dHUk) - A quick introduction to Visual Studio Code.
* [Binding of Isaac: Lua Docs](https://wofsauge.github.io/IsaacDocs/rep/) - The API documentation. It should be treated as the holy bible for modding.
* [Slugcat's Repentance Modding Series](https://www.youtube.com/watch?v=rukHB48olG8&list=PLkIbky8_pFUpqAF9l7dh_YsEV-zpJ4q50) - A video series which also teaches you how to mod the game.
* [AgentCucco's Modding Series](https://www.youtube.com/playlist?list=PLUYzSIp7NO8cEer2FmtxSXlXoMFirvYDN) - A video series which covers Lua, an introduction to the game's animation editor, and a basic introduction to the modding API. Although this was made during the AB+ era, the material taught in this playlist still transfer well to Repentance.


