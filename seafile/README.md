# Seafile

Buka bash container seafile.

docker exec -it seafile bash

edit /opt/seafile/conf/ccnet.conf

[General]
SERVICE_URL = https://sea.korone.my.id


edit /opt/seafile/conf/seahub_settings.py

FILE_SERVER_ROOT = "https://sea.korone.my.id/seafhttp"


docker-compose restart
