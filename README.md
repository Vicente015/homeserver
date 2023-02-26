# homeserver
🛖 Docker-compose config for my Raspberry Pi

## Services
* [Homer](https://github.com/bastienwirtz/homer): a fancy homepage.
* [Pihole](https://github.com/pi-hole/docker-pi-hole): a local DNS server that blocks malware & phishing.
* [Cloudflared](https://github.com/crazy-max/docker-cloudflared): proxy-DNS for [DoH](https://developers.cloudflare.com/1.1.1.1/encryption/dns-over-https/).
* [Caddy](https://hub.docker.com/\_/caddy): reverse proxy.
* [Vaultwarden](https://github.com/dani-garcia/vaultwarden): password manager.
* [Openbooks](https://github.com/evan-buss/openbooks): ebook downloader.
* [Wallabag](https://github.com/wallabag/wallabag): read later/bookmarks app.

## Things that I usually forgot

### How to generate a local certificate

Using [mkcert](https://github.com/FiloSottile/mkcert).

1. Generate certificates:
  `mkcert home.local home.box pihole.local pihole.box vault.local vault.box openbooks.local openbooks.box wallabag.local wallabag.box tab.local tab.box memos.local memos.box`.
2. Install them on the computer and your browser:
  `mkcert -install`.
3. Make sure to copy the certificates to a `certs/` folder on the server machine and name the certificates `cert.pem` and `key.pem`.
4. Enjoy your own local domain ;).
