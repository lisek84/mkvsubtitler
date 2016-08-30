# mkvsubtitler
Tool to automatically merge subtitles to mkv container on Synology NAS


# USAGE :

Just copy your mkv files to Subtitler folder and run script, or wait until cron does this.

It will look for txt or srt files with the same base name as mkv file. If the file if found, it will be checked for character set, and converted to UTF-8. Then It will be merged (as another stream, not burned on picture) into this mkv file.
After that, prepared mkv movie will be transfered to synology basic video setting and registered for media server.
Now You can Use your TV DLNA player to play this movie, and choose subtitles for this title.

If File will not be found, it will trigger script for napiprojekt.pl to download subtitles if they are available there.
Everything Will be written to Log.txt file in Subtitler directory.

It's really fast even on slow NAS systems.
It's prepared for DS212j - so it's for Marvell CPU's, but it should work for any other propely bootstraped Synology machine, or even for QNAP or Any other Linux based machine after some small modifications.

# INSTALL:
on Synology:
Download files, run install_synology.sh. That's pretty all.
On other systems read the same file for what is needed and install proper tools with other way (apt-get etc)
After all. Add mkv_subtitler_crontab script to Synology Scheduler (crontab :P ) 

See README.txt for more information inside

# Copyrights:
Portions from:
https://github.com/dagon666/napi



