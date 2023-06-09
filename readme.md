# Media Server

> Educational purposes only.

This project allows users to stream their own media files and includes
additional features such as automated downloading of TV shows
and movies, a BitTorrent client, and a GUI for managing Docker
containers and images.

## Installation

Before installing the project, ensure that you have the following dependencies installed:

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

To install the project, follow these steps:

1. Clone the repository to your local machine.

``` bash
git clone https://github.com/pablopun/server && cd server
```

2. Copy the example `.env` file and modify it to fit your needs:

``` bash
cp .env.example .env
```

3. Build and run all the images:

``` bash
docker-compose up -d
```

> **Note**
> If you don't want to use a particular service, such as Time Machine, simply remove it from the `docker-compose.yml` file.


## Usage

Once the project is installed and running, you can access the following services at the specified ports:

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

- **Plex**: Like Netflix for your own media files.
- **Overseerr**: Allows users to request new shows/movies to be
    downloaded.
- **Sonarr**: Monitors multiple RSS feeds for new episodes of TV shows
    and will grab, sort and rename them.
- **Radarr**: Monitors multiple RSS feeds for new movies and will
    grab, sort and rename them.
- **Jackett**: To find torrent trackers.
- **Transmission**: BitTorrent client.
- **Cloudflare Tunnel**: Cloudflare's proxy to securely access your
    services over HTTPS.
- **Time Machine**: Wireless backups for your Mac.
- **Portainer**: GUI for managing Docker containers and images.

![diagram](./diagram.png)

## Troubleshooting

If you encounter any issues while installing or using the media server, try the following solutions:

-   Check that all dependencies are installed correctly.
-   Ensure that the `.env` file is configured correctly.
-   Check the logs of the Docker containers (in portainer, port 9000) for any error messages.

## License

MIT License

