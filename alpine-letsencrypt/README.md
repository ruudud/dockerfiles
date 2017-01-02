# Let's encrypt

Installs letsencrypt from the APK community repository.

Example using nginx in other container:

```bash
docker run -it --rm \
        -v /opt/tls-nginx:/etc/letsencrypt \
        -v /opt/static-data/:/opt/www \
        ruudud/alpine-letsencrypt \
        certonly \
        --webroot --webroot-path /opt/www \
         --agree-tos --renew-by-default \
        -d <domain> \
        -m <email>
```
