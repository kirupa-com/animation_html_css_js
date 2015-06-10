#**General Known Issues**

----------
The “Solution Platform” dropdown may not appear in the toolbar when upgrading Visual Studio 2013 from a previous version to Update 4. You can add using the “Standard Toolbar Options” dropdown as described in [Microsoft Support article 2954109](http://support.microsoft.com/kb/2954109).

----------
If you already had the Android SDK installed, you may also need to update and install the SDK for Android 4.4.x (API level 19). You may need to restart Visual Studio if it is open while updating the Android SDK through the SDK Manager to be able to build for Android after the update is complete. See [Manually Installing Dependencies](https://msdn.microsoft.com/en-us/library/dn757054.aspx#ThirdParty) for details.

----------
In some circumstances, when deploying to iOS devices, they phone may enter an unresponsive state where apps may stops responding. Avoid deploying an app when the same app is still running. 
As a workaround, if you enter this state, soft reset your iOS device.

----------
While setting a PIN for secure iOS builds, if you later re-open the Remote Agent Configuration options page, clicking "OK" will clear the PIN and revert to non-secure builds unless you re-enter a PIN. 

As a work-around, either hit "Cancel" whenever you re-open the options page to Remote Agent Configuration, or re-enter a new PIN.

----------
Plugins will be re-downloaded after a “clean” operation. Developers should specify a version number or reference the plugins locally when using third-party plugins. See the [Plugins](https://msdn.microsoft.com/en-us/library/dn757051.aspx) section for details.

----------
The contents of the “res” folder cannot be accessed by web content as they are copied into platform-specific native project locations.

----------
Not all iOS Simulator devices are currently listed in the Debug Target dropdown in Visual Studio. A workaround is to manually change the device using the iOS Simulator Hardware > Device menu.

----------
If a plugin is added to your project, built for iOS, and then removed from the project, the plugin will still be included in the iOS build until you clean or build for another platform. As a workaround, clean or rebuild instead of build.

----------
The first time you launch Visual Studio after installing the Tools for Apache Cordova extension, IntelliSense will not work for the Apache Cordova™ object or other Cordova plugins. Please restart Visual Studio to fix the problem.

----------
When using TypeScript, there are known issues that will incorrectly identify project items as external code or will fail to read in a user configuration file. To avoid unexpected behavior when working with a Cordova TypeScript project, turn off Just My Code (Options > Debugger > General > uncheck Enable Just My Code).

----------
The project name automatically sets the display name in config.xml. If you encounter a build error because of this problem, set your system locale, then clean your project and rebuild.

----------
During installation, if your “My Documents” path redirects to a server share location, install the MSI from“%localappdata%\Microsoft\MultiDeviceHybridApps” instead.

----------
Dragging a mixed-case file into an HTML page creates a lowercase reference which will cause it to not be found on Android and iOS. Manually update the reference with the correct casing.
