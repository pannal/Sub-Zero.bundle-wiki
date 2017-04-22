# Information
Sub-Zero detects certain media properties of your media files (especially their file names) and compares them to the same properties derived from a potential subtitle.

Every significant property has a particular score assigned. When evaluating which subtitle to download Sub-Zero sums the scores for each matching property and takes the one with the highest.

The minimum score a subtitle has to have for it to be downloaded by Sub-Zero can be set in the preferences dialog. The defaults should fit perfectly for most people, you may wish to customize them to your likings, though. Have a look below, then.

# Properties (TV Series)

### hash (Score: 137 (v2: 359))
The specific hash of your local file matches against the hash given by the subtitle provider for the file(s) it matches perfectly for. This is error-prone as people tend to add wrong hashes for wrong subtitles on OpenSubtitles especially. That's why Sub-Zero sanity-checks the hashes and only applies the score if certain other parameters match correctly (`series`, `season`, `episode`, `format`).


### imdb_id (Score: 110 (v2: n/a))
The IMDB ID of the subtitle provider's returned data matches your locally stored IMDB ID.


### tvdb_id (Score: 88 (v2: n/a))
The TVDB ID of the subtitle provider's returned data matches your locally stored TVDB ID.


### series (Score: 44 (v2: 180))
The series title matches.


### year (Score: 44 (v2: 90))
The year info of the series matches (either none given or correct one given)


### title (Score: 22 (v2: n/a))
The _episode_ title given matches.


### season (Score: 11 (v2: 30))
The season number matches yours.


### episode (Score: 11 (v2: 30))
The episode number matches yours.


### release_group (Score: 11 (v2: 15))
The release group for that particular subtitle matches the release group of your media file.


### format (Score: 6 (v2: 7))
The format matches (HDTV, BluRay, WEB-DL, WEBRip, DVDRip, ...).


### video_codec (Score: 4 (v2: 2))
The video codec matches (x264, XViD, ...).


### resolution (Score: 4 (v2: 2))
The resolution matches (720p, 1080p, ...). Probably one of the parameters that can be ignored the most. Hence the low score.


### audio_codec (Score: 2 (v2: 3))
The audio codec matches (AAC, MP3, ...). Probably one of the parameters that can be ignored the most. Hence the low score.


### hearing_impaired (Score: 1)
The hearing impaired flag matches your Sub-Zero setting. (E.g. you've got the setting at force-HI and the subtitle is hearing impaired: match)


# Properties (Movies)

### hash (Score: 62 (v2: 119))
See [TV hash property](#hash-score-137). The only difference is the sanity check, which relies on matching `video_codec` and `format`.

### imdb_id (Score: 62 (v2: n/a))
See [TV hash property](#imdb_id-score-110).

### title (Score: 23 (v2: 60))
The movie title matches.

### year (Score: 12 (v2: 30))
A year info is given and it matches the subtitle.

### release_group (Score: 11 (v2: 15))
See [TV hash property](#release_group-score-11).

### format (Score: 6 (v2: 7))
See [TV hash property](#format-score-6).

### video_codec (Score: 4 (v2: 2))
See [TV hash property](#video_codec-score-4).

### resolution (Score: 4 (v2: 2))
See [TV hash property](#resolution-score-4).

### audio_codec (Score: 2 (v2: 3))
See [TV hash property](#audio_codec-score-2).

### hearing_impaired (Score: 1)
See [TV hash property](#hearing_impaired-score-1).


# Defaults
* Minimum: Find subtitles no matter what
* Sane: Find subtitles matching your media file
* Ideal: Find subtitles mostly exactly matching your media file (same video format or same release group)
* Exact: Find subtitles exactly matching your media file

## TV
### Minimum: 77 and above (v2: 240)
v1: `series` 44 + `season` 22 + `episode` 11 = 77

v2: `series` 180 + `season` 30 + `episode` 30 = 240

### Sane: 110 and above (v2: 337)
v1: `series` 44 + `season` 22 + `episode` 11 + `title` 22 + `release_group` 11 = 110

v2: `series` 180 + `season` 30 + `episode` 30 + `year` 90 +  `format` 7 = 337

### Ideal: 116 and above (default) (v2: 345)
v1: `series` 44 + `season` 22 + `episode` 11 + `title` 22 + `release_group` 11 + `format` 6 = 116

v2: `series` 180 + `season` 30 + `episode` 30 + `year` 90 +  `release_group` 15 + `format` 7 = 352

### Exact: 137 (few to none early matches) (v2: 359)
verified `hash` = 137 or<br>
`resolution` 4 + `format` 6 + `video_codec` 4 + `audio_codec` 2 + `series` 44 + `season` 11 + `episode` 11 + `year` 44 + `release_group` 11 = 137 (v2: 359)


## Movies
### Minimum: 23 and above (v2: 60)
v1: `title` 23 = 23

v2: `title` 60 = 60

### Sane: 33 and above (default) (v2: 69)
v1: `title` 23 + `format` 6 + `video_codec` 4 = 33

v2: `title` 60 + `format` 7 + `video_codec` 2 = 69

### Ideal: 40 and above (v2: 82)
v1: `title` 23 + `format` 6 + `release_group` 11 = 40

v2: `title` 60 + `format` 7 + `release_group` 15 = 82

### Exact: 62 (few to none early matches) (v2: 119)
verified `hash` 62 = 62 or<br>
`resolution` 4 + `format` 6 + `video_codec` 4 + `audio_codec` 2 + `title` 23 + `year` 12 + `release_group` 11 = 62


# Special scores
### addic7ed_boost (TV)
Can be configured in the preferences dialog. If a subtitle was found for your configured score on Addic7ed and it matches at least `series`, `season`, `episode`, `year`, `format`, the configured value gets added to the subtitle's final score to lift it "above" the other provider's results.

This is often used and has a default value of 10, because in general, when Addic7ed matches a subtitle, it tends to have a very high quality compared to other providers. As Addic7ed doesn't use hashes and doesn't have too much media property info on their site, `addic7ed_boost` helps by prioritizing the provider.

[[Next page|User-Guide]]

[[Back to main page|Home]]

[Go to top](#top)