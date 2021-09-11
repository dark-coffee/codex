# Adblocking

## Pihole

Pi-hole is a DNS-based adblocker for your network. Think of it as a /etc/hosts on steriods.

### Personal Blocklists

### Pihole on Docker

Here's a docker-compose containg the useful info to spawn a pi-hole container.

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

### Links

* [Firebog.net](https://firebog.net) - a great selection of blocklists
