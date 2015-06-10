#**Known Issues - iOS Build**

----------
After installing the latest version of [vs-mda-remote package](https://www.npmjs.com/package/vs-mda-remote), you will need to run the following commands before you start up the remote agent. These commands ensure your user has permissions to the contents of the npm package cache in your home directory when using older versions of Node.js and npm. Newer versions of Node.js and npm will do this for you automatically.

    sudo npm cache clear 
    sudo chown -R `whoami` ~/.npm

----------
If deploying to iOS 8.3 device fails because vs-mda-remote cannot find DeveloperDiskImage.dmg, ensure you are running OSX Yosemite and Xcode 6.3. Xcode 6.3 is required to deploy to an 8.3 device and only runs on Yosemite.

----------
Cordova plugins that contain custom frameworks like the Facebook Connect plugin may experience compilation errors when building for iOS due to missing symlinks. As a workaround, use the following Cordova hook, clean the solution, and try again: [https://github.com/Chuxel/taco-tricks/tree/master/ios-plugin-symlink-fix](https://github.com/Chuxel/taco-tricks/tree/master/ios-plugin-symlink-fix) 
