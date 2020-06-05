chmod +x docker_script.sh

nano ./ddclient/config/ddclient.conf
cd ddclient && docker-compose up -d

chmod 600 ./traefik/data/acme.json
nano ./traefik/.env
nano ./traefikdata/traefik.yml # correo
cd traefik && docker-compose up -d

nano ./web/.env
cd web && docker-compose up -d
