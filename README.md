# Project ironica

## Background

The project was inspired by the famous *playgrounds* application of iOS/MacOS but also *Karel The Robot*. Both programs illustrate a simple teaching environment for imperative programming basics while the first also integrates a full language runtime (in Swift) into the environment.

The idea was first implemented by creating my own DSL using ANTLR 4.9. Later, I have decided to switch to using Kotlin DSL solely.

## What's difference?

The implementation takes full advantages of Kotlin DSL. By the way, it's based on a client-server structure, which means that the server and client are implemented independently. In theory, you can switch from different implementations of server but also client, although currently there is only one client and only one server.

## Where to go from here?

In DESIGN.md we have discussed the advantage of our C/S architecture. However, from the user's experience this structure may be a little complicated.

A standalone version with an embedded server might be therefore easy to use for end users while taking advantages of a C/S structure, just like what we know from Minecraft.

However, a monolithic application could be also interesting, just in this scenario we need to change our server implementation to Java stack, such as LWJGL or libKTX, etc.

## Getting Started

\<TODO\>

## Language reference

The language used in this project is a Kotlin DSL, which is entirely a subset of the language Kotlin.

Get [here](https://play.kotlinlang.org/) for more information about the Kotlin Language.

We will only illustrate the commands and features that might be useful in this project.

\<TODO\>