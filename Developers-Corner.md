[![GitHub issues](https://img.shields.io/github/issues/dagalufh/WebTools.bundle.svg?style=flat)](https://github.com/dagalufh/WebTools.bundle/issues) [![Github All Releases](https://img.shields.io/github/downloads/pannal/Sub-Zero.bundle/total.svg?maxAge=2592000)]()

If you are a developer, that wants to help/add to Sub-Zero, then please read ahead

## Installation:
In order to allow your development to not be overwritten automatically by the Plex Media Server, you should follow the following installation procedure:

### Manual/Development/Testing Installation

* go to Library/Application Support/Plex Media Server/Plug-ins/
* rm -r Sub-Zero.bundle (remove the folder if it already exists) (If running windows, simply delete the directory from explore)
* get the release you want from [https://github.com/pannal/Sub-Zero.bundle/releases/](https://github.com/pannal/Sub-Zero.bundle/releases/)
* unzip the release into Library/Application Support/Plex Media Server/Plug-ins/
* edit Contents/Info.plist and set <key>PlexPluginDevMode</key>'s value to <string>1</string> to avoid automatic updates with the stable release to your manual installation
* restart your plex media server!!!

### Logging to console:

During development, it might be useful to enable [[Console logging|Configuration#wiki-develop]], but do note, that if no console is running, some platforms will error out then

[[Back to main page|Home]]