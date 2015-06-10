#**Known Issues: Visual Studio 2015 RC**

----------
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

----------
When you upgrade from VS2015 CTP5 to CTP6, Apache Ant gets uninstalled. The workaround is to reinstall Ant. You can find manual instructions for installing and configuring Ant at [this location](https://msdn.microsoft.com/en-us/library/dn757054.aspx#InstallTools).

----------
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
