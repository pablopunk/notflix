# Notflix. Your media server

> Educational purposes only.

This project allows users to stream their own media files and includes
  additional features such as automated downloading of TV shows
  and movies, and a BitTorrent client.

## Installation

Before installing the project, ensure that you have the following dependencies installed:

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

To install the project, follow these steps:

1. Clone the repository to your local machine.

``` bash
git clone https://github.com/pablopunk/notflix && cd notflix
```

2. Copy the example `.env` file and modify it to fit your needs:

``` bash
cp .env.example .env
```

3. Build and run all the images:

``` bash
docker-compose up -d
```


## Usage

Once the project is installed and running, you can access the following services at the specified ports:

| Service          | Port   |
|------------------|--------|
| Jellyfin         | 8096   |
| Overseerr        | 5055   |
| Sonarr           | 8989   |
| Radarr           | 7878   |
| Bazarr           | 6767   |
| Jackett          | 9117   |
| Transmission     | 9091   |

To link containers, e.g. **Overseerr+Sonarr**, in the Overseerr configuration you can
specify the **container name** instead of the host IP: `http://sonarr:8989`.

- **Jellyfin**: Like Netflix for your own media files.
- **Overseerr**: Allows users to request new shows/movies to be
    downloaded.
- **Sonarr**: Monitors multiple RSS feeds for new episodes of TV shows
    and will grab, sort and rename them.
- **Radarr**: Monitors multiple RSS feeds for new movies and will
    grab, sort and rename them.
- **Bazarr**: Automatically download subtitles in your desired languages.
- **Jackett**: To find torrent trackers.
- **Transmission**: BitTorrent client.

<!-- ![diagram](./diagram.png) -->

## Troubleshooting

If you encounter any issues while installing or using the media server, try the following solutions:

- Check that all dependencies are installed correctly.
- Ensure that the `.env` file is configured correctly.
- Check the logs of the Docker containers (in portainer, port 9000) for any error messages.

## License

MIT License

