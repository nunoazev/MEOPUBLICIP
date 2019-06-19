# MEOPUBLICIP
## How change MEO public ip

#### LOGIN TELNET 
TELNET 192.168.1.254<br/>
USERNAME: sumeo<br/>
PASSWORD: bfd,10ng<br/>

#### COMMANDS TO FIBER:
dhcp client ifdetach intf=InternetGPON<br/> 
dhcp client ifattach intf=InternetGPON<br/>


#### COMMANDS TO ADSL: 
dhcp client ifdetach intf=InternetADSL<br/>
dhcp client ifattach intf=InternetADSL<br/>

#### (OPTIONAL) STATUS:
dhcp client iflist


REPEAT COMMANDS ALL TIMES YOU WANT FOR GET DIFFERENT IP.

---

### (NOT RECOMMENDED)
### DISABLE IPV6:
dhcp serverv6 config state=disabled<br/>
ip ifconfig intf=LocalNetwork ipv6=disabled<br/>
saveall

### REVERT:
dhcp serverv6 config state=enabled<br/>
ip ifconfig intf=LocalNetwork ipv6=enabled<br/>
saveall<br/>
