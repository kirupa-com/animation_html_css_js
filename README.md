#**Visual Studio 2015 RC**

**Issue #1**
------------
Projects created in an earlier version of Visual Studio will need to be migrated to support the new project structure that is more interoperable with 3rd party tools and CLIs. 

To migrate your previous projects to the new structure:

 1. Make a backup of your existing project (obligatory first step :))
 2. Create a new project using the JavaScript \ Apache Cordova Apps \
    Blank App template
	 * For TypeScript projects, you can use the TypeScript equivalent of this same project
 3. Copy the .jsproj and taco.json files created by this template into your own project's folder
 4. In your project, create a new folder named www
 5. Delete the following folders from your project's folder:
	 * bin
	 * bld
 8. Leave the following folders/files in your project directory:
	 * merges
	 * res
	 * plugins
	 * config.xml
 13. Copy all other files/folders into the www folder
 14. If you're using TypeScript, you'll need to add a tsconfig.json to
     your project folder and define config settings for your project –
     see more in the Configuring TypeScript section
 15. Now you can build and run your application

If you have errors, you may need to update file references to reflect the new folder structure. 

Lastly, you should add the following XML elements to your config.xml to ensure your icons and splash screens are picked up by right clicking on the file and selecting "View Code":

    <platformname="android">
        <iconsrc="res/icons/android/icon-36-ldpi.png"density="ldpi" />
        <iconsrc="res/icons/android/icon-48-mdpi.png"density="mdpi" />
        <iconsrc="res/icons/android/icon-72-hdpi.png"density="hdpi" />
        <iconsrc="res/icons/android/icon-96-xhdpi.png"density="xhdpi" />
      </platform>
      <platformname="ios">
        <iconsrc="res/icons/ios/icon-60-3x.png"width="180"height="180" />
        <iconsrc="res/icons/ios/icon-60.png"width="60"height="60" />
        <iconsrc="res/icons/ios/icon-60-2x.png"width="120"height="120" />
        <iconsrc="res/icons/ios/icon-76.png"width="76"height="76" />
        <iconsrc="res/icons/ios/icon-76-2x.png"width="152"height="152" />
        <iconsrc="res/icons/ios/icon-40.png"width="40"height="40" />
        <iconsrc="res/icons/ios/icon-40-2x.png"width="80"height="80" />
        <iconsrc="res/icons/ios/icon-57.png"width="57"height="57" />
        <iconsrc="res/icons/ios/icon-57-2x.png"width="114"height="114" />
        <iconsrc="res/icons/ios/icon-72.png"width="72"height="72" />
        <iconsrc="res/icons/ios/icon-72-2x.png"width="144"height="144" />
        <iconsrc="res/icons/ios/icon-small.png"width="29"height="29" />
        <iconsrc="res/icons/ios/icon-small-2x.png"width="58"height="58" />
        <iconsrc="res/icons/ios/icon-50.png"width="50"height="50" />
        <iconsrc="res/icons/ios/icon-50-2x.png"width="100"height="100" />
      </platform>
      <platformname="windows">
        <iconsrc="res/icons/windows/Square150x150Logo.scale-100.png"width="150"height="150" />
        <iconsrc="res/icons/windows/Square150x150Logo.scale-240.png"width="360"height="360" />
        <iconsrc="res/icons/windows/Square30x30Logo.scale-100.png"width="30"height="30" />
        <iconsrc="res/icons/windows/Square310x310Logo.scale-100.png"width=""height="" />
        <iconsrc="res/icons/windows/Square44x44Logo.scale-240.png"width="106"height="106" />
        <iconsrc="res/icons/windows/Square70x70Logo.scale-100.png"width="70"height="70" />
        <iconsrc="res/icons/windows/Square71x71Logo.scale-240.png"width="170"height="170" />
        <iconsrc="res/icons/windows/StoreLogo.scale-100.png"width="50"height="50" />
        <iconsrc="res/icons/windows/StoreLogo.scale-240.png"width="120"height="120" />
        <iconsrc="res/icons/windows/Wide310x150Logo.scale-100.png"width="310"height="150" />
        <iconsrc="res/icons/windows/Wide310x150Logo.scale-240.png"width="744"height="360" />
      </platform>
      <platformname="wp8">
        <iconsrc="res/icons/wp8/ApplicationIcon.png"width="62"height="62" />
        <iconsrc="res/icons/wp8/Background.png"width="173"height="173" />
      </platform>
      <platformname="android">
        <splashsrc="res/screens/android/screen-hdpi-landscape.png"density="land-hdpi" />
        <splashsrc="res/screens/android/screen-ldpi-landscape.png"density="land-ldpi" />
        <splashsrc="res/screens/android/screen-mdpi-landscape.png"density="land-mdpi" />
        <splashsrc="res/screens/android/screen-xhdpi-landscape.png"density="land-xhdpi" />
        <splashsrc="res/screens/android/screen-hdpi-portrait.png"density="port-hdpi" />
        <splashsrc="res/screens/android/screen-ldpi-portrait.png"density="port-ldpi" />
        <splashsrc="res/screens/android/screen-mdpi-portrait.png"density="port-mdpi" />
        <splashsrc="res/screens/android/screen-xhdpi-portrait.png"density="port-xhdpi" />
      </platform>
      <platformname="ios">
        <splashsrc="res/screens/ios/screen-iphone-portrait.png"width="320"height="480" />
        <splashsrc="res/screens/ios/screen-iphone-portrait-2x.png"width="640"height="960" />
        <splashsrc="res/screens/ios/screen-ipad-portrait.png"width="768"height="1024" />
        <splashsrc="res/screens/ios/screen-ipad-portrait-2x.png"width="1536"height="2048" />
        <splashsrc="res/screens/ios/screen-ipad-landscape.png"width="1024"height="768" />
        <splashsrc="res/screens/ios/screen-ipad-landscape-2x.png"width="2048"height="1536" />
        <splashsrc="res/screens/ios/screen-iphone-568h-2x.png"width="640"height="1136" />
        <splashsrc="res/screens/ios/screen-iphone-portrait-667h.png"width="750"height="1334" />
        <splashsrc="res/screens/ios/screen-iphone-portrait-736h.png"width="1242"height="2208" />
        <splashsrc="res/screens/ios/screen-iphone-landscape-736h.png"width="2208"height="1242" />
      </platform>
      <platformname="windows">
        <splashsrc="res/screens/windows/SplashScreen.scale-100.png"width="620"height="300" />
        <splashsrc="res/screens/windows/SplashScreen.scale-240.png"width="1152"height="1920" />
        <splashsrc="res/screens/windows/SplashScreenPhone.scale-240.png"width="1152"height="1920" />
      </platform>
      <platformname="wp8">
        <splashsrc="res/screens/wp8/SplashScreenImage.jpg"width="480"height="800" />
      </platform>

**

Issue #2
--------

**
When you upgrade from VS2015 CTP5 to CTP6, Apache Ant gets uninstalled. The workaround is to reinstall Ant. You can find manual instructions for installing and configuring Ant at [this location](https://msdn.microsoft.com/en-us/library/dn757054.aspx#InstallTools).
**

Issue #3
--------

**
Due to a Cordova issue with Cordova 4.3.0, you can run into problems with plugin variables in Cordova < 5.0.0. Plugin variable information is lost if you install the "plugin" before the "platform" which can happen depending on your workflow. They do, however, function in Cordova 5.0.0 which you can use with VS 2015 RC. To update to 5.0.0 and use plugin variables, you will need to update your VS project and use the command line.

 1. Remove the plugins with the variables via the config designer.
 2. Update to Cordova 5.0.0 via the config designer (Platforms > Cordova
    CLI)
 3. From the command line:
	 1. Go to your project directory.
	 2. Type the following substituting the plugin name for the plugin you
	    wish to add:
	    
		> npm install -g cordova cordova plugin add
		> nl.x-services.plugins.launchmyapp --variable URL_SCHEME=myscheme

This issue is actively being worked so things should improve in the future. You will also want to take note of the additional known issues pertaining to 5.0.0 when using it.

#**iOS Build Related Known Issues**

**Issue #1**
------------
After installing the latest version of [vs-mda-remote package](https://www.npmjs.com/package/vs-mda-remote), you will need to run the following commands before you start up the remote agent. These commands ensure your user has permissions to the contents of the npm package cache in your home directory when using older versions of Node.js and npm. Newer versions of Node.js and npm will do this for you automatically.

    sudo npm cache clear 
    sudo chown -R `whoami` ~/.npm

**Issue #2**
------------
If deploying to iOS 8.3 device fails because vs-mda-remote cannot find DeveloperDiskImage.dmg, ensure you are running OSX Yosemite and Xcode 6.3. Xcode 6.3 is required to deploy to an 8.3 device and only runs on Yosemite.

**Issue #3**
------------
Cordova plugins that contain custom frameworks like the Facebook Connect plugin may experience compilation errors when building for iOS due to missing symlinks. As a workaround, use the following Cordova hook, clean the solution, and try again: [https://github.com/Chuxel/taco-tricks/tree/master/ios-plugin-symlink-fix](https://github.com/Chuxel/taco-tricks/tree/master/ios-plugin-symlink-fix) 

#**Apache Cordova 5.0.0 Related Known Issues**

> Visual Studio 2015 RC uses Cordova 4.3.0 by default. If you’ve opted
> to use 5.0.0 instead, there are some issues with the changes to the
> Android platform in this major release that you will need to work
> around.

**Issue #1**
------------
Visual Studio 2015 RC uses Ant to build Android while the command line has switched to Gradle by default in version 5.0.0 of the CLI.

**Issue #2**
------------
To build a project that uses the Crosswalk plug-in, you will need to build using the command line:

    npm install -g cordova 
    cordova platform remove android 
    cordova platform add android 
    
    cordova build android 
    
    or 
    
    cordova run android 
    
    or 
    
    cordova emulate android

**Issue #3**
------------
The Android platform in Cordova 5.0.0 requires Android SDK API Level 22. Install the SDK using the Android SDK manager.

**Issue #4**
------------
If you experience slow build performance and reliability issues when using the Crosswalk plugin, we recommend you add this plugin towards the end of your development as you are starting to finalize your app.

**Issue #5**
------------
The Android platform contained within Cordova 5.0.0 does not have a "whitelist" plugin installed by default and therefore blocks network access by default. There are now two whitelist plugins that can be installed:

 - Installing “cordova-plugin-legacy-whitelist” will cause the platform
   to behave the way it did in 4.x and enables the "Domain Access" list
   in the configuration designer. You can install it from the command
   line or using
   https://github.com/apache/cordova-plugin-legacy-whitelist.git from
   the Custom tab of the configuration designer.
    
 - Installing “cordova-plugin-whitelist” results in some new behaviors
   and introduces new config.xml elements that can be added manually by
   right clicking on config.xml and selecting "View Code." You can
   install it from the command line or using
   https://github.com/apache/cordova-plugin-whitelist.git from the
   Custom tab of the configuration designer.

**Issue #6**
------------
Visual Studio 2015 RC uses Ant to build Android while the command line has switched to Gradle by default in version 5.0.0 of the CLI. When switching between Visual Studio and the command line with the version of Android in Cordova 5.0.0, you may want to specify that the platform should be built with Ant instead if you are running into unexpected issues.

**Ex:**

    cordova build android -- --ant

You can also set an environment variable to keep this preference around for a command line session.

    set ANDROID_BUILD=ant

Finally, if you are still build errors, you may want to opt to remove and re-add the android platform after switching build systems.

    cordova platform remove android 
    cordova platform add android

**Issue #7**
------------
Ripple does not function properly in Cordova 5.0.0 due to a newly introduced validation check. This has already been fixed in Cordova main and will be resolved in a Cordova 5.x point release.

#**CTP 3.1 (Visual Studio 2013) Known Issues Section**

**Issue #1**
------------
While trying to associate a Cordova app with Windows store using Visual Studio 13 and CTP3.1 , the AppxManifest.xml doesn’t get updated with the appropriate Application Id & publisher name. We have fixed this issue in VS2015 RC. To fix this issue, install the plugin from [https://github.com/Chuxel/taco-tricks/tree/master/plugin-windows-package-fix](https://github.com/Chuxel/taco-tricks/tree/master/plugin-windows-package-fix) and try building your application again.

**Issue #2**
------------
When using version 0.2.8 or higher of vs-mda-remote, you should add the following XML elements to your config.xml to ensure your icons and splash screens are picked up properly.

    <platformname="ios">
        <iconsrc="res/icons/ios/icon-60-3x.png"width="180"height="180" />
        <iconsrc="res/icons/ios/icon-60.png"width="60"height="60" />
        <iconsrc="res/icons/ios/icon-60-2x.png"width="120"height="120" />
        <iconsrc="res/icons/ios/icon-76.png"width="76"height="76" />
        <iconsrc="res/icons/ios/icon-76-2x.png"width="152"height="152" />
        <iconsrc="res/icons/ios/icon-40.png"width="40"height="40" />
        <iconsrc="res/icons/ios/icon-40-2x.png"width="80"height="80" />
        <iconsrc="res/icons/ios/icon-57.png"width="57"height="57" />
        <iconsrc="res/icons/ios/icon-57-2x.png"width="114"height="114" />
        <iconsrc="res/icons/ios/icon-72.png"width="72"height="72" />
        <iconsrc="res/icons/ios/icon-72-2x.png"width="144"height="144" />
        <iconsrc="res/icons/ios/icon-small.png"width="29"height="29" />
        <iconsrc="res/icons/ios/icon-small-2x.png"width="58"height="58" />
        <iconsrc="res/icons/ios/icon-50.png"width="50"height="50" />
        <iconsrc="res/icons/ios/icon-50-2x.png"width="100"height="100" />
      </platform>
      <platformname="ios">
        <splashsrc="res/screens/ios/screen-iphone-portrait.png"width="320"height="480" />
        <splashsrc="res/screens/ios/screen-iphone-portrait-2x.png"width="640"height="960" />
        <splashsrc="res/screens/ios/screen-ipad-portrait.png"width="768"height="1024" />
        <splashsrc="res/screens/ios/screen-ipad-portrait-2x.png"width="1536"height="2048" />
        <splashsrc="res/screens/ios/screen-ipad-landscape.png"width="1024"height="768" />
        <splashsrc="res/screens/ios/screen-ipad-landscape-2x.png"width="2048"height="1536" />
        <splashsrc="res/screens/ios/screen-iphone-568h-2x.png"width="640"height="1136" />
        <splashsrc="res/screens/ios/screen-iphone-portrait-667h.png"width="750"height="1334" />
        <splashsrc="res/screens/ios/screen-iphone-portrait-736h.png"width="1242"height="2208" />
        <splashsrc="res/screens/ios/screen-iphone-landscape-736h.png"width="2208"height="1242" />
      </platform>

**(You can edit the contents of config.xml by right clicking on it and selecting "View Code".)**

Alternatively you can install version 0.2.7 instead by using the following command:

    npm install -g vs-mda-remote@0.2.7


#**General Known Issues**

**Issue #1**
------------
The “Solution Platform” dropdown may not appear in the toolbar when upgrading Visual Studio 2013 from a previous version to Update 4. You can add using the “Standard Toolbar Options” dropdown as described in [Microsoft Support article 2954109](http://support.microsoft.com/kb/2954109).

**Issue #2**
------------
If you already had the Android SDK installed, you may also need to update and install the SDK for Android 4.4.x (API level 19). You may need to restart Visual Studio if it is open while updating the Android SDK through the SDK Manager to be able to build for Android after the update is complete. See [Manually Installing Dependencies](https://msdn.microsoft.com/en-us/library/dn757054.aspx#ThirdParty) for details.

**Issue #3**
------------
In some circumstances, when deploying to iOS devices, they phone may enter an unresponsive state where apps may stops responding. Avoid deploying an app when the same app is still running. 
As a workaround, if you enter this state, soft reset your iOS device.

**Issue #4**
------------
While setting a PIN for secure iOS builds, if you later re-open the Remote Agent Configuration options page, clicking "OK" will clear the PIN and revert to non-secure builds unless you re-enter a PIN. 

As a work-around, either hit "Cancel" whenever you re-open the options page to Remote Agent Configuration, or re-enter a new PIN.

**Issue #5**
------------
Plugins will be re-downloaded after a “clean” operation. Developers should specify a version number or reference the plugins locally when using third-party plugins. See the [Plugins](https://msdn.microsoft.com/en-us/library/dn757051.aspx) section for details.

**Issue #6**
------------
The contents of the “res” folder cannot be accessed by web content as they are copied into platform-specific native project locations.

**Issue #7**
------------
Not all iOS Simulator devices are currently listed in the Debug Target dropdown in Visual Studio. A workaround is to manually change the device using the iOS Simulator Hardware > Device menu.

**Issue #8**
------------
If a plugin is added to your project, built for iOS, and then removed from the project, the plugin will still be included in the iOS build until you clean or build for another platform. As a workaround, clean or rebuild instead of build.

**Issue #9**
------------
The first time you launch Visual Studio after installing the Tools for Apache Cordova extension, IntelliSense will not work for the Apache Cordova™ object or other Cordova plugins. Please restart Visual Studio to fix the problem.

**Issue #10**
------------
When using TypeScript, there are known issues that will incorrectly identify project items as external code or will fail to read in a user configuration file. To avoid unexpected behavior when working with a Cordova TypeScript project, turn off Just My Code (Options > Debugger > General > uncheck Enable Just My Code).

**Issue #11**
------------
The project name automatically sets the display name in config.xml. If you encounter a build error because of this problem, set your system locale, then clean your project and rebuild.

**Issue #12**
------------
During installation, if your “My Documents” path redirects to a server share location, install the MSI from“%localappdata%\Microsoft\MultiDeviceHybridApps” instead.

**Issue #13**
------------
Dragging a mixed-case file into an HTML page creates a lowercase reference which will cause it to not be found on Android and iOS. Manually update the reference with the correct casing.
