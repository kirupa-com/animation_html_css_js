#**Known Issues - iOS Build**

----------
After installing the latest version of [vs-mda-remote package](https://www.npmjs.com/package/vs-mda-remote), you will need to run the following commands before you start up the remote agent. These commands ensure your user has permissions to the contents of the npm package cache in your home directory when using older versions of Node.js and npm. Newer versions of Node.js and npm will do this for you automatically.

    sudo npm cache clear 
    sudo chown -R `whoami` ~/.npm

----------
If deploying to iOS 8.3 device fails because vs-mda-remote cannot find DeveloperDiskImage.dmg, ensure you are running OSX Yosemite and Xcode 6.3. Xcode 6.3 is required to deploy to an 8.3 device and only runs on Yosemite.

----------
Cordova plugins that contain custom frameworks like the Facebook Connect plugin may experience compilation errors when building for iOS due to missing symlinks. As a workaround, use the following Cordova hook, clean the solution, and try again: [https://github.com/Chuxel/taco-tricks/tree/master/ios-plugin-symlink-fix](https://github.com/Chuxel/taco-tricks/tree/master/ios-plugin-symlink-fix) 

#**Apache Cordova 5.0.0 Related Known Issues**

> Visual Studio 2015 RC uses Cordova 4.3.0 by default. If you’ve opted
> to use 5.0.0 instead, there are some issues with the changes to the
> Android platform in this major release that you will need to work
> around.

----------
Visual Studio 2015 RC uses Ant to build Android while the command line has switched to Gradle by default in version 5.0.0 of the CLI.

----------
To build a project that uses the Crosswalk plug-in, you will need to build using the command line:

    npm install -g cordova 
    cordova platform remove android 
    cordova platform add android 
    
    cordova build android 
    
    or 
    
    cordova run android 
    
    or 
    
    cordova emulate android

----------
The Android platform in Cordova 5.0.0 requires Android SDK API Level 22. Install the SDK using the Android SDK manager.

----------
If you experience slow build performance and reliability issues when using the Crosswalk plugin, we recommend you add this plugin towards the end of your development as you are starting to finalize your app.

----------
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

----------
Visual Studio 2015 RC uses Ant to build Android while the command line has switched to Gradle by default in version 5.0.0 of the CLI. When switching between Visual Studio and the command line with the version of Android in Cordova 5.0.0, you may want to specify that the platform should be built with Ant instead if you are running into unexpected issues.

**Ex:**

    cordova build android -- --ant

You can also set an environment variable to keep this preference around for a command line session.

    set ANDROID_BUILD=ant

Finally, if you are still build errors, you may want to opt to remove and re-add the android platform after switching build systems.

    cordova platform remove android 
    cordova platform add android

----------
Ripple does not function properly in Cordova 5.0.0 due to a newly introduced validation check. This has already been fixed in Cordova main and will be resolved in a Cordova 5.x point release.
