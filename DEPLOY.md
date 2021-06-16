# Deployment

## Server Side

The project is build with Intellij IDEA 2021.1. You could either get newest release from [here](https://github.com/Ironica/simulatte/releases) or build the project manually.

If you just want to launch the game, you don't need to deploy the server, please go directly to section **Client**.

#### Prerequisite

JDK version between 11 and 15 (inclusive) is required. Any other version (8 or 16) are not supported. According to your OS platform, you can use `choco`, `brew` or `apt-get` or other package manager to get the latest OpenJDK with `adoptopenjdk`.

#### Clone the project

Ensure that you have `git` installed.

Change directory to your workspace and use `git` to clone the repo into your workspace:

```bash
git clone https://github.com/Ironica/simulatte
```

If you are using Intellij IDEA, you can also clone the project via the `Get from VCS` button within the welcome interface.

#### Build in Intellij IDEA

Open the project in Intellij IDEA. 

The project is initialized with Gradle. You can open the Gradle panel, to process several tasks. Otherwise, you can build and run the project using the `Build` or `Run` features within Intellij IDEA. The default configuration should launch from the `ApplicationKt` main entrance.

Be aware that in order to produce an executable product, you shouldn't use the `Build Artifacts` command. Use `shadowJar` command in Gradle instead.

Here are several tasks that might be interesting:

-   `run` in `Tasks/application`, this will run the program with entrypoint as `ApplicationKt`
-   `build` in `Tasks/build`, this will rebuild the project
-   `buildClassDiagram` in `Tasks/documentation`, this will generate a UML description of all classes within the project (at a point of view of Java), which could be read by PlantUML to generate a UML representation.
-   `shadowJar` in `Tasks/shadow`, this will produce a bundled Java executable file within `/build/libs`.

#### Build in Gradle

If you have Gradle installed, you could use it to build the project.

The usage of `gradle build tool` is not tested but normally it should work with the above introduced commands. e.g. `gradle shadowJar`. Syntaxs could be differ.

## Client

You could download release from [here](https://github.com/Ironica/Unity-Front-End/releases). Each release contains a target for Windows and a target for macOS. M1 is not tested but the game might run.

Just unarchive the archive and run the executable to launch the game. Do not modify the `Assets` folder.

#### Runtime Prerequisite

No .NET environment is required for launching the game.

However, a Java JDK version of between 11 and 15 (inclusive) is required to make the embedded server run correctly. See section **Server > Prerequisite** for more info.

#### Build Prerequisite

Unity 2020.3.7f1 is required to build the project.

#### Build the project

Make sure that in `Build Settings > Player Settings > Other Settings > Configuration`, the `API Compatibility Level` is set to `.NET 4.x`

In `Build Settings`, choose the target platform and corresponding architecture, then click `Build` to select your path to the target and build the project.

The game is tested in PC/Mac, and it should work on Linux platform. Other platforms are not supported.

Default path is within the project's root directory. If you want to specify another path, then please make sure that some files in `Assets` directory is copied to the path that contains your target file.

Here's a list of directories that's necessary for the game to be launched correctly

```
Assets
  └─ Resources
       ├─ EmbeddedServer
       ├─ MapJson
       ├─ Inventory
       └─ Scripts
            └─ Store
                 └─ JsonFile
```

You can delete safely everything else and all `.meta` files in your copy of `Assets` directory. Don't delete anything in your `Assets` directory within the repo.

#### Run the game

Click on the executable to launch the game.