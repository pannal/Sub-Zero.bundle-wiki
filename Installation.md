## Automatic Installation (Normal installation)
Sub-Zero is part of the Official Plex Channel Directory, so to install it, look [here](https://support.plex.tv/hc/en-us/articles/201053758)

## Manual/Development/Testing Installation

* go to Library/Application Support/Plex Media Server/Plug-ins/
* rm -r Sub-Zero.bundle (remove the folder if it already exists) (If running windows, simply delete the directory from explore)
* get the release you want from [https://github.com/pannal/Sub-Zero.bundle/releases/](https://github.com/pannal/Sub-Zero.bundle/releases/)
* unzip the release into Library/Application Support/Plex Media Server/Plug-ins/
* edit Contents/Info.plist and set <key>PlexPluginDevMode</key>'s value to <string>1</string> to avoid automatic updates with the stable release to your manual installation
* restart your plex media server!!!

[Back](https://github.com/pannal/Sub-Zero.bundle/wiki)