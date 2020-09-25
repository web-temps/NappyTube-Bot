# NappyTube-bot

## About <a name = "about"></a>

NappyTube is a radio bot for Discord servers.\
It runs on Discord.js, and scrapes the Napster API to create playlists, then persists them to a sqlite database.\
It takes each track from the database, uses GAPI to search Youtube for the artist/song/album name and creates a list of urls to play from. It then adds the list to the column in the database related to that track.\
It then streams a track using ytdl-core. It finds a track from the database, grabs the first url from the list, and streams from that url.\
If the stream throws an error (such as the content was not available in this country error, or requires YT-premium) it will automatically "debug the track" by choosing the next url from the list, and from then on will stream from that url.

It is hosted on an AWS EC2 instance. Please contact me for a demo, since it is not running 24/7.