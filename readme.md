# media server

> Educational purposes only

- [Requirements](#requirements)
- [Features and
    usage](#features-and-usage)
  - [Plex Media
      server](#plex-media-server)
  - [Extras](#extras)

## Requirements

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

Copy the example `.env` and modify it to fit your needs.

``` bash
cp .env.example .env
```

Build and run all the images.

``` bash
docker-compose up -d
```

> **Note**
> If you don't want one of those (e.g. Time Machine, etc), just remove it from `docker-compose.yml`

All services are available through `http://<host>:<port>`.

| Service          | Port   |
|------------------|--------|
| Plex             | 32400  |
| Sonarr           | 8989   |
| Radarr           | 7878   |
| Bazarr           | 6767   |
| Overseerr        | 5055   |
| Jackett          | 9117   |
| Transmission     | 9091   |
| Portainer        | 9000   |


## Features

### Plex Media server

- **Plex**: Like Netflix for your own media files.
- **Overseerr**: Allows users to request new shows/movies to be
    downloaded.
- **Sonarr**: Monitors multiple RSS feeds for new episodes of TV shows
    and will grab, sort and rename them.
- **Radarr**: Monitors multiple RSS feeds for new movies and will
    grab, sort and rename them.
- **Jackett**: To find torrent trackers.
- **Transmission**: BitTorrent client.

![diagram](./diagram.png)

### Extras

- **Cloudflare Tunnel**: Cloudflare's proxy to securely access your
    services over HTTPS.
- **Time Machine**: Wireless backups for your Mac.
- **Portainer**: GUI for managing Docker containers and images.
