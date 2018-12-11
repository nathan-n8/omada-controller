Docker image for TP-Link Omada Controller v3.0.5 based off of ubuntu:18.04.

Forked from ehseroffice/omada-controller to add time zone support for Los Angeles

To pull this image: `docker pull nathannathannathan/omada-controller`

Example usage:

```
docker run -d --restart unless-stopped --name omada-controller \
-p 8043:8043/tcp \
-p 8088:8088/tcp \
-p 27001:27001/udp \
-p 27002:27002/tcp \
-p 29810:29810/udp \
-p 29811:29811/tcp \
-p 29812:29812/tcp \
-p 29813:29813/tcp \
-v omada-data:/opt/tplink/EAPController/data \
-v omada-work:/opt/tplink/EAPController/work \
-v omada-logs:/opt/tplink/EAPController/logs \
nathannathannathan/omada-controller
```
