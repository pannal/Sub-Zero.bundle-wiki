<a name="top"></a>
# Accessing the configuration

To access the configuration of Sub-Zero, first select the Channels menu, and then press the little gear icon.
You can also access Sub-Zero's settings from the Agents menu in your PMS configuration.

![Channels](https://github.com/pannal/Sub-Zero.bundle/blob/master/Wiki/Images/Select_Channels.png)
![Select Gear Icon](https://github.com/pannal/Sub-Zero.bundle/blob/master/Wiki/Images/Select_Gear_Icon.png)

The configuration page will now show, and let's go through that in a couple of steps:

## Basic configuration
![Conf1](https://github.com/pannal/Sub-Zero.bundle/blob/master/Wiki/Images/Conf-1.png)

1. Enable Sub-Zero channel.this will disable manual operation, but still allows Sub-Zero to work automatically
2. How many download tries per subtitle (on timeout or error): How often should we retry a failed subtitle download?
3. Addic7ed username: 
 * Provide your addic7ed username here, otherwise the provider won't work. Please make sure your account is activated, before using the agent
4. Addic7ed password for your account
5. Opensubtitles username: Generally recommended to be provided (not necessarily needed, but avoids errors, and increase the amount of subtitles you can download)
6. Opensubtitles password for your account
7. Addic7ed: Use random user agent: Randomizes the user agent with which the Addic7ed service is being requested. Legacy feature, will be removed in one of the upcoming versions
8. Subtitle language (1)/(2)/(3): Your preferred languages to download subtitles for

## Language and provider configuration
![Conf-2](https://github.com/pannal/Sub-Zero.bundle/blob/master/Wiki/Images/Conf-2.png)

1. Additional Subtitle languages (Use [ISO-639-1 codes](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes), on a comma separated list)
2. Restrict to one language (skips adding ".lang." to the subtitle filename; only uses "Subtitle Language (1)")
3. Normalize subtitle encoding to UTF-8 (UTF-8 encoding is needed by most Plex Players)
4. Provider: Enable ...: 
 * Enable/disable this provider. Affects both movies and series
5. Addic7ed: (TV only) boost over hash score if requirements met: 
 * if an Addic7ed subtitle matches the video's series, season, episode, year, boost its score, possibly over OpenSubtitles/TheSubDB direct hash match. Recommended for higher quality subtitle results.

## Library, scoring and scanning configuration
![Conf-3](https://github.com/pannal/Sub-Zero.bundle/blob/master/Wiki/Images/Conf-3.png)

1. I keep the exact (release-) filename of my media files: 
 * If you don't rename your media files automatically or manually and keep the original release's file names, enabling this option may help finding suitable subtitles for your media. Otherwise: disable this.
2. Scan: Include embedded subtitles: 
 * When enabled, subliminal finds embedded subtitles (ignoring forced) that are already present within the media file.
3. Scan: Include external subtitles: 
 * When enabled, subliminal finds subtitles located near the media file (or in the configured sub-folder) on the filesystem. (SideCars)
4. Minimum score for TV-Show download (keep the default value for best results): 
 * When configured, what is the minimum score for subtitles to download them? Lower scored subtitles are not downloaded. See [here](https://github.com/pannal/Sub-Zero.bundle/wiki/Media-Score) for more info
5. Minimum score for Movie download (keep the default value for best results): 
 * When configured, what is the minimum score for subtitles to download them? Lower scored subtitles are not downloaded.See [here](https://github.com/pannal/Sub-Zero.bundle/wiki/Media-Score) for more info
6. Download hearing impaired subtitles:
 * "prefer": score subtitles for hearing impaired higher
 * "don't prefer": score subtitles for hearing impaired lower
 * "force HI": skip subtitles if the hearing impaired flag isn't set
 * "force non-HI": skip subtitles if the hearing impaired flag is set

<a name="store"></a>

## Subtitles storage location and naming configuration
![Conf-4](https://github.com/pannal/Sub-Zero.bundle/blob/master/Wiki/Images/Conf-4.png)

1. Store subtitles next to media files (instead of metadata): 
 * See [[Store as metadata or on filesystem|Store-as-metadata-or-on-filesystem]]
2. Subtitle folder: 
 * (default: current media file's folder) See [[Store as metadata or on filesystem|Store-as-metadata-or-on-filesystem]]
3. Custom Subtitle folder: 
 * See [[Store as metadata or on filesystem|Store-as-metadata-or-on-filesystem]]
4. Treat [IETF language tags](https://en.wikipedia.org/wiki/IETF_language_tag) as ISO 639-1: 
 * Treats subtitle files with IETF language identifiers, such as pt-BR, as their ISO 639-1 counterpart. Thus "pt-BR" will be shown as "Portuguese" instead of "Unknown"

* Fall back to metadata storage if filesystem storage failed

<a name="scheduler"></a>

## Scheduler configuration
![Conf-5](https://github.com/pannal/Sub-Zero.bundle/blob/master/Wiki/Images/Conf-5.png)

1. Ignore folders (...): 
 * If a folder contains one of the files named `subzero.ignore`, `.subzero.ignore`, `.nosz`, don't process them. This applies to sections/libraries, movies, series, seasons, episodes
2. Ignore anything in the following paths (comma-separated)
3. Call this executable upon successful subtitle download:
  * Executes a given executable with an optional amount of variables filled by SZ:
    `%(subtitle_language)s %(subtitle_path)s %(subtitle_filename)s %(provider)s %(score)s %(storage)s %(series_id)s %(series)s %(title)s %(section)s %(filename)s %(path)s %(folder)s %(season_id)s %(type)s %(id)s %(season)s`
4. Scheduler:
Periodically search for recent items with missing subtitles: 
 * self-explanatory, executes the task "Search for missing subtitles" from the channel menu regularly. Configure how often it should do that. For the average library 6 hours minimum is recommended, to not hammer the providers too heavily, since this could cause you to be banned for a period of time
5. Item age to be considered recent: 
 * The "Search for missing subtitles"-task only considers those items in the recently-added list, that are at most this old
6. Recent items to consider per library:
 * How many items to consider for every section/library you have - used in "Search for missing subtitles"-task and Items with missing subtitles"-menu. Change at your own risk!



<a name="develop"></a>

## Advanced configuration
![Conf-6](https://github.com/pannal/Sub-Zero.bundle/blob/master/Wiki/Images/Conf-6.png)

1. Amount of data to store for the history
2. Check for correct folder permissions of every library on plugin start: 
 * if enabled, SZ checks for write permissions of your library folders and warns about them in the plugin channel
3. How verbose should the logging be?: 
 * Controls how much info SZ writes into the log files (default: only warnings) - this is decoupled from your PMS logging settings and determines how verbose Sub-Zero logs information
4. Log to console (for development/debugging): 
 * You know when you need it
5. Help the developers collecting anonymous usage statistics
 * Helps in planning new features

[[Next page|User-Guide]]

[[Back to main page|Home]]

[Go to top](#top)