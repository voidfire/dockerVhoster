
cd ..
- Installation

First create the network
```
docker network create nginx-proxy
```

Folder Structure

```
.
+-- nginx-proxy
|   +-- docker-compose.yml
|   +-- nginx.tmpl
|   +-- conf.d
|   +-- vhost.d
|   +-- html
|   +-- certs
+-- site1.gr
|   +-- docker-compose.yml

```

1. Start the proxy server
```
cd ./nginx-proxy/ && docker-compose up -d
```

Proxy Environmental Variables example for container
```
    environment:
    -  VIRTUAL_HOST=site1.gr 
    -  VIRTUAL_PORT=3000
    -  LETSENCRYPT_HOST=site1.gr
    -  LETSENCRYPT_EMAIL=your-email@site1.gr
```