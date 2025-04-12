# qtorrent

See https://discourse.linuxserver.io/t/opening-qbittorrent-webui-via-dashboard-app-is-unauthorized-mismatched-ips/7363/7

Make sure the docker container has been shutdown before editing qBittorrent.conf. This is because the conf file is written to on shutdown, so any changes made whilst it's still running will be lost otherwise.

```
WebUI\HostHeaderValidation=false
WebUI\CSRFProtection=false
```