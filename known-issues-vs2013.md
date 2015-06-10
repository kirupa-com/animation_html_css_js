#**Known Issues - CTP 3.1 for Visual Studio 2013**

----------
While trying to associate a Cordova app with Windows store using Visual Studio 13 and CTP3.1 , the AppxManifest.xml doesn’t get updated with the appropriate Application Id & publisher name. We have fixed this issue in VS2015 RC. To fix this issue, install the plugin from [https://github.com/Chuxel/taco-tricks/tree/master/plugin-windows-package-fix](https://github.com/Chuxel/taco-tricks/tree/master/plugin-windows-package-fix) and try building your application again.

----------
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

