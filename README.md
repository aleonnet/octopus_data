# Octopus Data App 🐙

[![Codemagic build status](https://api.codemagic.io/apps/5e8227914b4d3247a2739c79/5e8227914b4d3247a2739c78/status_badge.svg)](https://codemagic.io/apps/5e8227914b4d3247a2739c79/5e8227914b4d3247a2739c78/latest_build)
  
A Flutter application to read tariff and consumption data for Agile Octopus tariffs. I made this as an experiment and wanted to make it better but don't have a great deal of time. Feel free to use and contribute as you see fit!
If you are considering going with Octopus then please use my referral code: https://share.octopus.energy/witty-hyena-591
  
## Building  it
So far only built and tested for iOS and Android. Not tested on macOS or the Web although I'd love to see PRs to support that!
The app should import well into Android Studio or VS Code with the Flutter plugin. 
See https://flutter.dev/docs/get-started/install to get the tools installed.

To edit the app icons, change the files in `assets/icon/` and then run the following command in a terminal:

`flutter pub run flutter_launcher_icons:main`

See https://github.com/fluttercommunity/flutter_launcher_icons for more info.

## Using the app
  
If this is the first time you've run the app, you will be taken to a settings page for your API key and account credentials. Note that these are stored in the clear in a key/value store (SharedPreferences on Android, NSUserDefaults on iOS). Please don't use if that makes you uncomfortable.

To determine these:  
- Go to `https://octopus.energy/dashboard/developer/` and login to your Octopus Energy account.  
- Copy and past 2 curl commands (as shown in the settings screen) into the fields
- The app captures the following credentials from those commands (which are presented when you click Save):
  
```
String API_KEY = "[KEY]";  
String ELECTRICITY_MPAN = "[MPAN VALUE]";  
String ELECTRICITY_SERIAL = "[SERIAL NUMBER OF METER]";  

String TARIFF_CODE_1 = "[eg AGILE-18-02-21]";  
String TARIFF_CODE_2 = "[eg E-1R-AGILE-18-02-21-L]";  
```


When you first see the main screen there will be no data stored. The floating action button is used to query the API and save data to the phone's database (Sqlite under the hood).

## How to contribute
Fork the repository, make changes, and submit a pull request. There's plenty that can be done. I only ask that PRs are kept small and focused.

## Android screenshots

![some early hours high usage!](docs/android_debug.png) ![Dark mode build in](docs/android_debug_dark.png)

