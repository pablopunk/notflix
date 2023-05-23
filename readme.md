# media server

> Educational purposes only

## Usage

> Requirements: It runs on Docker using [`docker-compose`](https://docs.docker.com/compose/).

First, copy the example `.env` and modify it to fit your needs.

```bash
cp .env.example .env
```

Now run the apps you want

```bash
docker-compose up -f docker-compose.plex.yml -d # media server
docker-compose up -f docker-compose.hosting.yml -d # nginx with custom server
docker-compose up -f docker-compose.utils.yml -d # other utils
```

## Features

### `plex`: Media server

-  **Plex**: Like Netflix for your own media files.
-  **Overseerr**: Allows users to request new shows/movies to be downloaded.
-  **Sonarr**: Monitors multiple RSS feeds for new episodes of TV shows and will grab, sort and rename them.
-  **Radarr**: Monitors multiple RSS feeds for new movies and will grab, sort and rename them.
-  **Jackett**: To find torrent trackers.
-  **Transmission**: BitTorrent client.

### `hosting`: Use a custom domain

-  **Cloudflare DDNS**: Automatically updates your Cloudflare DNS records to point to your home IP.
-  **Nginx**: Reverse proxy server to securely access your services over HTTPS.
-  **Certbot**: Automatically obtains and renews SSL/TLS certificates from Let's Encrypt.

### `utils`: Additional features

-  **Time Machine**: Wireless backups for your Mac.
-  **Portainer**: GUI for managing Docker containers and images.
-  **Watchtower**: Automatically updates other containers to their latest versions.

![diagram](./diagram.png)
