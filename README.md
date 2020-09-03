# arm32v7-bind9
Image docker bind9 for arm (raspberry)

Swarm mode compatible

```
version: '3'
services:
    
    image: juxo/arm32v7bind9  
    volumes:
      - "./bind/conf/named.conf:/etc/bind/named.conf:ro"
      - "./bind/conf/named.conf.default-zones:/etc/bind/named.conf.default-zones:ro"
      - "./bind/conf/named.conf.local:/etc/bind/named.conf.local:ro"
      - "./bind/conf/named.conf.options:/etc/bind/named.conf.options:ro"
      - "./bind/zones:/etc/bind/pri:rw"
    deploy:
      mode: replicated
      replicas: 1
    ports:
      - "53:53/tcp"
      - "53:53/udp"
      - "63:63/udp"
```

if your need more information : mail !
