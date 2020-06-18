# Android-Note-Study
Record for Android used Reference list

## Tools

Source In Sight - Friendly for AOSP Editer

Android Studio - Android Application IDE

Zulu open JDK - open source for java develop kit

Vysor - google Application for remote control Android device with usb line

ADB(Android Debug Bridge) - cmd to interaction with Android device

DB Browser for SQLite - for open local db file in Android App package in device

Draw.io - flow chart web editor tool

## Useful open source libs

nanohttpd - httpServer in Android

GreedDao - local sql database lib

### some customer references

文繞圖 : https://blog.csdn.net/zhangtongyuan0909/article/details/54864294

### bindService

How to use bindService

ref : https://blog.csdn.net/iispring/article/details/48169339



## Build Config

### set apk name when build in grandle

ref : https://www.tanelikorri.com/tutorial/android/set-apk-filename-in-gradle/

## Record some method

### List SSIDs of stored networks

des : List stored networks

ref : https://stackoverflow.com/questions/3531940/how-to-get-name-of-wifi-network-out-of-android-using-android-api/15976165

pre prepare : 

add permissions about Wifi access

code 

    // List stored networks, this method exec normally needed WifiEnable as ture
    WifiManager wm = (WifiManager) getApplicationContext().getSystemService(WIFI_SERVICE);  
    List<WifiConfiguration> configs = wm.getConfiguredNetworks();
    String connRecord = "List stored networks : \n";
    for (WifiConfiguration config : configs) {
        connRecord += "\n" + config.SSID;
    }
    Log.i(TAG, connRecord);
