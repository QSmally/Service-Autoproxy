
# Service autoproxy

Automatic reverse proxy with LetsEncrypt support.

The repository is derived from a [a Docker + Nginx + LetsEncrypt example](https://github.com/fatk/docker-letsencrypt-nginx-proxy-companion-examples)
with my own adjustments and fixes as per their MIT license. It's flexible enough to interface with
any exposed service, so not just an Nginx file server, depending on the configuration of
`docker-compose.yml`.

## Architecture

* Nginx reverse proxy;
* Per-service configuration generation;
* LetsEncrypt certificate generation;
* Services...

## Notes

* `$ docker compose up [--build --remove-orphans]`: boot up or update the proxy and their services;
* `$ docker exec -it nginx cat /etc/nginx/conf.d/default.conf`: view the generated configuration;
* `$ docker compose logs`: view the logs of all the containers.
