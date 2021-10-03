# Adblocking

## Pi-hole

Pi-hole is a DNS-based adblocker for your network. Think of it as /etc/hosts on steriods.  
_no, you can't block youtube ads_

### Personal Blocklists

I maintain a list of the blocklists I use, [here](https://github.com/dark-coffee/keylime)

### Pi-hole on Docker

Here's a docker-compose containg the useful info to spawn a pi-hole container.

> **Important:** this is a generic pi-hole installation, with some personal preferences.  
> DNS points to the malware-blocking Cloudflare resolver, but I can also highly recommend Quad9.

```yml
version: "3.3"

services:
  pihole:
    container_name: pihole
    image: pihole/pihole:latest
    hostname: pihole
    ports:
      - "53:53/tcp"
      - "53:53/udp"
      - "80:80/tcp"
    environment:
      TZ: "Europe/London"
      WEBPASSWORD: "<web-password>"
      ServerIP: "<ip-address>"
      PIHOLE_DNS_: "1.1.1.2;1.0.0.2"
      DNSSEC: "true"
      BLOCK_ICLOUD_PR: "true"
      WEBUIBOXEDLAYOUT: "traditional"
      WEBTHEME: "default-dark"
      REV_SERVER: "true"
      REV_SERVER_TARGET: "<gateway-ip>"
      REV_SERVER_CIDR: "<ip-cidr>/24"
    volumes:
      - "./etc-pihole/:/etc/pihole/"
      - "./etc-dnsmasq.d/:/etc/dnsmasq.d/"
    cap_add:
      - NET_ADMIN
    restart: unless-stopped
```

To persist data, the container mounts the host locations `./etc-pihole/` & `./etc-dnsmaq.d/`

> To combat iCloud Private Relay, which bypasses pihole, the additional option `BLOCK_ICLOUD_PR: "true"` has now been added.

**File Breakdown:**
| Element | Meaning |
| ------- | ------- |
| TZ | Standard Format Timezone |
| WEBPASSWORD | Web Console Password |
| PIHOLE_DNS_ | Target DNS Servers (Pihole will forward requests to these addresses |
| BLOCK_ICLOUD_PR | Drop iCloud Private Relay DNS Requests |

### Links

- [Pi-Hole](https://pi-hole.net) - The official Pi-Hole website
- [Firebog.net](https://firebog.net) - a great selection of blocklists
- [1.1.1.2](https://one.one.one.one/family/) - Cloudflare's DNS resolver site
- [Quad9](https://www.quad9.net) - Quad9 homepage
