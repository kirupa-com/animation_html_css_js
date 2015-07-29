

Visual Studio and Apache Cordova
================================

You know about Apache Cordova! You probably even know about Visual Studio's awesome support for building and debugging Apache Cordova apps through its IDE. What you may not know is how the integration between Visual Studio and Apache Cordova actually works, and in this short article, let's take an overview of what is involved.

Our Approach
------------
One of the guiding principles that influenced our Visual Studio integration with Apache Cordova can be summed up in one word: **interoperability**. More specifically, interoperability with the rich set of tools and CLIs developers (such as yourself) use to build your projects. Apache Cordova projects you create in Visual Studio should work on the Cordova CLI, Ionic CLI, and any other tools that make up your workflow. Likewise, Apache Cordova projects created outside of Visual Studio open and work just as well as projects you create in Visual Studio itself.

The way we ensured this interoperability is by not inventing "yet another way" to build your Apache Cordova projects. Instead, we use the same open source tools that Apache Cordova CLI uses to get your project ready to run on Android, iOS, or Windows devices. We also use the same platform-specific SDKs to build and package the app.

The Details
-----------
When building an Apache Cordova project, under the covers, Visual Studio relies on the same tools that you would use when building a Cordova project manually using the command-line. We'll look into the tools in in much greater detail shortly, but at a high-level, the following diagram provides an overview of the components at play when building for Android and Windows devices:

<img src="http://www.kirupa.com/temp/build_windows.png" alt="Drawing" width=400px/>

When building for iOS devices, you have the addition of remotebuild tools running on the Mac side that you need for building an iOS package:

<img src="http://www.kirupa.com/temp/build_ios.png" alt="Drawing" width=600px/>

Let's describe what each of the components mean in much greater detail:

 - Visual Studio: This is the IDE that, besides being the place you spend most of your time in, is the entry point for all of your code to interface
 - MSBuild: When you build your projects in Visual Studio, all requests go through the MSBuild component
 - vs-tac: This is the layer where requests from MSBuild are translated into the various commands that Apache Cordova relies on for building the binaries for each platform. Beyond just acting as a mediator, this layer also extends Visual Studio with project and build-system support for allowing you to create and work with Apache Cordova projects.
 - Cordova: This takes all of your project files and creates the native project that
 - Native Tools: These are the platform specific tools that you will need to get your application packaged and deployed to either a simulator, emulator, or actual device. You have a different set of tools for Android, iOS, and Windows.
 
For building iOS apps, you have everything above in addition to:
 - remotebuild: This is a remote build agent that runs on the Mac. It listens for build requests from Visual Studio and then relies on the native tools on the Mac side to create the final iOS output
 - Xcode: Provides the linkers and build tools that the remotebuild agent uses to create the iOS binaries and then deploy them to an actual device or simulator

