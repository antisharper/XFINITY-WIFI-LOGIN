# XFINITY-WIFI-LOGIN
How to log into secure "XFINITY" wifi hotspots (not open "xfinitywifi") on ubuntu linux

## Prerequisites
1. XFINITY secure network is ONLY 5GHz, must have an Wifi device capable of 5 GHz A or AC
2. 5 GHz wifi device must have an installed and WORKING Linux driver.

## Configure Security Via Settings->Wi-Fi
1. After clicking on XFINITY network
2. Parameters:
. Security: *WPA & WPA2 Enterprise*
. Authentication: *Tunneled TLS*
. Anonymous identity: _Leave this empty_
. Domain: *secure.aaa.wifi.xfinity.com*
. CA Certificate: _Select file /usr/share/ca-certificate/mozilla/Comodo_AAA_Services_root.crt_
. No CA Certificate is required: _Leave unchecked_
. Inner Authentication: *PAP*
. Username: _Your comcast email account_
. Password: _Your comcast password_
