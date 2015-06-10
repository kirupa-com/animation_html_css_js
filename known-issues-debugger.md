#**VS Debugger Known Issues and Limitations**

----------
There is currently no Visual Studio debugger support for Windows Phone 8. Developers can use the Weinre (Web Inspector Remote) project as described in this [blog post](http://msopentech.com/blog/2013/05/31/now-on-ie-and-firefox-debug-your-mobile-html5-page-remotely-with-weinre-web-inspector-remote/) from MS OpenTech as an alternative.

----------
When debugging an application deployed to the Ripple emulator, the JavaScript Console's default execution target is the Ripple top-level, instead of the application frame. To switch to the execution target of the user’s application, change the execution target of the JavaScript Console to the "frame: <application html page>" target using the target selector in the upper right of the JavaScript Console window.

----------
You cannot use the VS Debugger for apps deployed to Android emulators or devices that are built in the Release or Distribution Solution Configurations (by design) as they are signed. JavaScript console output is, however, captured in the Output window.

----------
Due to an issue with the InAppBrowser plugin, we currently do not support debugging on iOS applications that utilize it. The Azure Mobile Services plugin depends on InAppBrowser and is affected by this issue.

**When using the VS Debugger with Android < 4.4 emulators, devices, or Apache Ripple™:**

----------
You cannot use the VS Debugger for apps deployed to emulators or devices running Android versions prior to 4.4. JavaScript console output is, however, captured in the Output window.

----------
While debugging to devices with Android versions <4.4, an error popup shows up “Unable to start program” citing “adb.exe” as the cause. The app should still load and work on your device, without debugger support.

**When using the VS Debugger with Android 4.4 emulators, devices, or Apache Ripple™:**

----------
The VS Debugger will not stop at breakpoints that occur prior to the first page load in Ripple or Android emulators or devices. However, these breakpoints will be hit after refreshing the browser (Ripple) or executing “window.location.reload()” from the JavaScript Console.

----------
If you start up Chrome Dev Tools in Ripple when debugging from VS, Ripple will shut down. To use Chrome Dev Tools, start without debugging (Ctrl+F5).

----------
Breakpoint stop and step through performance degrades significantly with large projects when debugging against an Android 4.4 device or emulator.

----------
An HTML file will only appear under Script Documents in the Solution Explorer if the HTML file contains code that can still run in the engine.

----------
Only script blocks that contain code that can still run will be visible.

----------
If an HTML file only contains script that ran and was immediately unloaded, the HTML will never appear in the Solution Explorer.

----------
Not all JavaScript Console APIs are available.

----------
DOM Explorer Events and Changes panes are not available.

**When using jsHybugger for debugging Android <4.4:**

----------
While using the JS Debugger with jsHybugger, there is no support for Source Maps.

----------
While using the DOM explorer with jsHybugger, there is no support for:

 - Deleting CSS properties
 - Selecting DOM elements by clicking on them
 - Add/edit/delete of element attributes
 - Add/edit of CSS rules
 - Forcing Hover and Visited Pseudo-class states
 - Undo/redo
 - Edit as HTML
 - Shorthand property display is generally not supported.

----------
While using the JavaScript Console with the jsHybugger, the JS Console works as output only – messages are logged but we do not execute commands.  We also do not support source locations of messages, clearing messages on navigation, and expanding objects and properties of the logged messages.
