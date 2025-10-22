# Cloudflare-DDNS

Docker Compose setup for automatically updating Cloudflare DNS records with your current public IP using the **oznu/cloudflare-ddns** container.

---

## Example `docker-compose.yml`

```yaml
version: '2'
services:
  cloudflare-ddns:
    image: oznu/cloudflare-ddns:latest
    restart: always
    environment:
      - API_KEY=${CLOUDFLARE_API_KEY}
      - ZONE=mrdtech.me
      - SUBDOMAIN=pialert.mrdtech.me,adguard.mrdtech.me,adguard2.mrdtech.me,nc.mrdtech.me,proxmox.mrdtech.me,guac.mrdtech.me,subsonic.mrdtech.me,tandoor.mrdtech.me,uk.mrdtech.me,pwndrop.mrdtech.me,wiki.mrdtech.me,piwigo.mrdtech.me,pivpn.mrdtech.me,dw.mrdtech.me,cryptgeon.mrdtech.me
      - PROXIED=True
      - PUID=1000
      - PGID=1000
