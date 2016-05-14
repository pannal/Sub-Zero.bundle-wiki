# Accessing the configuration

To access the configuration of Sub-Zero, first select the Channels menu | Then press the little gear icon

![Channels](https://github.com/pannal/Sub-Zero.bundle/blob/master/Wiki/Images/Select_Channels.png)
![Select Gear Icon](https://github.com/pannal/Sub-Zero.bundle/blob/master/Wiki/Images/Select_Gear_Icon.png)

The configuration page will now show, and let's go through that in a couple of steps:

![Conf1](https://github.com/pannal/Sub-Zero.bundle/blob/master/Wiki/Images/Conf-1.png)

1. Enable Sub-Zero channel.this will disable manual operation, but still allows Sub-Zero to work automatically
2. How many download tries per subtitle (on timeout or error): How often should we retry a failed subtitle download?
3. Your Plex.tv User name (This will not be needed in the next version)
4. Your Plex.tv Password (This will not be needed in the next version)
5. Addic7ed username: 
 * Provide your addic7ed username here, otherwise the provider won't work. Please make sure your account is activated, before using the agent
6. Addic7ed password for your account
7. Opensubtitles username: Generally recommended to be provided (not necessarily needed, but avoids errors, and increase the amount of subtitles you can download)
8. Opensubtitles password for your account
9. Addic7ed: Use random user agent **THIS IS UNKNOWN TO ME**
10. Subtitle language (1)/(2)/(3): Your preferred languages to download subtitles for

![Conf-2](https://github.com/pannal/Sub-Zero.bundle/blob/master/Wiki/Images/Conf-2.png)

1. Additional Subtitle languages (Use [ISO-639-1 codes](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes), on a comma separated list)
2. Restrict to one language (skips adding ".lang." to the subtitle filename; only uses "Subtitle Language (1)")
3. Normalize subtitle encoding to UTF-8 (UTF-8 encoding is needed by most Plex Players)
4. Provider: Enable ...: 
 * Enable/disable this provider. Affects both movies and series
5. Addic7ed: (TV only) boost over hash score if requirements met: 
 * if an Addic7ed subtitle matches the video's series, season, episode, year, boost its score, possibly over OpenSubtitles/TheSubDB direct hash match. Recommended for higher quality subtitle results.

![Conf-3](https://github.com/pannal/Sub-Zero.bundle/blob/master/Wiki/Images/Conf-3.png)

1. I keep the exact (release-) filename of my media files: 
 * If you don't rename your media files automatically or manually and keep the original release's file names, enabling this option may help finding suitable subtitles for your media. Otherwise: disable this.
2. Scan: Include embedded subtitles: 
 * When enabled, subliminal finds embedded subtitles (ignoring forced) that are already present within the media file.
3. Scan: Include external subtitles: 
 * When enabled, subliminal finds subtitles located near the media file on the filesystem. (SideCars)
4. Minimum score for TV-Show download: 
 * When configured, what is the minimum score for subtitles to download them? Lower scored subtitles are not downloaded.
5. Minimum score for Movie download: 
 * When configured, what is the minimum score for subtitles to download them? Lower scored subtitles are not downloaded.
6. Download hearing impaired subtitles:
 * "prefer": score subtitles for hearing impaired higher
 * "don't prefer": score subtitles for hearing impaired lower
 * "force HI": skip subtitles if the hearing impaired flag isn't set
 * "force non-HI": skip subtitles if the hearing impaired flag is set

![Conf-4](https://github.com/pannal/Sub-Zero.bundle/blob/master/Wiki/Images/Conf-4.png)

1. Store subtitles next to media files (instead of metadata): 
 * See Store as metadata or on filesystem
2. Subtitle folder: 
 * (default: current media file's folder) See Store as metadata or on filesystem
3. Custom Subtitle folder: 
 * See Store as metadata or on filesystem
4. Treat [IETF language tags](https://en.wikipedia.org/wiki/IETF_language_tag) as ISO 639-1: 
 * Treats subtitle files with IETF language identifiers, such as pt-BR, as their ISO 639-1 counterpart. Thus "pt-BR" will be shown as "Portuguese" instead of "Unknown"

![Conf-5](https://github.com/pannal/Sub-Zero.bundle/blob/master/Wiki/Images/Conf-5.png)

1. Ignore folders (...): 
 * If a folder contains one of the files named subzero.ignore, .subzero.ignore, .nosz, don't process them. This applies to sections/libraries, movies, series, seasons, episodes
2. Scheduler:
Periodically search for recent items with missing subtitles: 
 * self-explanatory, executes the task "Search for missing subtitles" from the channel menu regularly. Configure how often it should do that. For the average library 6 hours minimum is recommended, to not hammer the providers too heavily, since this could cause you to be banned for a period of time
3. Item age to be considered recent: 
 * The "Search for missing subtitles"-task only considers those items in the recently-added list, that are at most this old
4. Recent items to consider per library: 
 * How many items to consider for every section/library you have - used in "Search for missing subtitles"-task and "Items with missing subtitles"-menu. Change at your own risk!

![Conf-6](https://github.com/pannal/Sub-Zero.bundle/blob/master/Wiki/Images/Conf-6.png)

1. Check for correct folder permissions of every library on plugin start: 
 * if enabled, SZ checks for necessary permissions of your library folders and warns about them in the plugin channel
2. How verbose should the logging be?: 
 * Controls how much info we write into the log files (default: only warnings)
3. Log to console (for development/debugging): 
 * You know when you need it

[Back](https://github.com/pannal/Sub-Zero.bundle/wiki)
