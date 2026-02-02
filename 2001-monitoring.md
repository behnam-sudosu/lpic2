# monitoring  

## install package

```bash
sudo apt install stress-ng
sudo apt install sysstat
sudo apt install iotop
sudo apt install nload
sudo apt install iperf
sudo apt install net-tools
sudo apt install iptrf-ng
sudo apt install 
sudo apt install 
sudo apt install 
sudo apt install 
```

# memory and cpu monitoring

### vmstat  

```bash
#show memory, cpu, swap, disk 
vmstat  
``` 
---  
### free  

```bash
#show memory
free  

#megabite
free -m

#human readable
free -h

#gigabite
free -g  

#show memory live
watch free
```
---  
### top  

```bash
#show cpu, memory, swap, disk  
top  

#show all core cpu
1  

#delay  
d  

#kill process id  
k  

#renice process  
r  
```
---  
stress-ng -c 1
htop
uptime
htop
sar 1 10

# network
    ifconfig
    netstat -s or -ie
    iftop
    nload
    iperf -s
    iperf -c (ip server)
    iptraf-ng -i ens37

# graph
    cacti
    zabbix
    grafana
    netdata
    collectd
    collectd web





