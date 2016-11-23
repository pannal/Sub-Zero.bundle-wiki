# Preword
When you are reading this page, we assume, that you already [[installed|Installation]] and [[configured|Configuration]] Sub-Zero, and if not, then please do that first.

# Recommended steps
Create an account and provide your credentials (in the plugin configuration) for:
* Addic7ed
* Opensubtitles

# Attention on the initial refresh
When you first use this plugin and run a refresh on all of your media, you may be blacklisted out of excessive usage by some or all of the subtitle providers depending on your library's size. This will result in a bunch of errors in the log files as well as missing subtitles.

Just be patient, after a day most of those providers will allow you to access them again and you can refresh the remaining items. If you use the default settings, this will also skip the items it has already downloaded all the wanted languages for. Also, as subtitles will be missing, the scheduler should pick up the items with missing subtitles automatically.

# Channel Menu

Since 1.3.0 Sub-Zero not only comes as an agent plugin, but also has channel properties. By accessing the Sub-Zero channel you can get viable information about the scheduler state, search for missing subtitles, trigger forced-searches for individual items, and many more features yet to come.

To access the channel menu, start by selecting the Channel menu, followed by clicking on the image for Sub-Zero, and **not** the gear icon.

![Channels](https://github.com/pannal/Sub-Zero.bundle/blob/master/Wiki/Images/Select_Channels.png) ![Channel1](https://github.com/pannal/Sub-Zero.bundle/blob/master/Wiki/Images/Channel_1.png)

The Channel menu will then show, and we'll go through that in a few steps:

![Channel1](https://github.com/pannal/Sub-Zero.bundle/blob/master/Wiki/Images/Channel_1_1.png)

![Settings](https://github.com/pannal/Sub-Zero.bundle/blob/master/Wiki/Images/Channel_2.png)

1. On Deck Items
 * Here you see the medias that are On Deck (returned by the Plex API), allowing you to:
    - Refresh the item, in order to maybe pick up a missing subtitle
    - Force Refresh, Ignoring all subs, and go hunt for them again
    - Add the media to the internal [Ignore list](#ignore), meaning that Sub-Zero will not process that media again
2. Items with missing subtitles
 * Here you search for items considered recent (See the [[Sub‐Zero Configuration|Sub‐Zero-Configuration]] menu)
   - you can then select the individual medias, and select between the medias as on above
3. Browse all items
 * here you start by selecting a library, and then a media based on the alphabet list.
   - after that, menu is as [this](https://github.com/pannal/Sub-Zero.bundle/wiki/Media)
4. Search for missing subtitles
 * runs the search-for-missing-subtitles task manually. This normally runs periodically as configured via [scheduler configuration](https://github.com/pannal/Sub-Zero.bundle/wiki/Sub%E2%80%90Zero-Configuration#scheduler-configuration). 

![Settings](https://github.com/pannal/Sub-Zero.bundle/blob/master/Wiki/Images/Channel_3.png)

1. Display [Ignore list](#ignore)
  * List all items in the [Ignore list](#ignore), and allowing you to remove an item, if needed
2. Display History of latest downloaded subtitles
3. Refresh
  * This will refresh the status of the Channel menu
4. Advanced functions
  * See [[Advanced usage|Advanced-usage]]

<a name="ignore"></a>

#Ignore list
There are numerous occasions where one wouldn't want a certain item or even a library be included in the periodic "Search for missing subtitles"-task or the "Items with missing subtitles" menu function. Anime libraries are a good example of that, or home videos. Perhaps you've got your favourite series in your native language and don't want subtitles for it.

The ignore list can be managed by going through your library using the "Browse all items" menu and the "Display ignore list" menu.

# Scheduler

The built-in scheduler is capable of running a number of tasks periodically in a separate Thread of the plugin. This currently is used to automatically periodically search for new subtitles for your media items. See [[Sub‐Zero Configuration|Sub‐Zero-Configuration#wiki-scheduler]]

# Physically Ignoring Media

Sometimes subtitles aren't needed or wanted for parts of your library.

When a file named `subzero.ignore`, `.subzero.ignore`, or `.nosz` is found by the plugin in any of your library's folders, be it the section itself, a TV show, a movie, or even a season, Sub-Zero will skip processing the contents of that folder on a scheduled run.

BETA notes: This may still mean that the scheduler task for missing subtitles triggers refresh actions on those items, but the refresh handler itself will skip those.

[[Next page|Advanced-usage]]

[[Back to main page|Home]]