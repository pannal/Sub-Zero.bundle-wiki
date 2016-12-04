### Sub-Zero is not visible among the channels
Most likely, channel mode has been disabled. See [Configuration/Basic item 1](https://github.com/pannal/Sub-Zero.bundle/wiki/Sub%E2%80%90Zero-Configuration#basic-configuration)

### I'm running the plugin for the first time and want to have subtitles for all of my old items
[In your Plex library press the little cog, "Refresh all", it should trigger SZ](https://forums.plex.tv/discussion/comment/1230216/#Comment_1230216)

### Sub-Zero complains about permissions
your library folders should be writable by the user your Plex server runs as
  * to make your PMS user own your example library folder `/path/to/library`
  * run ```chown -R `ps aux |grep -m1 com.plexapp.system |cut -f1 -d " " /path/to/library` ```
  * while your PMS is running, on your own risk

### After I install Sub-Zero it finds some but not all subtitles for my media
[Maybe it won't, on the first try](https://github.com/pannal/Sub-Zero.bundle/wiki/User-Guide#attention-on-the-initial-refresh)

### Sub-Zero doesn't find any or wrong subtitles for my media
[Although SZ tries to be smart, folder/file-naming may be your issue](https://forums.plex.tv/discussion/comment/1234850/#Comment_1234850)

### Where are the logs
See [Support](https://github.com/pannal/Sub-Zero.bundle/wiki/Support#support)

### What is the "I keep the exact release title" setting?
It's a special case for OpenSubtitles. They support matching for an exact filename (they call it tag match). When the option is turned on, SZ also tries the exact match (in addition to a hash based match), and if found, scores it the same as an exact hash match.<br><br>
Turning this on should not have a big negative effect if you have some renamed files.<br><br>
But consider this: You've got release name `Blabla.2015.x264-GROUP.mkv` and you rename it to `Blabla.mkv`. SZ searches for that filename on OpenSubtitles and some other dude (there are many of them) have added it as an alternative filename for his/her subtitle - you'll most likely get that subtitle because it's being treated with the highest possible score.
But as the tag match is treated the same as a hash match, the sanity checks are applied as well, which may help enough to not get any wrong subtitles.<br><br>
Due to the nature of OpenSubtitles one can add `Moviename Blabla Subtitle HEHEHE` as a subtitle name and specify multiple movie hashes, and alternative file names (tags), which may match your local file. The feature was added because Sub-Zero can't determine enough info from `Moviename Blabla Subtitle HEHEHE` because the uploader was lazy, but it may find the full filename in the alternative names list.

### DistributionNotFound Error
Your PythonPath may include your system python.<br>
Please [follow this to fix the issue](https://forums.plex.tv/discussion/209304/suggestion-debian-packages-and-pythonpath).

[[Back to main page|Home]]