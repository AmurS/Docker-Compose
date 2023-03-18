# LibreSpeed

Run LibreSpeed in multi server mode with frontend and backend container. Customize the compose file to fit your purpose.

### Frontend Server List
Create servers.json in the working directory before starting the frontend container.
```
[
    {
        "name": "Friendly name for Server 1",
        "server" :"http://server1.mydomain.com/",
        "dlURL" :"garbage.php",
        "ulURL" :"empty.php",
        "pingURL" :"empty.php",
        "getIpURL" :"getIP.php"
    },
    {
        "name": "Friendly name for Server 2",
        "server" :"https://server2.mydomain.com/",
        "dlURL" :"garbage.php",
        "ulURL" :"empty.php",
        "pingURL" :"empty.php",
        "getIpURL" :"getIP.php"
    },
    {
        "name": "Friendly name for Server 3",
        "server" :"//server3.mydomain.com/",
        "dlURL" :"garbage.php",
        "ulURL" :"empty.php",
        "pingURL" :"empty.php",
        "getIpURL" :"getIP.php"
    },    

]
```