![Logo](img/logo.png)

# Project ironica

## Background

The project was inspired by the famous *playgrounds* application of iOS/MacOS but also *Karel The Robot*. Both programs illustrate a simple teaching environment of imperative programming basics for beginners while the first also integrates a full language runtime (in Swift) into the environment.

The idea was first implemented by creating a homemade DSL using ANTLR 4.9. Later, we have decided to switch to using Kotlin DSL solely.

## What's difference?

The implementation takes full advantages of Kotlin DSL (such as extension methods, coroutines, etc). By the way, it's based on a client-server structure, which means that the server and client are implemented independently. In theory, you can switch from different implementations of server but also client.

## Implemented Features

-   A playground server that receives requests from client, simulates a playground and resends responses back.

    -   Based on Kotlin DSL for language support and full power of Kotlin Language
    -   Supports different type of items and characters in server side, but several are not implemented at the front-end
    -   Implemented a simple console to print out messages
    -   Supports different game mode and configurations
    -   Supports multi requests at the same time

    See the [wiki of simulatte](https://github.com/Ironica/simulatte/wiki/About) for more info.

-   A client that sends requests to server and receives responses from server.

    -   The client decodes the response and render the tilemap
    -   The server is embedded within the client, launched at the start and closed at the exit of client
    -   The playground was first implemented in isometry then in true 3d (models, lights, etc)
    -   The playground's camera could be zoomed in/out/rotated/panned
    -   Any error will be caught and displayed within the console
    -   Some additional systems
        -   Map switching system
        -   Music system
        -   Store system
        -   i18n

See `DESIGN.md` and documents of each repo for more info.

## Unimplemented Features

Currently we have decided to abandon lots of features due to the time and resource limits.

-   Beepers/Platform/Platform locks/Specialist character at front-end
-   Notification messages and reminder at front-end
-   Stamina system and other systems for playground
-   An elaborated error handling and report system
-   Dancing character and other customized actions
-   Real animations
-   ...

Besides, there are many possibilities for this project. See **Where to go from here**.

## Tech stack

-   Server side: Kotlin + Ktor + Ki-Shell
-   Client side: Unity3D + Blender

See `ARCHITECTURE.md` and each repo for more informations.

## Project Licenses

-   AGPL for Back-end
-   LGPL for Front-end

## Where to go from here?

In `ARCHITECTURE.md` we have discussed the advantage of our C/S architecture. However, a monolithic application could be also interesting, just in this scenario we need to change our server implementation to Java stack, such as LWJGL or libKTX, etc.

If we stick on Unity stack, lots of improvements could be done in the future:

-   Improve the 3d effects such as animation
-   UI/UX improvements
-   More complex configurations and game rules
-   More game modes
-   Improve extensibility
-   More helper features such as syntax highlighting, auto-completion, static analysis, etc...

We have also explored some possibilities in the [wiki of simulatte](https://github.com/Ironica/simulatte/wiki/About).

---

## Getting Started

See `DEPLOY.md` for instructions for building the projects and running the game.

## Language reference

The language used in this project is a Kotlin DSL, which is entirely a subset of the language Kotlin.

Get [here](https://play.kotlinlang.org/) for more information about the Kotlin Language.

See `Language Reference.md` in [wiki of project simulatte](https://github.com/Ironica/simulatte/wiki) for which is **not** a comprehensive Kotlin Language reference but tries to introduce as many language features as possible.
