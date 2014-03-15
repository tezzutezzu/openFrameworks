[openFrameworks](http://openframeworks.cc/) | [Documentation table of contents](table_of_contents.md)

OS X
====


[Installing Xcode](#installing)

[Running the examples](#running)

[Errors and Warnings](#errors)

[The difference between Debug and Release scheme](#debugrelease)

[Creating a new openFrameworks project](#creatingnew)

[Including addons to your project](#addons)

[Renaming Projects](#renaming)

[Why my app doesn't run? – Common build errors](#issues)

[openFrameworks resources](#resources)


<a name="installing" />
Installing Xcode
---------------------------------------------
To use openFrameworks with OS X, you need to have Xcode 4+ installed. 

You can download and install Xcode from the App Store. After the installation, make sure to install the Xcode command line tools.

You can install Xcode command line tool using the Download tab in the Xcode preferences or by typing "xcode-select -install" in your Terminal.

<a name="running" />
Running the examples
---------------------------------------------

![The .xcodeproj file of the GraphicsExample ](http://i.imgur.com/0WbPVqF.png)


You can run any project in the examples folder by opening its relative .xcodeproj file. 

Each project needs to be built before it can run, Xcode uses [schemes](https://developer.apple.com/library/mac/featuredarticles/XcodeConcepts/Concept-Schemes.html) to define the products to build. 


### Schemes

![Building the GraphicsExample](http://i.imgur.com/A4GZsgT.png)

For each example you will find three schemes: openFrameworks, a debug and a release target for the project. To run the project make sure the debug example's scheme is selected and hit the Build & Run button (the triangle in the toolbar).




<a name="errors" />
Errors and Warnings
---------------------------------------------
![](http://i.imgur.com/rNUTH7l.jpg)

While the app is building Xcode will show you the number of warnings (in yellow) and errors (in red). 
Most of the time you can ignore the warnings, but if your app has a high number of errors it will likely fail to build. See below for common issues when building.



<a name="debugrelease" />
The difference between Debug and Release scheme
-----------------------------------------------
![](http://i.imgur.com/kBelTKn.png)


- Debug is useful when developing your project, as it will provide the most information about where and why something crashed.
- Release is useful when you're done developing your project. It will create a smaller, faster app but it won't give you much information if it crashes.




<a name="creatingnew" />
Creating a new openFrameworks project
-------------------------------------

###Using Project Generator

The easiest way to create a new OF project is using the Project Generator tool located in the projectGenerator_osx folder at the root of your OF installation.

Name your project, select your addons and a new project will be generated in your "myApps" folder

###From an existing example

Another way to create a new openFrameworks project is to copy one that's similar to what you want to do. OF Examples follow the app directory structure pattern (e.g. apps/categoryName/appName) and are grouped by topic/addon.

For example:

- Copy an example folder like: examples/empty/emptyExample/ and rename the copy to apps/examples/myApp/
- Inside the myApp/ folder rename the .xcodeproj file to myApp.xcodeproj
- Open myApp.xcodeproj

<a name="addons" />
Including addons to your project
---------------------------------------------
Addons can be tricky to add, the best way of adding an addon to your project is:

1. Right click the "addons" group in your project 
2. Select New Group 
3. Select and Rename the group with the addon's name 
4. Add Files to your project (under File menu). 
5. Select the 'src' or 'libs' folder in the addon folder

Xcode is smart enough to add the eventual Header paths to your project so you don't need to do that.

(screenshot of final folder structure)


<a name="renaming" />
Renaming Projects
---------------------------------------------
To rename your project name click twice (as you usually do in OSX) on the project icon 
![Project renaming](http://i.imgur.com/BOHaTq6.png)

To change the name of your schemas: click on "Manage schemes" and rename the Schemes by selecting and clicking twice on them (as per above) or by just hitting Enter

![](http://i.imgur.com/8cHC9eB.png)

![](http://i.imgur.com/NNtXWO3.png)






<a name="issues" />
Common issues 
---------------------------------------------
There are a few common issues that cause your sketch build to fail:

- Lexical or Preprocessor Issue: "'tr1/memory' not found"
-- You need to change your Base SDK (see below) 

- "TargetConditionals.h" not found
-- Xcode Terminal may not be installed

- Undefined symbols for architecture i386
-- This usually happens when addons have been added incorrectly (see above for instructions)


###Change Base SDK

<a name="resources" />
openFrameworks resources
------------------------
If you have questions or issues, the best place to look is the openFrameworks forum: 
http://forum.openframeworks.cc/


Thanks for reading this and enjoy!
- The OF Team
