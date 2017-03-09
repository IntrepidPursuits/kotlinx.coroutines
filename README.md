# kotlinx.coroutines [ ![Download](https://api.bintray.com/packages/kotlin/kotlin-eap-1.1/kotlinx.coroutines/images/download.svg) ](https://bintray.com/kotlin/kotlin-eap-1.1/kotlinx.coroutines/_latestVersion)

Library support for Kotlin coroutines. This is a companion version for Kotlin 1.1.0 release. 

## Modules

Basic modules:

* [kotlinx-coroutines-core](kotlinx-coroutines-core) -- core primitives to work with coroutines. 
* [kotlinx-coroutines-jdk8](kotlinx-coroutines-jdk8) -- additional libraries for JDK8 (or Android API level 24).
* [kotlinx-coroutines-nio](kotlinx-coroutines-nio) -- extensions for asynchronous IO on JDK7+.

Modules that provide builders and iteration support for various reactive streams libraries:

* [kotlinx-coroutines-reactive](reactive/kotlinx-coroutines-reactive) -- utilities for [Reactive Streams](http://www.reactive-streams.org)
* [kotlinx-coroutines-rx1](reactive/kotlinx-coroutines-rx1) -- utilities for [RxJava 1.x](https://github.com/ReactiveX/RxJava/tree/1.x)
* [kotlinx-coroutines-rx2](reactive/kotlinx-coroutines-rx2) -- utilities for [RxJava 2.x](https://github.com/ReactiveX/RxJava)

Modules that provide coroutine dispatchers for various single-threaded UI libraries:

* [kotlinx-coroutines-android](ui/kotlinx-coroutines-android) -- `UI` context for Android applications.
* [kotlinx-coroutines-javafx](ui/kotlinx-coroutines-javafx) -- `JavaFx` context for JavaFX UI applications.
* [kotlinx-coroutines-swing](ui/kotlinx-coroutines-swing) -- `Swing` context for Swing UI applications.
 
## Documentation

* [Guide to kotlinx.coroutines by example](coroutines-guide.md) (**read it first**)
* [Guide to UI programming with coroutines](ui/coroutines-guide-ui.md)
* [Change log for kotlinx.coroutines](CHANGES.md)
* [Coroutines design document (KEEP)](https://github.com/Kotlin/kotlin-coroutines/blob/master/kotlin-coroutines-informal.md)
* [Full kotlinx.coroutines API reference](http://kotlin.github.io/kotlinx.coroutines)
 
## Using in your projects

> Note that these libraries are experimental and are subject to change.

The libraries are published to [kotlin-eap-1.1](https://bintray.com/kotlin/kotlin-eap-1.1/kotlinx.coroutines) bintray repository.

These libraries require kotlin compiler version to be at least `1.1.0` and 
require kotlin runtime of the same version as a dependency.

### Maven

Add the bintray repository to `<repositories>` section (and also add `pluginRepository` to `<pluginRepositories>`,
if you're willing to get `kotlin-maven-plugin` from there):

```xml
<repository>
    <snapshots>
        <enabled>false</enabled>
    </snapshots>
    <id>dl</id>
    <name>bintray</name>
    <url>http://dl.bintray.com/kotlin/kotlin-eap-1.1</url>
</repository>
```

Add dependencies (you can also add other modules that you need):

```xml
<dependency>
    <groupId>org.jetbrains.kotlinx</groupId>
    <artifactId>kotlinx-coroutines-core</artifactId>
    <version>0.12</version>
</dependency>
```

And make sure that you use the right Kotlin version:

```xml
<properties>
    <kotlin.version>1.1.0</kotlin.version>
</properties>
```

### Gradle

Add the bintray repository (and also add it to `buildScript` section, if you're willing to get `kotlin-gradle-plugin` from there):

```groovy
repositories {
    maven {
        url "http://dl.bintray.com/kotlin/kotlin-eap-1.1"
    }
}
```

Add dependencies (you can also add other modules that you need):

```groovy
compile 'org.jetbrains.kotlinx:kotlinx-coroutines-core:0.12'
```

And make sure that you use the right Kotlin version:

```groovy
buildscript {
    ext.kotlin_version = '1.1.0'
}
```