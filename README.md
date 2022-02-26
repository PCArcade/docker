# Server application documentation and links to the projects used  

Full list of services enabled by this docker file:  
  
asf - farms steam cards - https://github.com/JustArchiNET/ArchiSteamFarm/releases  
dockerproxy - a security-enhanced proxy for the Docker Socket - https://github.com/Tecnativa/docker-socket-proxy  
Netdata - system monitoring - https://www.netdata.cloud/  
MariaDB - database - https://mariadb.org/  
open-vpn - open VPN solution - https://openvpn.net/  
heimdall - web based frontend - https://heimdall.site/  
nzbget - usenet client - https://nzbget.net/  
sonarr - TV Series management tool - https://nzbget.net/  
radarr - Movie management tool - https://radarr.video/  
jackett - Index management tool - https://github.com/Jackett/Jackett  
swag - Secure Web Application Gateway (nginx webserver and reverse proxy) - https://github.com/linuxserver/docker-swag  
deemix - Deezer client - https://gitlab.com/Bockiii/deemix-docker  
deluge - bittorrent client - https://www.deluge-torrent.org/  
ddclient - updates dynamic dns - https://github.com/linuxserver/docker-ddclient/pkgs/container/ddclient  
flaresolver - proxy server to bypass Cloudflare protection - https://github.com/FlareSolverr/FlareSolverr  
plex - media streaming client - https://www.plex.tv/  
ombi - add wanted media to *arr - https://ombi.io/  
lidarr - Music management tool - https://lidarr.audio/  
pihole - Network-wide Ad Blocking  - https://pi-hole.net/  
unbound - recursive, caching DNS resolver - https://pi-hole.net/

# instructions for updating pihole

After docker-compose up -d:

docker exec -it pihole /bin/bash

apt update  
apt install python3 nano  
curl -sSl https://raw.githubusercontent.com/mmotti/pihole-regex/master/install.py | python3  
crontab -e  

## add the following then save and exit - the updates regex filters automatically

SHELL=/bin/bash  
PATH=/usr/local/sbin:/usr/local/bin:/sbin:/bin:/usr/sbin:/usr/bin  
30 2 * * 1 /usr/bin/curl -sSl https://raw.githubusercontent.com/mmotti/pihole-regex/master/install.py | /usr/bin/pytho  

# blocklists 

## Firebog

https://zerodot1.gitlab.io/CoinBlockerLists/hosts_browser  
https://raw.githubusercontent.com/DandelionSprout/adfilt/master/Alternate%20versions%20Anti-Malware%20List/AntiMalwareHosts.txt  
https://osint.digitalside.it/Threat-Intel/lists/latestdomains.txt  
https://s3.amazonaws.com/lists.disconnect.me/simple_malvertising.txt  
https://v.firebog.net/hosts/Prigent-Crypto.txt  
https://bitbucket.org/ethanr/dns-blacklists/raw/8575c9f96e5b4a1308f2f12394abd86d0927a4a0/bad_lists/Mandiant_APT1_Report_Appendix_D.txt  
https://phishing.army/download/phishing_army_blocklist_extended.txt  
https://gitlab.com/quidsup/notrack-blocklists/raw/master/notrack-malware.txt  
https://raw.githubusercontent.com/Spam404/lists/master/main-blacklist.txt  
https://raw.githubusercontent.com/FadeMind/hosts.extras/master/add.Risk/hosts  
https://urlhaus.abuse.ch/downloads/hostfile/  
https://v.firebog.net/hosts/Easyprivacy.txt  
https://v.firebog.net/hosts/Prigent-Ads.txt  
https://raw.githubusercontent.com/FadeMind/hosts.extras/master/add.2o7Net/hosts  
https://raw.githubusercontent.com/crazy-max/WindowsSpyBlocker/master/data/hosts/spy.txt  
https://hostfiles.fhttps://adaway.org/hosts.txt  
https://v.firebog.net/hosts/AdguardDNS.txt  
https://v.firebog.net/hosts/Admiral.txt  
https://raw.githubusercontent.com/anudeepND/blacklist/master/adservers.txt  
https://s3.amazonaws.com/lists.disconnect.me/simple_ad.txt  
https://v.firebog.net/hosts/Easylist.txt  
https://pgl.yoyo.org/adservers/serverlist.php?hostformat=hosts&showintro=0&mimetype=plaintext  
https://raw.githubusercontent.com/FadeMind/hosts.extras/master/UncheckyAds/hosts  
https://raw.githubusercontent.com/bigdargon/hostsVN/masthttps://raw.githubusercontent.com/PolishFiltersTeam/KADhosts/master/KADhosts.txt  
https://raw.githubusercontent.com/FadeMind/hosts.extras/master/add.Spam/hosts  
https://v.firebog.net/hosts/static/w3kbl.txter/hostsrogeye.fr/firstparty-trackers-hosts.txt  

## Developer Dan's  
https://www.github.developerdan.com/hosts/lists/ads-and-tracking-extended.txt  
https://www.github.developerdan.com/hosts/lists/amp-hosts-extended.txt  
https://www.github.developerdan.com/hosts/lists/dating-services-extended.txt  
https://www.github.developerdan.com/hosts/lists/hate-and-junk-extended.txt  
https://www.github.developerdan.com/hosts/lists/tracking-aggressive-extended.txt  

## Whitelist to enable achievements  
attestation.xboxlive.comcert.mgt.xboxlive.com  
ctldl.windowsupdate.comdef-vef.xboxlive.com  
device.auth.xboxlive.comeds.xboxlive.com  
help.ui.xboxlive.comlicensing.xboxlive.commicrosoft.com  
notify.xboxlive.comsettings-win.data.microsoft.com  
title.auth.xboxlive.comtitle.mgt.xboxlive.com  
v10.vortex-win.data.microsoft.com  
www.msftncsi.com  
xbox.ipv6.microsoft.com  
xboxexperiencesprod.experimentation.xboxlive.com  
xflight.xboxlive.comxkms.xbolive.com  
xsts.auth.xboxlive.com  
v20.events.data.microsoft.com  
watson.telemetry.microsoft.com  
web.vortex.data.microsoft.com  
v10.events.data.microsoft.com  
