# media server

> Educational purposes only

## Usage

> Requirements: It runs on Docker using [`docker-compose`](https://docs.docker.com/compose/).

First, copy the example `.env` and modify it to fit your needs.

```bash
cp .env.example .env
```

Now run it:

```bash
docker-compose up
```

## Features

-  **Plex**: Like Netflix for your own media files.
-  **Overseerr**: Allows users to request new shows/movies to be downloaded.
-  **Sonarr**: Monitors multiple RSS feeds for new episodes of TV shows and will grab, sort and rename them.
-  **Radarr**: Monitors multiple RSS feeds for new movies and will grab, sort and rename them.
-  **Jackett**: To find torrent trackers.
-  **Transmission**: BitTorrent client.
-  **Time Machine**: Wireless backups for your Mac.
-  **Portainer**: GUI for managing Docker containers and images.
-  **Watchtower**: Automatically updates other containers to their latest versions.

![diagram](./diagram.png)
