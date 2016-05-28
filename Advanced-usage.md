# Advanced Usage
Here you'll find information about adv. usage, and please only use the info below, if you know what you are doing

## Remote access to the channel

The features available in the channel menu are in fact accessible and usable from the outside, just as any other channel with routes. This means, that if you're not happy with the scheduler's interval for example, you can take the following URL: http://plex_ip:32400/video/subzero/missing/refresh?[X-Plex-Token=XXXXXXXXXXXXXXX](https://support.plex.tv/hc/en-us/articles/204059436) (the X-Plex-Token part may not be needed outside of a Plex Home) and open the URL using your favourite command line tool or script (curl, wget, ...). This will trigger the same background task which would be started by the scheduler or by clicking the item in the channel menu.

You can find all available routes by querying http://plex_ip:32400/video/subzero (look for the key="" entries).

To lookup your personal token, take a peak [here](https://support.plex.tv/hc/en-us/articles/204059436)

## Adv. Channel menu

In the Advanced channel menu, you'll see the following:

![Advanced_1](https://github.com/pannal/Sub-Zero.bundle/blob/master/Wiki/Images/Advanced_1.png)

1. Restart the plugin
 * This will restart Sub-Zero, and read the configuration
2. This will make a log entry of the selected setting.
 * Used if debugging, or if asked so by a developer
3. This will reset a saved setting to it's default
 * Used if debugging, or if asked so by a developer

[[Next page|Developers-Corner]]

[[Back to main page|Home]]
