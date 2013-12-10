FreeFactory
===========

A control script and modules that utilize the a/v transcoding functions of both FFmpeg and FFmbc to hopefully simplify video and audio transcoding for both Professionals and Enthusiast alike.

This functuions by setting up shared and watched directories that have specific scripts assigned to those folders. Inotify is used to watch these directories (for now, /video/dropbox/directorynames). When an audio or a/v file is copied into one of the watched directories, the ff-ctrl.sh script recieves a notification from inotify, and lauches the correct factory module with FFmpeg or FFmbc paramaters to convert it to that particular output.

This is a fully functioning project. It is certainly not the best BASH programming, but it does work. What will be here will be a partial rewrite of what I have already done, since many of my already existing factory modules have passwords embedded in them. I will be rewriting those to be more generic in nature, unless the passwords end up be the default for a specific manufacturer. ie, For the Ross Blackstorm Server, it will be the un/pw of blackstorm/blackstorm. If it is an Adtec server, it will be preset to adtec/none.

Inotify starts the FreeFactory with a pipe to the ff-ctrl.sh control program. I am presently starting this via rc.local, but would think making it a service would be a lot wiser.

The installer script will create a directory in /opt called FreeFactory, From there, it will create FreeFactory/ffmpeg_sources, FreeFactory/ffmodules, FreeFactory/bin and perhaps a few others.

This project is in its infancy bigtime!

TODO:
- Create a PHP and/or TK GUI for graphical based factory module script construction.
- Run under a user, and not root, which is presently the case.
- Determine the best way to set up the /video/dropbox. My /video is actually a mount point for a 2TB RAID, but this will    vary widely with users.
- Clean up the damn code!
- Rewite in something better than BASH. Perhaps even database all the modules using either MySQL and/or PostgreSQL.
- Installer script will be finished soon. It builds both FFMPEG and FFMBC within the /opt/FreeFactory directory as        non-free, and contains it all there, to not interfer with your installed versions.

I would love to get some help with this from people much more knowlegable than me.  My BASH writing is terrible, I am the first to admit it. If you, or you know somebody that may wish to contribute to this project, please notify me and I will allow access.

I am presently running this on a dedicated eight core AMD 64bit ASUS system, with 8gb RAM which was custom built excluively for this project....rack mounted and headless. It is a fully dedicated system. It literally blows away our Telestream transcoder, which is also busy, but this machine is pretty killer! Oh, it also records news teases with a Blackmagic Duo card while transcoding video, without even a glitch! :)





