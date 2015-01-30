---
published: true
layout: post
---

### Installation

- Install the Ionic framework if it is not installed yet:  
	- `$ npm install -g cordova ionic gulp ios-sim`

>	If you already have ionic installed you can see you version by `$ ionic -version`.  '$ npm update' will update any npm packages.

- **OPTIONAL:** Install the Android SDK & Emulator (if you want to target Android): 
	- `$ brew install ant`.  To see the version:  `$ ant -version`
    - `$ brew install android-sdk` installs it to `/usr/local/opt/android-sdk/23.0.2` 
    
    >	`$ brew update` will update brew.  `$ brew upgrade` will upgrade all brew features.
    
    - ``$ export ANDROID_HOME=`brew --prefix android` `` or `$ export ANDROID_HOME=/usr/local/opt/android-sdk`
    - Install sdk 19
    
    	- `$ tools/`
        - `$ android sdk`
        - Select `Android 4.4.2 (API 19)` and Install.
    
    - Emulator Option #1:  Install Genymotion emulator for Android.  This is the preferred method because the Android emulator is so slow.

        - Goto [Genemotion](https://www.genymotion.com/) and sign up for a new account
        - Follow these [instructions](https://www.genymotion.com/?utm_source=dlvr.it&utm_medium=twitter#!/developers/user-guide) to download and install Genemotion.

            - NOTE: You will need to install VirtualBox first if running on OS X
            - The Ionic page on Genymotion is [here](http://ionicframework.com/docs/ionic-cli-faq/#genymotion)
            - NOTE: Running in a virtual Android 4.4 and above device will run slow because of the switch to use the new Cromeview imbeded browser.  The solution is to target the vitual device to 4.2.2.

    - Emulator Option #2:  Use the Android emulator

    	- Create an emulator (avd). I created a adv called `my19`:
        
            - `$ android create avd -n my19 -t android-19 -b default/x86`
            - `$ android avd` will allow you to edit the adv or enter new ones.

    	- Install HAXM.  This is hardware accelerator required for the emulator.
        
        	- Download the [zip file](https://software.intel.com/en-us/android/articles/intel-hardware-accelerated-execution-manager) for the Mac.
            - Install `IntelHAXM_1.1.1_for-10_9_and_above.dmg`
    


### Create a test app

```
$ ionic start myApp tabs (start with the tabs app, you can also start with ‘blank’ or ’sideMenu’)
$ cd myApp
$ ionic platform add ios
$ ionic platform add android
```

### Run in the iOS emulator _(ctrl-C to exit)_

```
$ ionic build ios
$ ionic emulate ios
```

>	`command-shift-h` then `h` again simulates double tapping the home button.

>	Alternatively, you should probably do most of your testing in your browser with `$ ionic serve`, as it's much quicker (note: features such as the camera will not be available for testing if you use this method).

>	When in the iOS simulator you can view `console.log` line by double-clicking `\<app dir>\platforms\ios\cordova\console.log`.

### Run in the Android emulator _(ctrl-C to exit)_

```
$ ionic build android
$ ionic emulate android

--- for Genymotion do the following:

$ ionic run android
```



### Resouces

- Ionic Guide: http://ionicframework.com/docs/guide/installation.html 
- Max’s video walkthrough:  https://www.youtube.com/watch?v=C-UwOWB9Io4&feature=youtu.be
- Android help:
	- http://dara.azurewebsites.net/ionic-android-osx/
    - http://ionicframework.com/docs/ionic-cli-faq/#android-sdk