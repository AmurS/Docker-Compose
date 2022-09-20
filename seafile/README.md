# Seafile

Buka bash container seafile.

```
docker exec -it seafile bash
```

edit ```/opt/seafile/conf/ccnet.conf```

```[General]
SERVICE_URL = https://sea.domain.id
```

edit ```/opt/seafile/conf/seahub_settings.py```

```
FILE_SERVER_ROOT = "https://sea.domain.id/seafhttp"
```


Restart container

```
docker-compose restart
```
