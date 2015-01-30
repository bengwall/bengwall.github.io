---
published: true
layout: post
title: WebSQL and SQLite with Ionic
---

I want to create a mobile app and first mock the REST service.  To make my development and testing effecient, I want a solution where I can test the app in Chrome before I tested in the mobile emulators.  For the first iteration of the app, I used local storage to store the data in name/value pairs because it seemed so easy and is widely supported.  I used the [angular-local-storage module](https://github.com/agrublev/angularLocalStorage) which worked well.  The pattern of writing records in JSON to the local storage, however, broke down quickly as I got further in to the app.  Therefore, I started looking for a local SQL implementation.

There are a few choices for local SQL stores:  WebSQL, SQLite, and IndexDB. I quickly ruled out IndexDB because it does not run in web kit browsers which are Chrome & Safari.  WebSQL does work in Chrome & Safari, but has a size limit of 5mb.  That may be ok with a test application, but if I ever wanted this to be used in a production application, I would not want such a small limit.

I settled on trying to get SQLite to work with Ionic.  I found Nic Raboy's [post on SQLite and Ionic](https://blog.nraboy.com/2014/11/use-sqlite-instead-local-storage-ionic-framework/) and that was a great starting point.  His example using [ngCordova](http://ngcordova.com/) from the Ionic team and the [Cordova SQLite plugin](https://github.com/brodysoft/Cordova-SQLitePlugin) from Chris Brody worked great...  At least in the iOS and Android emulators.  

The SQLite plugin it turns out will not work with `ionic serve` because it relies on Cordova.   To work and debug directly in Chrome,  I needed to have a solution to work with `ionic serve`.  The solution ends up using WebSQL for local development and to switch over to SQLite for production.

Below is the code for SQLite.  This will work in the emulators.

```
.run(function($ionicPlatform, $cordovaSQLite) {
    $ionicPlatform.ready(function() {
        if(window.cordova && window.cordova.plugins.Keyboard) {
            cordova.plugins.Keyboard.hideKeyboardAccessoryBar(true);
        }
        if(window.StatusBar) {
            StatusBar.styleDefault();
        }
        db = $cordovaSQLite.openDB({ name: "my.db" });
        $cordovaSQLite.execute(db, "CREATE TABLE IF NOT EXISTS people (id integer primary key, firstname text, lastname text)");
    });
})
```

To switch to WebSQL for Chrome development, simply change the open database line as follows.

```
db = window.openDatabase("my.db", "1.0", "Cordova Demo", 200000);
```