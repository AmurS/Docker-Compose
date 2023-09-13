# Cloudflare Zero Trust Tunnel
### Config
```
    environment:
      - TUNNEL_TOKEN= insert super sekrit cloudflare tunnel token here
```


### Other Container
To use this tunnel on other container, use the cloudflared network.
```
services:
  container-example:
    networks:
      - cloudflared
networks:
  cloudflared:
    external: true
```