# docker armhf syncthing

This is a Dockerfile to run syncthing on a an arm based server.
This has been tested on https://www.scaleway.com .

## Instructions

```
docker run -d \
    --name syncthing \
    --restart always \
    -p 8384:8384 -p 22000:22000 -p 21025:21025/udp \
    -v <your_syncthing_config_location>:/home/syncthing/.config/syncthing \
    -v <your_data_location>:/home/syncthing/Sync \
    adrienbrault/armhf-syncthing
```

