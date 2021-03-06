# Design Patterns IntelliJ IDEA Plugin
This plugin is meant to provide on the fly implementation of various design patterns.
<br/>
You can download it directly from IntelliJ IDEA or from https://plugins.jetbrains.com/plugin/10856-design-patterns-plugin

## Currently supported design patterns
* Behavioral
  * Strategy
* Creational
  * Builder (Inner)
  * Factory
  * Singleton
* Structural

## How to use
Assuming you have already installed the plugin, you can use it just by right-clicking inside a .java file while your mouse is inside a code block that defines a class. This will bring up the editor menu and the first option will be Design Patterns, where you can choose which one should be implemented.<br/>
![Demonstration screenshot](/../screenshots/Demonstration.png?raw=true)<br/>
![Demo gif](/../screenshots/BuilderDemo.gif?raw=true)

## Getting started
In order to avoid some common importing errors (when it comes to intellij plugin development), please follow the steps listed below.<br/>
* Open the project using IntelliJ IDEA (Community or Ultimate)
* In `Project Structure` -> `Project Settings` -> `Project` -> `Project SDK` create a new `IntellJ Platform Plugin SDK`</br>
  * When asked for directory, use your IntelliJ IDEA installation directory.
  * Note that you will need IntelliJ IDEA Community in order to be able to properly debug the SDK's core code. If no debug is required though, Ultimate will work just fine as well.
* In `Project Language Level` choose `8 - Lambdas, type annotations etc` 
* In `Project compiler output` choose the out folder (for example `C:\Users\design-patterns\out`
* Use `gradlew runIde` to run the plugin

## Release History
* <string>2.0.1</strong>
  * Adds support for IDEA builds from '145.20' to '191.*'
  * Fixes bug that was causing 'NullPointerException' when clicking on non .java files
  * Code refactoring
* <strong>2.0.0</strong>
  * Fixes bug that was causing 'ActionDuplicationException' during IDEA launch
  * Migrates plugin's build tool from DevKit to Gradle
  * Changes Singleton and Builder to use resource templates instead of String literals
  * Adds support for IDEA builds from '145.20' to '183.*'
* <strong>1.1.0</strong>
  * Updated Builder DP, so that it can now handle mandatory fields (if the user wants to)
  * Fixed bug in Builder DP, that would produce multiple constructors when ran again
  * Fixed bug in Strategy/Factory DP, that would cause error, when running it in a class without package statement
  * Fixed bug in Factory DP, that would produce multiple constructors when ran again
  * Fixed bug in Factory DP, that would not always find all implementors of an interface
* <strong>1.0.1</strong>
  * Added Factory Design Pattern 
  * Fixed bug with package declaration in Strategy Design Pattern 
  * Fixed bug with modifiers of fields and methods in Singleton Design Pattern
* <strong>1.0.0</strong>
  * Added Builder Design Pattern
  * Added Singleton Design Pattern
  * Added Strategy Design Pattern

## Authors
* **Orestes Polyzos** - *Initial work* - [OrPolyzos](https://github.com/OrPolyzos)