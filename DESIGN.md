# Design of Project ironica

### Overview Architecture

The project is decoupled with a C/S structure. This structure allow us to decouple the project into two (or eventually more) parts that are independent to each other. Each part is concentrated by its own issues and do not influence others.

Even in the future if we will carry on the project into a standalone application, it's still preferable to implement with an embedded C/S structure rather than a monolithic application.

The communication between client and server is HTTP request with data structures in json format.

For the back-end (server) we have chosen to use Kotlin as the main language, mainly because of its strong expressiveness and flexibility of Kotlin DSL. Other libraries such as Ktor, Kotlin-serialization, KI-Shell and KotlinPoet have been used. See [the repo of Simulatte](https://github.com/Ironica/simulatte) for more information.

As for the front-end (client), we have chosen Unity3D and therefore C# as the main language. Several libraries have been used.

### Back-end

Here's a simplified class/module diagram of implementation of back-end (without the ktor module). The overall UML will be too complicated to be shown here therefore I will move it to appendix.

![](./img/back-end-archi.png)

Each module are loosely coupled therefore you can easily replace an implementation of one part by another implementation but the project will still work.

\<TODO\>

Other informations:

-   `gradle` for project & package managements
-   `Space / GitHub` for checklist / TODO / project management
-   `Space` for CI/CD deployment

### Front-end

\<TODO\>

### Misc

Here's a use-case of a server connected by two different clients, to illustrate the connections between front-end and server but also the possibility to manage multiple requests at same time.

![](./img/request-flow.png)