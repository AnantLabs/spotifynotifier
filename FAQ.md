## Frequently Asked Questions ##

### 1) Can I download the zip file from alternate sources? ###
Yes, you can download the file from **Github**. There are basically two ways to get the file from github:

#### Method 1 ####

If you have **Git** installed on your system you can do
```
git clone https://github.com/ranveer5289/SpotifyNotifier-Windows.
```

#### Method 2 ####

Alternatively you can download the zip file from the github repo https://github.com/ranveer5289/SpotifyNotifier-Windows.


### 2) Why am I getting `"W`indows cannot open the folder. The Compressed (zipped) folder `'S`potifyNotifier`*`.zip`'` is invalid`"` error when trying to extract the zip file? ###

#### User Suggested Solution ####

Try opening the file with something other than Window's built-in zip file viewer like WinRAR or 7Zip.


### 3) `S`potify`N`otify`G`rowl crashes on `W`in7 x64 machine. ###

The problem is occuring with versions 1.0 & 1.1.

Check issue http://code.google.com/p/spotifynotifier/issues/detail?id=2

### 4) `S`potify`N`otifier`S`narl Keeps `U`nregistering itself. ###

This is a known bug with Snarl v2.5.1. It is mentioned at http://snarl-development.blogspot.in/2012/01/snarl-251-available.html and is also duscussed at http://goo.gl/xmxIU.

#### Solution ####

> Use Snarl version < 2.5.1 or use the latest version of Snarl i,e [R3](https://code.google.com/p/spotifynotifier/source/detail?r=3).0 Beta1

### 5) How to compile the **.cs** file of latest `S`potify`N`otifier`G`rowl version? ###

The latest version `S`potify`N`otifier`G`rowl(ver 1.2) uses the growl API(.dll files).

So, in order to compile the .cs file with .dll files use the follwing command
```
C:\Windows\Microsoft.NET\Framework\vXXXX\csc.exe /r:Growl.Connector.dll,Growl.CoreLibrary.dll /out:SpotifyNotifierGrowl.exe *.cs
```

Change XXXX with the **.Net** version installed on your system.

### 6) How can I send my application to system tray after execution? ###

There is no native support for that but you can use [PowerMenu](http://www.abstractpath.com/powermenu/) to send application to system tray.