multi-kotlin-project-with-buildSrc
==================================

A multi-project build with two Kotlin based projects:

 1. [core](./core) implements the main algorithm to compute the answer to the ultimate question of Life, the Universe and Everything
 2. [cli](./cli) implements the command line interface

Gradle Script Kotlin support is enabled recursively for all projects in [settings.gradle](./settings.gradle#L3).

Common behavior for all projects, such as the configuration of _group_, _version_ and _repositories_, is defined in the [root project build script](./build.gradle.kts).

Plugin application and dependency configuration is segregated to each
separate subproject with some common build logic in [`buildSrc`](./buildSrc/src/main/kotlin/utils.kt).

Run with:

    ./gradlew run

Check all project dependencies with:

    ./gradlew dependencies
