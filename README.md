# XFINITY-WIFI-LOGIN
How to log into secure "XFINITY" wifi hotspots (not open "xfinitywifi") on ubuntu linux

## Prerequisites
1. XFINITY secure network is ONLY 5GHz, must have an Wifi device capable of 5 GHz A or AC
2. 5 GHz wifi device must have an installed and WORKING Linux driver.

## Configure Security Via Settings->Wi-Fi
After clicking on XFINITY network
|Parameters|Value|
|---|---|
|Security|**WPA & WPA2 Enterprise**|
|Authentication|**Tunneled TLS**|
|Anonymous identity|_Leave this empty_|
|Domain|**secure.aaa.wifi.xfinity.com**|
|CA Certificate|_Select **file /usr/share/ca-certificate/mozilla/Comodo_AAA_Services_root.crt**_|
|No CA Certificate is required|_Leave unchecked_|
|Inner Authentication|**PAP**|
|Username|_Your comcast email account_|
|Password|_Your comcast password_|

## Configure wpa_supplicant.conf
_Add to the current file_
network={
    ssid="XFINITY"
    scan_ssid=1
    key_mgmt=WPA-EAP
    eap=TTLS
    domain="secure.aaa.wifi.xfinity.com"
    phase2="auth=PAP"
    identity="**Your Comcast Account/Emailaddress**"
    password="**Your Comcast Account Password**"
    
}
