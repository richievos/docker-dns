# Description
This image starts a *bind9* server. Its configuration is read from a data 
container.

# Use
Create the data container, as explained here: 
https://github.com/PascalBod/docker-dns-data

This data container is named `dnsserverdata`.

Get the image: 
```
docker pull pascalbod/dns:20141223
```

Run it:
```
docker run --name dnsserver --volumes-from dsnserverdata -d \
    -p 53:53/udp -p 53:53 pascalbod/dns:20141223
```