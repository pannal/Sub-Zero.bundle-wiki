* Sub-Zero is not visible among the channels
  * Most likely, channel mode has been disabled. See [Configuration/Basic item 1](https://github.com/pannal/Sub-Zero.bundle/wiki/Sub%E2%80%90Zero-Configuration#basic-configuration)
* I'm running the plugin for the first time and want to have subtitles for all of my old items
  * [In your Plex library press the little cog, "Refresh all", it should trigger SZ](https://forums.plex.tv/discussion/comment/1230216/#Comment_1230216)
* Sub-Zero complains about permissions
  * your library folders should be writable by the user your Plex server runs as
    * to make your PMS user own your example library folder `/path/to/library`, run ```chown -R `ps aux |grep -m1 com.plexapp.system |cut -f1 -d " " /path/to/library` ``` - while your PMS is running, on your own risk
* After I install Sub-Zero it finds some but not all subtitles for my media
  * [Maybe it won't, on the first try](https://github.com/pannal/Sub-Zero.bundle/wiki/User-Guide#attention-on-the-initial-refresh)
* Sub-Zero doesn't find any or wrong subtitles for my media
  * [Although SZ tries to be smart, folder/file-naming may be your issue](https://forums.plex.tv/discussion/comment/1234850/#Comment_1234850)
* Where are the logs
  * See [Support](https://github.com/pannal/Sub-Zero.bundle/wiki/Support#support)




[[Back to main page|Home]]