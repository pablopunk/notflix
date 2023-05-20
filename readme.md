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

-  **Plex**: A media server that allows you to stream your media files to various devices.
-  **Sonarr**: It can monitor multiple RSS feeds for new episodes of TV shows and will grab, sort and rename them.
-  **Radarr**: It can monitor multiple RSS feeds for new movies and will grab, sort and rename them.
-  **Overseerr**: It allows users to request new content and tracks the status of those requests.
-  **Jackett**: A proxy server that allows you to access various torrent trackers without having to sign up for each one individually.
-  **Transmission**: A BitTorrent client that allows you to download and upload files over the BitTorrent protocol.
-  **TimeMachine**: A network backup system that allows you to back up your data from a Mac computer to a networked storage device.
-  **Portainer**: A web-based GUI for managing Docker containers and images.
-  **Watchtower**: A container that automatically updates other containers to their latest versions.

![diagram](./diagram.png)
