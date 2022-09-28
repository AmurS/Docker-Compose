# Seafile

Open seafile container terminal.

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


Restart container.

```
docker-compose restart
```

### OAuth2 Authentik

Edit ```/opt/seafile/conf/seahub_settings.py```


```
ENABLE_OAUTH = True
OAUTH_ENABLE_INSECURE_TRANSPORT = True

OAUTH_CLIENT_ID = "Authentik-clientid"
OAUTH_CLIENT_SECRET = "Authentik-clientsekrit"
OAUTH_REDIRECT_URL = 'http://sea.domain.id/oauth/callback/'

# The following shoud NOT be changed if you are using Google as OAuth provider.
OAUTH_PROVIDER_DOMAIN = 'domain.id'
OAUTH_AUTHORIZATION_URL = 'https://auth.domain.id/application/o/authorize/'
OAUTH_TOKEN_URL = 'https://auth.domain.id/application/o/token/'
OAUTH_USER_INFO_URL = 'https://auth.domain.id/application/o/userinfo/'
OAUTH_SCOPE = [
  "openid",
  "profile",
  "email",
]
OAUTH_ATTRIBUTE_MAP = {
    "preferred_username": (False, "email"), 
    "name": (False, "name"),
    "id": (False, "not used"),
    "email": (True, "email"),
}
```