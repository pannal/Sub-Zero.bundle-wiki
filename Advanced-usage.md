# Advanced Usage
Here you'll find information about adv. usage, and please only use the info below, if you know what you are doing

## Remote access to the channel

The features available in the channel menu are in fact accessible and usable from the outside, just as any other channel with routes. This means, that if you're not happy with the scheduler's interval for example, you can take the following URL: http://plex_ip:32400/video/subzero/missing/refresh?X-Plex-Token=XXXXXXXXXXXXXXX (the X-Plex-Token part may not be needed outside of a Plex Home) and open the URL using your favourite command line tool or script (curl, wget, ...). This will trigger the same background task which would be started by the scheduler or by clicking the item in the channel menu.

You can find all available routes by querying http://plex_ip:32400/video/subzero (look for the key="" entries).

To lookup your personal token, take a peak [here](https://support.plex.tv/hc/en-us/articles/204059436)

[[Back to main page|Home]]
