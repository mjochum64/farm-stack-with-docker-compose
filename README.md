# Todo App mit React/MongoDB und FasAPI

Basierend auf einem FARM-STACK-Tutorial.
https://www.youtube.com/watch?v=OzUzrs8uJl8

Allerdings wollte ich alle Applikationen mittels docker-compose betreiben.

Für das Frontend hab ich auf das Basis-Image "tiangolo/node-frontend:10" zurückgegriffen.

Damit das ganze in der docker-compose Umgebung funktioniert, musste der integrierte "nginx" eine besondere Config-Datei erhalten, da man ansosten eine CORS-Problematik gelaufen wäre (frontend hätte sich nicht mit backend über http unterhalten können).

```nginx.configuration
    # the request made to localhost/api are enabled to CORS
    #
    add_header 'Access-Control-Allow-Origin' '*';
```

# Installation und Betrieb

Ich verwende Windows 11, zusammen mit Ubuntu 22.04 in der WSL-Umgebung.
Für die Docker-Container nutze ich Rancher Desktop 1.6.0 (dockerd moby).

Start erfolgt einfach durch das Kommando

```bash
docker compose up -d
```

Nach dem hoffentlich erfolgreichen Start kann man dann einfach über die URL http://localhost auf die App zugreifen.
