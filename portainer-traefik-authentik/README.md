# Portainer + Traefik + Authentik

This is a docker compose file that combine portainer, traefik and authentik. 

### Setup

With a fresh install run the following command to generate secret key for authentik.
```
sudo apt-get install -y pwgen
echo "AUTHENTIK_SECRET_KEY=$(pwgen -s 50 1)" >> .env
```
After that just run docker compose to deploy  the container.

```
docker-compose up -d
```
