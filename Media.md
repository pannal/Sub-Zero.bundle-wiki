When selecting a media, while like browsing a library from Sub-Zero, you are presented with the following menu:

![Media](https://github.com/pannal/Sub-Zero.bundle/blob/master/Wiki/Images/Item_1.png) 

1. Back to home
 * returns you to the home menu of Sub-Zero
2. Refresh <Media title>
 * Refresh media info, and if new/changed subtitles are present, the info will be updated
3. Auto-search: <Media title>
 * This will issue a Plex Media Server "Forced Refresh"
   - All metadata except locked items will be refreshed
   - All current subtitles will be discarded from agent downloads, and new ones will be fetched/downloaded
   - Locally stored subs (Next to the media) will not be touched
4. List <Language> subtitles
   - All enabled providers will be searched for availible subtitles, and shown in an ordered list, with the best match on the top
    - you will have to refresh in order to see progress in the fetching of this info
   - After list is populated, you can select one, and it will be downloaded
5. Add this media to the "ignore list", so Sub-Zero will skip this in the future