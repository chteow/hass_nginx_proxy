Workaround for nginx reverse proxy on hass
hass not working with subdomain using below format

         location /ha {
            proxy_pass https://hass_ip:8123;
            proxy_redirect off;
            proxy_http_version 1.1;
            proxy_set_header Upgrade $http_upgrade;
            proxy_set_header Connection "upgrade";
            proxy_read_timeout 3600s;
        }


However, added location in nginx where needed by hass managed to overcome this.
