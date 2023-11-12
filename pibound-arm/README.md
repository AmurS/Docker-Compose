# PiHole + Unbound for ARM Servers


Ubound Statistics
```
docker exec unbound-arm unbound-control stats_noreset
```

PiHole Statistics
```
docker exec pihole-arm sh -c "echo '>stats >quit' | nc localhost 4711"
```