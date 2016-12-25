<a name="top"></a>
# Accessing the configuration

To access the configuration of Sub-Zero, first select the Channels menu, and then press the little gear icon.
You can also access Sub-Zero's settings from the Agents menu in your PMS configuration.

![Channels](https://github.com/pannal/Sub-Zero.bundle/blob/master/Wiki/Images/Select_Channels.png)
![Select Gear Icon](https://github.com/pannal/Sub-Zero.bundle/blob/master/Wiki/Images/Select_Gear_Icon.png)

The configuration page will now show, and let's go through that in a couple of steps:

## Language configuration
![Language](https://github.com/pannal/Sub-Zero.bundle/blob/master/Wiki/Images/Settings-1-Language.png)

1. Subtitle language (1)/(2)/(3): Your preferred languages to download subtitles for
2. Additional Subtitle languages (Use [ISO-639-1 codes](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes), on a comma separated list)
3. Only download foreign/forced subtitles
4. Treat [IETF language](https://en.wikipedia.org/wiki/IETF_language_tag) tags as [ISO 639-1](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) (e.g. pt-BR = pt)
5. Restrict to one language (Only used if you only download for one language, and will avoid MyMedia.**LangCode**.srt)

## Provider configuration
![Provider](https://github.com/pannal/Sub-Zero.bundle/blob/master/Wiki/Images/Settings-2-Provider.png)

Sub-Zero allows you to select the best subtitle from multiple providers,thus providing a better match.

1. Download from OpenSubtitles if enabled. Add Username/Password for access to download more subtitles during each run
2. Download from Podnapisi.NET if enabled
3. Download from Addic7ed if enabled. Add Username/Password for access to download more subtitles during each run
4. Since Addic7ed tends to have better subtitles for Shows, you can by enabling this option boost the score of subtitles from Addic7ed, when compared to other enabled providers
5. Addic7ed: Use random user agent: Randomizes the user agent with which the Addic7ed service is being requested. Legacy feature, will be removed in one of the upcoming versions
6. Download from TVsubtitles.net if enabled

## Scanning configuration
![Scanning](https://github.com/pannal/Sub-Zero.bundle/blob/master/Wiki/Images/Settings-3-Scan.png)

1. I keep the exact (release-) filename of my media files: 
 * If you don't rename your media files automatically or manually and keep the original release's file names, enabling this option may help finding suitable subtitles for your media. Otherwise: disable this.
2. Scan: Include embedded subtitles: 
 * When enabled, subliminal finds embedded subtitles (ignoring forced) that are already present within the media file.
3. Scan: Include external subtitles: 
 * When enabled, subliminal finds subtitles located near the media file (or in the configured sub-folder) on the filesystem. (SideCars)
4. Scan: include "exotic" external subtitle formats (anything else than .srt/.ssa/.ass)
 * Enabling this if you got subtitles in other formats than above, but do note, that they most likely req. transcoding
5. Scores
 * Minimum score for TV-Show subtitle download (keep the default value for best results): 
  * When configured, what is the minimum score for subtitles to download them? Lower scored subtitles are not downloaded. See [here](https://github.com/pannal/Sub-Zero.bundle/wiki/Media-Score) for more info
 * Minimum score for Movie download (keep the default value for best results): 
  * When configured, what is the minimum score for subtitles to download them? Lower scored subtitles are not downloaded.See [here](https://github.com/pannal/Sub-Zero.bundle/wiki/Media-Score) for more info
6. Download hearing impaired subtitles:
 * "prefer": score subtitles for hearing impaired higher
 * "don't prefer": score subtitles for hearing impaired lower
 * "force HI": skip subtitles if the hearing impaired flag isn't set
 * "force non-HI": skip subtitles if the hearing impaired flag is set

<a name="store"></a>

## Subtitles storage configuration
![Storage](https://github.com/pannal/Sub-Zero.bundle/blob/master/Wiki/Images/Settings-4-Store.png)

1. Normalize subtitle encoding to UTF-8 (UTF-8 encoding is needed by most Plex Players)
2. Store subtitles next to media files (instead of metadata)
 * (default: current media file's folder) See [[Store as metadata or on filesystem|Store-as-metadata-or-on-filesystem]]
3. Custom Subtitle folder: 
 * See [[Store as metadata or on filesystem|Store-as-metadata-or-on-filesystem]]
4. Custom Subtitle folder
 * See [[Store as metadata or on filesystem|Store-as-metadata-or-on-filesystem]]
5. Fall back to metadata storage if filesystem storage failed
 * If PMS is running on Linux, or on Windows as a service, it has to have read/write rights to media storage, in order to be able to scan/save subtitle files next to the media. If that fails, we can instead store in the PMS Library
6. When saving a subtitle file next to a media, we can on a Linux platform stamp file-rights, if needed
7. When scanning a filestore, if we find "left-over" subtitles for a media, that has been deleted, we can delete it if needed

<a name="scheduler"></a>

## Scheduler configuration
![Scheduler](https://github.com/pannal/Sub-Zero.bundle/blob/master/Wiki/Images/Settings-5-Scheduler.png)

1. Scheduler: Periodically search for recent items with missing subtitles
 * Here you can specify a scheduled interval, where SZ can catch up on missing subs
2. Item age to be considered recent: 
 * The "Search for missing subtitles"-task only considers those items in the recently-added list, that are at most this old
3. Scheduler:
Periodically search for recent items with missing subtitles: 
 * self-explanatory, executes the task "Search for missing subtitles" from the channel menu regularly. Configure how often it should do that. For the average library 6 hours minimum is recommended, to not hammer the providers too heavily, since this could cause you to be banned for a period of time
4. Scheduler: Days to search for better subtitles (max: 30 days)
5. Scheduler: Overwrite manually selected subtitles when better found

<a name="develop"></a>
<a name="advanced"></a>

## Advanced configuration
![Advanced](https://github.com/pannal/Sub-Zero.bundle/blob/master/Wiki/Images/Settings-6-Misc.png)

1. Amount of data to store for the history
2. How many download tries per subtitle (on timeout or error): How often should we retry a failed subtitle download?
3. Ignore folders (...)
 * If a folder contains one of the files named `subzero.ignore`, `.subzero.ignore`, `.nosz`, don't process them. This applies to sections/libraries, movies, series, seasons, episodes
4. Ignore anything in the following paths (comma-separated)
5. Enable Sub-Zero channel.this will disable manual operation, but still allows Sub-Zero to work automatically
6. Call this executable upon successful subtitle download
 * Here you can specify a file to be executed after SZ finish downloading a subtitle
7. Check for correct folder permissions of every library on plugin start
 * if enabled, SZ checks for write permissions of your library folders and warns about them in the plugin channel
8. How verbose should the logging be?: 
 * Controls how much info SZ writes into the log files (default: only warnings) - this is decoupled from your PMS 
9. Log to console (for development/debugging): 
 * You know when you need it
10. Help the developers collecting anonymous usage statistics
 * Helps in planning new features

[[Next page|User-Guide]]

[[Back to main page|Home]]

[Go to top](#top)