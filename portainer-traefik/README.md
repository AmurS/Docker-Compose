# Portainer with Traefik

### Portainer edge agent with Traefik
When using Portainer edge agent with trafeik we can't use it directly.
First you need to decode the  `EDGE_KEY` in order to obtain the endpoint and fingerprint. We can use https://www.base64decode.org/ to decode and encode.

```
https://edge.mydomain.com|edge.mydomain.com:8000|aa:bb:cc:dd:ee:ff:00:00:00:01:00:00:00:00:00:00|3
```
Change the entery point to our edge domain 
```
https://portainer.mydomain.com|https://edge.mydomain.com|aa:bb:cc:dd:ee:ff:00:00:00:01:00:00:00:00:00:00|3
```
Encode it again with url safe encoding.

Source : [github issue](https://github.com/portainer/portainer-compose/issues/24#issuecomment-942389178)
