#**Apache Cordova and Ripple-Related Issues**
----------
Due to a coding error, the Windows Cordova platform has a temporary key in it that expired on 11/11/2014. We are actively working with the community on long term fix. To work around this issue, [download this file](https://git-wip-us.apache.org/repos/asf?p=cordova-windows.git;a=blob;f=template/CordovaApp_TemporaryKey.pfx;h=90d7ab2208ce170d176a2ac8a60eb22fbc1cbf7a;hb=refs/tags/3.7.1) and place it in your Tools for Apache Cordova project in following location:

- CTP 1 or 2: res/cert/windows8/CordovaApp_TemporaryKey.pfx
- CTP 3: res/native/windows/CordovaApp_TemporaryKey.pfx

You can read more about the issue on the [MS Open Tech blog](http://go.microsoft.com/fwlink/?linkid=518810).

----------
Apps with certain non-Western characters in their Display Name may not build for iOS due to a known Cordova issue.

----------
Projects with non-Western characters in their project names or in the project path may not build for Android due to an Android SDK issue. You can workaround this by simply changing the project name and path to use western characters.

----------
When the Console plugin is used with the Cordova CLI or Visual Studio on Windows Phone 8, console output is not flushed until after an emulator or device is disconnected. Use Weinre (Web Inspector Remote) project as described in this blog post from MS OpenTech as an alternative.

----------
When using the Camera plugin with Ripple and the DATA_URL option, a file reference is returned instead.

----------
No IntelliSense is provided for Cordova plugins in JavaScript files in Apache Cordova projects. As a workaround, developers can enable IntelliSense for Cordova plugins by explicitly adding “/// <reference group="Implicit (Multi-Device Apps)” />” to the JavaScript file.

----------
No IntelliSense is provided within JavaScript files for other JavaScript files included via a script tag in a referring HTML page. As a workaround, developers can enable IntelliSense for other referenced JavaScript files by explicitly adding “/// <reference path=”referencedFile.js” />” to the JavaScript file.
