# media server

> Educational purposes only

## Requirements

* [Docker](https://www.docker.com/)
* [Docker Compose](https://docs.docker.com/compose/)

Copy the example `.env` and modify it to fit your needs.

```bash
cp .env.example .env
```

## Features and usage

### Plex Media server

```bash
docker-compose up -d
```

-  **Plex**: Like Netflix for your own media files.
-  **Overseerr**: Allows users to request new shows/movies to be downloaded.
-  **Sonarr**: Monitors multiple RSS feeds for new episodes of TV shows and will grab, sort and rename them.
-  **Radarr**: Monitors multiple RSS feeds for new movies and will grab, sort and rename them.
-  **Jackett**: To find torrent trackers.
-  **Transmission**: BitTorrent client.

![diagram](./diagram.png)

### Extras

```bash
docker-compose --profile all up -d
```

-  **Cloudflare Tunnel**: Cloudflare's proxy to securely access your services over HTTPS.
-  **Time Machine**: Wireless backups for your Mac.
-  **Portainer**: GUI for managing Docker containers and images.
