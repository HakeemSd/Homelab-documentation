# Jellyfin

## Purpose

Jellyfin is a self-hosted media server used to organize and stream movies, TV shows, and other video files across devices on the local network.

---

## Prerequisites

- Ubuntu Desktop 24.04 LTS
- Docker Engine
- Docker Compose
- Portainer
- Media folders for movies and TV shows

---

## Folder Structure

The Jellyfin media folders on the Ubuntu server are:

```text
/home/ahmad-saeed/media/
├── movies/
└── tv/
```

Inside the Jellyfin container, these folders are available as:

```text
/media/movies
/media/tv
```

---

## Installation

### Create the Jellyfin directories

```bash
mkdir -p ~/docker/jellyfin
mkdir -p ~/media/movies
mkdir -p ~/media/tv
cd ~/docker/jellyfin
```

### Create the Docker Compose file

Create:

```text
docker-compose.yml
```

Then add the Jellyfin Compose configuration from:

```text
docker/jellyfin/docker-compose.yml
```

### Start Jellyfin

```bash
docker compose up -d
```

### Verify the container

```bash
docker compose ps
```

or:

```bash
docker ps
```

---

## Access Jellyfin

Open a browser on the local network and navigate to:

```text
http://<SERVER-IP>:8096
```

---

## Initial Config

During the Jellyfin setup wizard:

1. Create the administrator account.
2. Add a Movies library using:

```text
/media/movies
```

3. Add a TV Shows library using:

```text
/media/tv
```

4. Complete the setup wizard.
5. Scan all libraries after adding media.

---

## Current Status

- [x] Jellyfin installed
- [x] Running in Docker
- [x] Administrator account created
- [x] Web dashboard accessible
- [x] Movies directory created
- [x] TV directory created
- [ ] Test media added
- [ ] Remote access configured
- [ ] Backup strategy configured

---

## What I Learned

- How to deploy an application with Docker Compose
- How Docker bind mounts connect host folders to containers
- How port mapping exposes a container service to the local network
- How Jellyfin organizes movies and TV shows into libraries
- How to access a self-hosted application through a browser

---

## Screenshot

![Jellyfin Dashboard](../screenshots/jellyfin-dashboard.png)

---

## Future Improvements

- Add movie and TV libraries
- Configure Tailscale for secure remote access
- Configure subtitle support
- Test playback on phones, computers, and TVs
- Add external storage for a larger media library
- Configure automated backups
- Evaluate hardware acceleration support