# Todo App mit React/MongoDB und FasAPI

Basierend auf einem FARM-STACK-Tutorial.

Allerdings mit einem vollständigen docker-compose-stack.

Für das Frontend hab ich auf das Basis-Image tiangolo/node-frontend:10 zurückgegriffen. Damit das ganze in der docker-Umgebung funktioniert musste der integrierte nginx eine besondere Config-Datei erhalaten, da man ansosten
in die CORS-Problematik gelaufen wäre.

```nginx.configuration
    # the request made to localhost/api are enabled to CORS
    #
    add_header 'Access-Control-Allow-Origin' '*';
```
