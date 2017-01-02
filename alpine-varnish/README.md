# Varnish in Alpine
Installs Varnish from the main APK repository, currently the version is 4.1.3.

This image requires the existence of `/etc/varnish/default.vcl`, so you need to
volume-mount that in from somewhere.

Example:
```bash
docker run -d -v `pwd`/default.vcl:/etc/varnish/default.vcl ruudud/varnish
```
