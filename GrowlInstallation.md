# Instructions to install `S`potifyNotifierGrowl previous versions #

## Version 1.0 ##

  1. First of all make sure you have **growl** installed on your system. It can be downloaded from http://www.growlforwindows.com/gfw/default.aspx
  1. Now go to the installation directory of growl.For me it is _C:\Program Files\Growl for Windows_ and check you have **growlnotify.exe** in that folder.
  1. Now add the above mentioned directory to the **path system variable** under windows environment variable.

To check growlnotify is added to path, write the below line of code in **command prompt**.

```
C:\Users\RanRag>growlnotify "hello world"
```

It will show a notification on your desktop.

#### Register the application ####

Before using spotifynotifier you have to register the application. Open command prompt and write the following commands.

  * To register
```
growlnotify /r:Spotify /a:Spotify test
```

  * Try sending a test message to growl from your registered application
```
growlnotify /t:"hello" /n:"Spotify" /a:"Spotify" "test message"
```

It will look something like

<a href='http://imgur.com/O284v'><img src='http://i.imgur.com/O284v.jpg' alt='' title='Hosted by imgur.com' /></a>


## Version 1.1 ##

  1. First of all make sure you have **growl** installed on your system. It can be downloaded from http://www.growlforwindows.com/gfw/default.aspx
  1. Now go to the installation directory of growl.For me it is _C:\Program Files\Growl for Windows_ and check you have **growlnotify.exe** in that folder.

## How to use ##

  1. Download **`S`potify`N`otifier`G`rowl\_ver1.1.zip**.
  1. Extract the content of zip file.
  1. Now need to register the application like we use to do in version 1.0 just run **`S`potify`N`otifier`G`rowl.exe**

Now if you have installed `Growl` in any directory other than _C:\Program Files\Growl for Windows_ than

  1. Open **`N`otify`G`rowl.cs** and replace `ApplicationName` variable's value with your path.

```

 private string ApplicationName = "C:\\Program Files\\Growl for Windows\\growlnotify.exe"; 

```

  1. Now move to folder which contain all the project files (**.cs files**) and recompile it using the below command in command prompt.
  1. Before compiling change **vXXX** to your **.NET** version.

```

C:\Windows\Microsoft.NET\Framework\vXXX\csc.exe  /out:SpotifyNotifierGrowl.exe *.cs

```

  1. Now run `S`potify`N`otifier`G`rowl.exe.

Now change the track in spotify and you will see

<a href='http://imgur.com/NmUON'><img src='http://i.imgur.com/NmUON.jpg' alt='' title='Hosted by imgur.com' /></a>

## Change Growl look and feel ##

You can add custom **icon** to the notification. To do that

  1. Replace _`A`pplication`A`rguments_ with below line of code in **`N`otify`G`rowl.cs** file and also replace **C:\\spotify.png** by the path of your image
```
 string ApplicationArguments = string.Format("/t:\"Song: {0}\" /i:\"C:\\spotify.png\" /n:\"Spotify\" /a:\"Spotify\" \"Artist: {1}\"",track,artist);
```
  1. Now move to folder which contain all the project files (**.cs files**) and recompile it using the below command in command prompt.
  1. Before compiling change **vXXX** to your **.NET** version.
```
C:\Windows\Microsoft.NET\Framework\vXXX\csc.exe  /out:SpotifyNotifierGrowl.exe *.cs
```
  1. Now run `S`potify`N`otifier`G`rowl.exe.

**Note**: For syntax of the above command refer http://www.growlforwindows.com/gfw/help/growlnotify.aspx