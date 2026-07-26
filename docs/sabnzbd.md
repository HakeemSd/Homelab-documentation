# SABnzbd

## Overview

SABnzbd is the download client used by the homelab media stack.

It receives download requests from Sonarr and Radarr, downloads media from the configured Usenet provider, and stores completed downloads for automatic import into the media library.

---

## Purpose

- Automated Usenet downloads
- Integration with Sonarr and Radarr
- Automatic download queue management
- Automatic repair and extraction
- Completed download handling

---

## Connected Services

- Sonarr
- Radarr
- Prowlarr
- Jellyfin

---

## Container

Image:

```
lscr.io/linuxserver/sabnzbd:latest
```

---

## Ports

| Port | Purpose |
|-------|----------|
| 8082 | Web Interface |

---

## Volumes

| Host | Container |
|-------|-----------|
| ./config | /config |
| /home/ahmad-saeed/media/downloads | /downloads |
| /home/ahmad-saeed/media | /media |

---

## What I Learned

While deploying SABnzbd I learned:

- Configuring Docker volume mappings
- Integrating a download client with Sonarr and Radarr
- Managing completed download directories
- Troubleshooting container networking
- Understanding how an automated media pipeline works