these are my personal docker composes.

and i dont use .env system.

if you use remember to update files acordingly. 


al my composes following this format 

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
