[openFrameworks](http://openframeworks.cc/) | [Documentation table of contents](table_of_contents.md)

OS X
====
To use openFrameworks with OS X, you need to have Xcode 4+ installed. 

##Installing Xcode
Download Xcode from the App Store and install the Command line tools by using the Download tab in the Xcode preferences or typing "xcode-select -install" in your Terminal.

##Running the examples
The first thing to do after installing Xcode is to check everything is working and to run some of the provided examples.

You can run any project in the examples folder by opening its relative .xcodeproj file.

(screenshot of GraphicsExample)

Each project contains schemes for building OpenFrameworks and the project itself. For compiling the project make sure the example's scheme (in our case GraphicsExample) is selected and hit the Build & Run button (cmd + R).

(screenshot of GraphicsExample)


##Including addons to your project
1. Right click the "addons" group in your project 
2. Select New Group 
3. Name the group whatever the addon is 
4. Drag the 'src' or 'libs' folder in the newly created group from the Finder


Common issues
-------------
- Lexical or Preprocessor Issue: "'tr1/memory' not found" (wrong Base SDK)
- Workspace integrity
- "TargetConditionals.h" not found
- Undefined symbols for architecture i386


Creating a new openFrameworks project
-------------------------------------
###From an existing example

The easiest way to create a new openFrameworks project is to copy one that's similar to what you want to do. OF Examples follow the app directory structure pattern (e.g. apps/categoryName/appName) and are grouped by topic/addon.

For example:

- Copy an example folder like: examples/empty/emptyExample/ and rename the copy to apps/examples/myApp/
- Inside the myApp/ folder rename the .xcodeproj file to myApp.xcodeproj
- Open myApp.xcodeproj
- In the sidebar, under "Targets", right click on "emptyExample" and rename it to "myApp"

###Using Project Generator

The difference between Debug and Release mode
---------------------------------------------
These are two build configurations, "Debug" and "Release".

- Debug is useful when developing your project, as it will provide the most information about where and why something crashed.
- Release is useful when you're done developing your project. Release will create a smaller, faster app -- but it won't give you much information if it crashes.


openFrameworks resources
------------------------
If you have questions or issues, the best place to look is the openFrameworks forum: 
http://forum.openframeworks.cc/


Thanks for reading this and enjoy!
- The OF Team
