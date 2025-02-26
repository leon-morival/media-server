# Docker VPN Stack avec Gluetun, qBittorrent, Jackett, Sonarr, Radarr et Prowlarr

Ce projet configure un **VPN avec NordVPN** via **Gluetun** pour sécuriser vos containers Docker qui gèrent vos téléchargements et médias, notamment avec **qBittorrent**, **Jackett**, **Sonarr**, **Radarr**, et **Prowlarr**. Ce `docker-compose.yml` crée une stack qui permet de gérer automatiquement les séries, films, et téléchargements.

## Prérequis

Avant de démarrer ce projet, assurez-vous de :

- Avoir un abonnement NordVPN (l'abonnement standard suffit).
- Avoir Docker et Docker Compose installés sur votre serveur.

## Configuration

1. **Clonez ce repository** (ou téléchargez le fichier `docker-compose.yml` et `README.md`).
2. **Obtenez votre clé privée WireGuard** suivie la documentation [ici](https://gist.github.com/bluewalk/7b3db071c488c82c604baf76a42eaad3)

## Étapes d'installation

### 1. Créer les répertoires nécessaires

Assurez-vous que les répertoires suivants existent sur votre serveur :

```bash
sudo mkdir -p /home/leon/docker/gluetun
sudo mkdir -p /home/leon/docker/qbittorrent
sudo mkdir -p /home/leon/docker/qbittorrent/downloads
sudo mkdir -p /home/leon/docker/jackett/data
sudo mkdir -p /home/leon/docker/jackett/blackhole
sudo mkdir -p /home/leon/docker/sonarr/data
sudo mkdir -p /home/leon/docker/sonarr/tvseries
sudo mkdir -p /home/leon/docker/sonarr/downloadclient-downloads
sudo mkdir -p /home/leon/docker/prowlarr/data
sudo mkdir -p /home/leon/docker/radarr/data
sudo mkdir -p /home/leon/docker/radarr/movies
sudo mkdir -p /home/leon/docker/radarr/downloadclient-downloads
```

### 2. Lancer l'installation

```bash
cd /home/leon/docker
sudo docker-compose up -d

```
