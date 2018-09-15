# Qt and RingQt for android Splash logo trick

This repo contains some files prepared to hide two stage (Black and White) default splash for Android apps created by Qt or RingQt.

        Note: Its highly recommanded that you set up this trick at clean newly created project, to avoid 
        rewriting some previously modified building template.

## Usage

- Open QtCreator.

- Create a new porject Or open an existed one.

- Create a new building template (Projects Mode ==> Building kit [ex. Android for armeabi-v7a] ==> Build ==> Build Steps ==> Build Android APK ==> Details ==> Create Template ==> Set the required location of template files [By default its a "android" folder in your project folder] ==> Finish).

- Copy the files from the "android" folder in this repo and paste them in the location of template files and accept overwriting them.

        Note: Be careful in case you have made some changes to "AndroidManifest.xml" file because 
        it will be overwritten.

      ** In case you have made some changes to the "AndroidManifest.xml" and don't want to lose them just DO THIS:
   
        1- Under ((<!-- Splash screen -->)) line you need to uncomment ((<!-- meta-data 
        android:name="android.app.splash_screen_drawable" android:resource="@drawable/logo"/ -->)) line.
    
        2- Inside ((<activity android:configChanges= ......>)) line add ((android:theme="@style/AppTheme")).
        
       So that there's no need to overwrite "AndroidManifest.xml" file.

- Change the splash pictures in the "drawable-xdpi" folders in the "res" folder to what ever you want, take care of the resolution for each one and their filenames should as same as they are.

        Note: hdpi folder for high resolution devices, mdpi for intermediate and ldpi for low ones.

- And You Are Done.


Now, try to build your project and see the results.

This method has been taken from more than one source and modified to just allow showing Only the splash picture we specify in this way.

        Note: This trick has been tested by QtCreator 5.11.0 to build application 
        for android 21 api armeabi-v7a.


## Screan sizes and resolutions

Here's how other smallest width values correspond to typical screen sizes [(Android Docs)](https://developer.android.com/training/multiscreen/screensizes):

- 320dp: a typical phone screen (240x320 ldpi, 320x480 mdpi, 480x800 hdpi, etc).
- 480dp: a large phone screen ~5" (480x800 mdpi).
- 600dp: a 7” tablet (600x1024 mdpi).
- 720dp: a 10” tablet (720x1280 mdpi, 800x1280 mdpi, etc).




