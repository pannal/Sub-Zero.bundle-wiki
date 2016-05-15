# Store as metadata or on filesystem

By default, Plex stores posters, fan art and subtitles as metadata in a separate folder which is not managed by the user. In Sub-Zero, though, 'Store subtitles next to media files' is enabled by default. The agent will write the subtitle files in the media folder next to the media file itself. The setting 'Subtitle folder' configures in which folder (current folder or other subfolder) the subtitles are stored. The expert user can also supply 'Custom Subtitle folder' which can also be an absolute path.

When a subfolder (either custom or predefined) is used, the automatic scheduled refresh of Plex won't pick up your subtitles, **only** a manual refresh will!
When a Sub-Zero-scheduled-refresh takes place, the external subtitles will be picked up, though.

[[Back to main page|Home]]