# cloudflare-ddns
version: '2'
services:
  cloudflare-ddns:
    image: oznu/cloudflare-ddns:latest
    restart: always
    environment:
      - API_KEY=${CLOUDFLARE_API_KEY}
      - ZONE=
      - SUBDOMAIN=
      - PROXIED=True
      - PUID=
      - PGID=
