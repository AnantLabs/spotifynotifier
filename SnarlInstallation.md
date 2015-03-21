# Instructions to install `S`potifyNotifierSnarl previous versions #

## Version 1.0 ##

  1. First of all make sure you have snarl installed on your system. It can be downloaded from http://snarl.fullphat.net/.
  1. Now go to _C:\Program Files\full phat\Snarl\tools_ and check you have **heysnarl.exe** present there.
  1. Now add the above mentioned directory to the **path system variable** under windows environment variable.
  1. Before using check whether **heysnarl.exe** is added to the path or not. To do that write the below line of code in command prompt.

```
heysnarl "register?app-sig=app/Spotify&title=test message"
heysnarl "notify?app-sig=app/Spotify&title=Hello, World&text=test message"
```

It will look something like

<a href='http://imgur.com/IKBfZ'><img src='http://i.imgur.com/IKBfZ.jpg' alt='' title='Hosted by imgur.com' /></a>

## How to use ##

  1. Download **`S`potify`N`otifer`S`narl.zip**.
  1. Extract the content of zip file.
  1. Open Spotify and run the **.exe** file present in the downloaded zip file.

## Change Snarl look and feel ##


You can add custom **icon** to the notification. To do that

  1. Replace `A`pplication`A`rguments with below line of code in **`N`otify`S`narl.cs** file and also replace **C:\\spotify.png** by the path of your image.
```
string ApplicationArguments = string.Format("notify?app-sig=app/Spotify&title=Song: {0}&text=Artist: {1}&icon=C:\\spotify.png",track,artist);
```
  1. Now move to folder which contain all the project files (**.cs files**) and recompile it using the below command in command prompt.
  1. Before compiling change **vXXX** to your **.NET** version.
```
C:\Windows\Microsoft.NET\Framework\vXXX\csc.exe  /out:SpotifyNotifierSnarl.exe *.cs
```
  1. Now run `S`potify`N`otifier`S`narl.exe.


**Note**: For syntax of the above command refer
http://sourceforge.net/apps/mediawiki/snarlwin/index.php?title=Generic_API