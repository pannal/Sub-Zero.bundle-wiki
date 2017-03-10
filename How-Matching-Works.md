Simple answer: SZ matches filenames against subtitle info.

A score of a subtitle is determined by the matching components of the media metadata (mostly from the filename) against the available subtitle info (depends on the provider). If your minimum movie score setting in SZ is too high and the info contained in the filename amounts to less than the score, the subtitles found on any provider won't match.

The more meta info a filename has, the better. Omitting a "DVDRip" information for example may result in a downloaded subtitle which was meant for a different framerate.
This is the basis of the score determination for a subtitle of a movie: https://github.com/pannal/Sub-Zero.bundle/blob/master/Contents/Libraries/Shared/subliminal/video.py#L202
This for an episode: https://github.com/pannal/Sub-Zero.bundle/blob/master/Contents/Libraries/Shared/subliminal/video.py#L141

Have a look at the subtitle example for a movie named `The.Movie.2016.1080.BluRay.x264.DTS.mkv` compared to your local  `The.Movie.2016.mkv`. The score for a title match is 23, for year it's 12. If your minimum movie score is more than 35, it won't be able to find any subtitles for this file, regardless of the amount of metadata a subtitle provider provides. (keep in mind that this is a simplified explanation, as subliminal uses "deeper" score computation, detailed here)

The more matching metadata between a filename and a subtitle, the higher the subtitle score, and the higher the likeliness, that a subtitle is "good" for your file.

You can see how matching is done by setting SZ to DEBUG info and studying the log files.

In short: renaming a media file while dropping info about its content (codecs, formats, language, year ...) will lower the quality of subtitles you get, or even stop you from getting any subtitles at all, depending on your minimum score for episodes or movie subtitles. You can rename the files to your liking, though. "Guessit", which is used by SZ for detecting info from the filename, is pretty smart.
SZ has sane defaults for minimum score: 23 for movies (title matches), for example.

[Original Post](https://forums.plex.tv/discussion/comment/1234850/#Comment_1234850)