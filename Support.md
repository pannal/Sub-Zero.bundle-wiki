# Support

If you have a question about Sub-Zero, please post a question in the [forum support thread](https://forums.plex.tv/discussion/186575)

Also note, that you might be asked to provide logs, and if so, make sure that the [[logging level|Configuration#wiki-develop]] is set to debug.

To locate the log files, look [here](https://support.plex.tv/hc/en-us/articles/200250417) and [below](#logging)

# Bug reporting

If you encountered a bug, then feel free to either post in the support forum, or, and preferred, create an [issue](https://github.com/pannal/Sub-Zero.bundle/issues) here on github, but before doing so, please search the [issue list](https://github.com/pannal/Sub-Zero.bundle/issues?utf8=%E2%9C%93&q=) to make sure, it isn't already reported, or even fixed.

When creating an issue, remember:

* be sure to post your logs with your log_level to DEBUG in Sub-Zero's settings
* <a name="logging"></a>get `Library/Application Support/Plex Media Server/Logs/PMS Plugin Logs/com.plexapp.agents.subzero.log`; there may be multiple logs (`com.plexapp.agents.subzero.log.*`) depending on the amount of Videos you're refreshing

**Remember**: If you're using the [[manual installation|Developers-Corner]], before you open a bug-ticket please double-check, that you've deleted the Sub-Zero.bundle folder **BEFORE** every update (to avoid .pyc leftovers)

[[Next page|License]]

[[Back to main page|Home]]