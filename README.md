```

version: "3.8"

services:
  service_name:
    hostname: service_name
    image: image_name:latest
    environment:
      - KEY=value
      - ANOTHER_KEY=value
    volumes:
      - /path/to/local:/path/in/container
    networks:
      cloudflared:
        aliases:
          - service_name
    restart: on-failure
    # ports:
    #   - "host_port:container_port"

networks:
  cloudflared:
    external: true

```






.env.example

```

# General Settings
TZ=
USER=
PASSWORD=
PUID=0 # root puid
PGID=0 # root pgid
UPUID= # user puid
UPGID= # user pgid
HOME_DIR=

# Web Config
SEARXNG_BASE_URL= ## url with http/https

# Samba Config
SAMBA_USER=

# WireGuard Config
WG_HOST= # host ip/url
WG_PASSWORD_HASH= # password bcrypt hash with extra  before all $, normal is $2y$10$XT........, you need to use $$2y$$10$$XT........., as per wg-easy doc

# Database Config
MYSQL_ROOT_PASSWORD=
MYSQL_DATABASE=
MYSQL_USER=
MYSQL_PASSWORD=

# WordPress Config
WORDPRESS_DB_USER=
WORDPRESS_DB_PASSWORD=

# Cloudflared Config
CLOUDFLARED_TOKEN=

```



