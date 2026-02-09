# netdata  

```bash
#install package
wget -O /tmp/netdata-kickstart.sh https://get.netdata.cloud/kickstart.sh && sh /tmp/netdata-kickstart.sh  
```
```bash
#check port is open (port=19999)
ss -ntlp  
```

---  

#### open browser  

```bash
#show cpu, ram, load, disk, swap
#find your IP_SERVER  
ip -br a  

#write this in browser  
192.168.1.100:19999  
```