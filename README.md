# XMRIG Proxy

Version v5.11

Usage example:
`docker run --restart unless-stopped -d -p 3333:3333 techcf/xmrig-proxy --coin=monero -o pool.xxx:5555 -u your-wallet-address -p x --bind 0.0.0.0:3333`

For running on unraid (add container/advanced settings). Only settings that differ from defaults are listed. Change command line to suit your config:

Name: **xmrig-proxy**
Repository: **techcf/xmrig-proxy**
Icon URL: https://raw.githubusercontent.com/pebroz/xmrig-proxy/master/xmrig-proxy-icon.png
Post Arguments: `--coin=monero --mode=simple -o randomxmonero.eu.nicehash.com:3380 -u wallet.minerid -p password -b 0.0.0.0:80 --tls-cert=/le-ssl/live/domain.com/fullchain.pem --tls-cert-key=/le-ssl/live/domain.com/privkey.pem --tls-bind=0.0.0.0:443 --no-color`

Map two ports. E.g.: `80:80` and `443:443`
Map a drive for SSL certs. E.g.: `/le-ssl:/mnt/user/appdata/letsencrypt/etc/letsencrypt/`

Certs are made with [linuxserver/docker-letsencrypt](https://forums.unraid.net/topic/51808-support-linuxserverio-letsencrypt-nginx/) (you'll find it in community apps).