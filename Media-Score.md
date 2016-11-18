# Information
Sub-Zero detects certain media properties of your media files (especially their file names) and compares them to the same properties derived from a potential subtitle.

Every significant property has a particular score assigned. When evaluating which subtitle to download Sub-Zero sums the scores for each matching property and takes the one with the highest.


# Properties (TV Series)

### hash (Score: 137)
The specific hash of your local file matches against the hash given by the subtitle provider for the file(s) it matches perfectly for. This is error-prone as people tend to add wrong hashes for wrong subtitles on OpenSubtitles especially. That's why Sub-Zero sanity-checks the hashes and only applies the score if certain other parameters match correctly (TV: series, season, episode, format; Movies: video_codec, format).


### imdb_id (Score: 110)
The IMDB ID of the subtitle provider's returned data matches your locally stored IMDB ID.


### tvdb_id (Score: 88)
The TVDB ID of the subtitle provider's returned data matches your locally stored TVDB ID.


### series (Score: 44)
The series title matches.


### year (Score: 44)
The year info of the series matches (either none given or correct one given)


### title (Score: 22)
The _episode_ title given matches.


### season (Score: 11)
The season number matches yours.


### episode (Score: 11)
The episode number matches yours.


### release_group (Score: 11)
The release group for that particular subtitle matches the release group of your media file.


### format (Score: 6)
The format matches (HDTV, BluRay, WEB-DL, WEBRip, DVDRip, ...).


### video_codec (Score: 4)
The video codec matches (x264, XViD, ...).


### resolution (Score: 4)
The resolution matches (720p, 1080p, ...). Probably one of the parameters that can be ignored the most. Hence the low score.


### audio_codec (Score: 2)
The audio codec matches (AAC, MP3, ...). Probably one of the parameters that can be ignored the most. Hence the low score.


### hearing_impaired (Score: 1)
The hearing impaired flag matches your Sub-Zero setting. (E.g. you've got the setting at force-HI and the subtitle is hearing impaired: match)



[[Next page|User-Guide]]

[[Back to main page|Home]]

[Go to top](#top)