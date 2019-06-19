# MEOPUBLICIP
## How change MEO public ip

### LOGIN TELNET
TELNET 192.168.1.254 ```
ACCESS: ```
USERNAME: sumeo ```
PASSWORD: bfd,10ng ```

### COMMANDS TO FIBER:
dhcp client ifdetach intf=InternetGPON ```
dhcp client ifattach intf=InternetGPON ```


### COMMANDS TO ADSL:
dhcp client ifdetach intf=InternetADSL
dhcp client ifattach intf=InternetADSL

### (OPTIONAL) STATUS:
dhcp client iflist


REPEAT COMMANDS ALL TIMES YOU WANT FOR GET DIFFERENT IP.

## (NOT RECOMMENDED)
## DISABLE IPV6:
dhcp serverv6 config state=disabled
ip ifconfig intf=LocalNetwork ipv6=disabled
saveall

## REVERT:
dhcp serverv6 config state=enabled
ip ifconfig intf=LocalNetwork ipv6=enabled
saveall
