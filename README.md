nginx + ngx_pagespeed Cookbook
==============
* Ubuntu 12.04
* nginx 1.4.4
* ngx_pagespeed-1.7.30.2-beta

this cookbook build nginx with the following command
```
  ./configure --prefix=/etc/nginx \
  --conf-path=/etc/nginx/nginx.conf \
  --error-log-path=/var/log/nginx/error.log \
  --http-client-body-temp-path=/var/lib/nginx/body \
  --http-fastcgi-temp-path=/var/lib/nginx/fastcgi \
  --http-log-path=/var/log/nginx/access.log \
  --http-proxy-temp-path=/var/lib/nginx/proxy \
  --http-scgi-temp-path=/var/lib/nginx/scgi \
  --http-uwsgi-temp-path=/var/lib/nginx/uwsgi \
  --lock-path=/var/lock/nginx.lock \
  --pid-path=/var/run/nginx.pid \
  --with-debug \
  --with-http_addition_module \
  --with-http_dav_module \
  --with-http_geoip_module \
  --with-http_gzip_static_module \
  --with-http_image_filter_module \
  --with-http_realip_module \
  --with-http_stub_status_module \
  --with-http_ssl_module \
  --with-http_sub_module \
  --with-http_xslt_module \
  --with-ipv6 \
  --with-sha1=/usr/include/openssl \
  --with-md5=/usr/include/openssl \
  --with-mail \
  --with-mail_ssl_module \
  --add-module=/usr/share/nginx/ngx_pagespeed-1.7.30.2-beta
  make
  make install
```

Usage
-----
#### nginx::default
Just include `nginx` in your node's `run_list`:

```json
{
  "name":"my_node",
  "run_list": [
    "recipe[nginx]"
  ]
}
```
