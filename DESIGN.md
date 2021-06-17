### Synopsis

The game is based on a grid (tilemap). There will be one or more characters on the grid, and other items (gems/switches/monsters/locks, etc). Player should write codes (in Kotlin DSL) to control these characters to move within the grid and interact with items on the grid.

There are several conditions when they hold the player might win or lose a game. At the end of game the player gains gem that he/she could spend in the store for different features.

The game should be fun while still providing an opening introduction to programming for novices in PL.

### Characteristics

-   Genre: ~~2.5D isometric~~ 3D tilemap
-   Single Player
-   Language: Kotlin DSL
-   Game Engine: Unity 3D
-   Target: Cross-Platform (currently Windows & Mac)

### Tech stack

-   Front-end
    -   Unity 2020.3.7f1
        -   C#7, .Net 4.7.1 (Mono), Nuget, ...
-   Back-end
    -   IntelliJ IDEA 2021
        -   Java 11, Kotlin 1.5, Gradle, ...
-   Graphics
    -   Sketch
-   Modeling
    -   Blender
-   Sounds / Musics
    -   N/A
-   Misc
    -   The Postman - for http request test
-   Video Capture and Editing
    -   QuickTime
    -   iMovie

### Gameplay

-   Types of characters

    -   Player: common character, has every possibilities to interact in a plains terrain

        ~~*naming system*: if user attributes the corresponding name to a player, then the player will have its special skin and could have some more actions.~~ (UNIMPLEMENTED)

    -   ~~Specialist: a special kind of character that have some more abilities regarding modifying the terrain (level up or down of platforms)~~ (IMPLEMENTED AT BACKEND BUT CURRENTLY UNAVAILABLE)

-   Types of items

    -   Gem: to be collected by user to achieve the goal
    -   Switch: to be toggled by user to achieve the goal
    -   ~~Beeper: could be collected or dropped on a tile~~ (IMPLEMENTED AT BACKEND BUT CURRENTLY UNAVAILABLE)
    -   Portal: could teleport a character to another tile
    -   ~~Lock & Platforms: specialists can level-up and level-down platforms by toggling a lock~~ (IMPLEMENTED AT BACKEND BUT CURRENTLY UNAVAILABLE)

-   Enemy

    At the stage the enemies are just a kind of monster that a character could attack. The monster dies instantly after the attack and character advance for a square.

    More complex enemies could be developed in the future.

-   Game Control

    Write codes.

-   Game system

    In each level, user must write some codes to drive the characters to move, to collect gems and to interact with other objects on the playground.

    In the future, it would be possible for players to write codes to change the terrains.

    Additional systems contains the change of character, the store, etc. 

-   UI

    The main UI is divided into two parts, a text area for entering codes with some more buttons, and a playground where the game animation is rendered.

    Player could choose to `START` or `RESET` the text area *and also* the game playground.

-   Additional features

    -   [x] Win/Lost/Pending status
    -   [x] Progress bar
    -   [x] Stats of the current game e.g. collected gems
    -   [x] Autosave: The codes of user are automatically saved when the user click on the `START` button
    -   [x] Different game levels and a menu to choose a level to play
    -   [x] Bundled levels, one must resolve enough levels in current stage to progress to the next stage
    -   [x] A console for the purpose of debugging
    -   [x] Messages or sound effects while special events is triggered

---

### Dev goal

-   Back-end
    -   A full featured server that could be build up to receive requests and make responses
    -   More features of playground (e.g. terrain changes, creative gamemode, etc)
-   Front-end
    -   A minimum playable client that could communicate with server, allows user to write codes and decode response of the server to make correct interactions
    -   A client with more additional features
    -   Improved UI/UX design with an adapted design language

