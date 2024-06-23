A dockeriezd WebDAV server based on Nginx. Example usage:

```
version: "3.4"
services:
  webdav:
    image: derkades/webdav
    volumes: ['/home/webdav-container:/data']
    ports: ['8418:80']
    environment:
      USERNAME: user
      PASSWORD: acLy_QCw1pynL
      UID: 1000
      GID: 1000
    restart: unless-stopped
```

Always runs as user 1000, hard coded. This makes it compatible with linuxserver.io containers.
