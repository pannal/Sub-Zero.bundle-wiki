# Information
Sub-Zero detects certain media properties of your media files (especially their file names) and compares them to the same properties derived from a potential subtitle.

Every significant property has a particular score assigned. When evaluating which subtitle to download Sub-Zero sums the scores for each matching property and takes the one with the highest.


# Properties (TV Series)

### hash (Score: 137)
The specific hash of your local file matches against the hash given by the subtitle provider for the file(s) it matches perfectly for. This is error-prone as people tend to add wrong hashes for wrong subtitles on OpenSubtitles especially. That's why Sub-Zero sanity-checks the hashes and only applies the score if certain other parameters match correctly (`series`, `season`, `episode`, `format`).


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


# Properties (Movies)

### hash (Score: 62)
See [TV hash property](#hash-score-137). The only difference is the sanity check, which relies on matching `video_codec` and `format`.

### imdb_id (Score: 62)
See [TV hash property](#imdb_id-score-110).

### title (Score: 23)
The movie title matches.

### year (Score: 12)
A year info is given and it matches the subtitle.

### release_group (Score: 11)
See [TV hash property](#release_group-score-11).

### format (Score: 6)
See [TV hash property](#format-score-6).

### video_codec (Score: 4)
See [TV hash property](#video_codec-score-4).

### resolution (Score: 4)
See [TV hash property](#resolution-score-4).

### audio_codec (Score: 2)
See [TV hash property](#audio_codec-score-2).

### hearing_impaired (Score: 1)
See [TV hash property](#hearing_impaired-score-1).


# Defaults

## TV
### Minimum: 77 and above
`series` 44 + `season` 22 + `episode` 11 = 77

### Sane: 110 and above (default)
`series` 44 + `season` 22 + `episode` 11 + `title` 22 + `release_group` 11 = 110

### Exact: 137 (few to none early matches)
verified `hash` = 137 or<br>
`resolution` 4 + `format` 6 + `video_codec` 4 + `audio_codec` 2 + `series` 44 + `season` 11 + `episode` 11 + `year` 44 + `release_group` 11 = 137


## Movies
### Minimum: 23 and above (default)
`title` 23 = 23

### Sane: 33 and above
`title` 23 + `format` 6 + `video_codec` 4 = 33 or <br>
`title` 23 + `release_group` 11 = 34

### Exact: 62 (few to none early matches)
verified `hash` 62 = 62 or<br>
`resolution` 4 + `format` 6 + `video_codec` 4 + `audio_codec` 2 + `title` 23 + `year` 12 + `release_group` 11 = 62


[[Next page|User-Guide]]

[[Back to main page|Home]]

[Go to top](#top)