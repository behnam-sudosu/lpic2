# monitoring  

    subnet 192.168..1.0/24
    netmask 255.255.255.0

---  

#### install package

```bash
sudo apt install stress-ng
sudo apt install sysstat
sudo apt install iotop
sudo apt install nload
sudo apt install iperf
sudo apt install net-tools
sudo apt install iptrf-ng
sudo apt install iftop
sudo apt install ethtool
```

# memory and cpu and disk monitoring

#### vmstat  

```bash
#show memory, cpu, swap, disk
vmstat  
``` 
---  

#### free  

```bash
#show memory
free  
```
```bash
    #megabite         |       #human readable       |       #gigabite       |       #show memory live    
     free -m          |          free -h            |        free -g        |          watch free
```
---  

#### top  

```bash
#show cpu, memory, swap, disk  
top  
```
```bash
    #show all core cpu   |         #delay           |       #kill process id       |      #change memory shows
           1             |           d              |            k                 |             m  
-----------------------------------------------------------------------------------------------------------------
    #renice process      |    #change cpu shows     |            #sort             |       #procesor sort
       r=-20,19          |           t              |         shift + <>           |         shift + P  
-----------------------------------------------------------------------------------------------------------------
    #memory sort         |     #absulute PATH       |        #change color         |           #quit
       shift + m         |           c              |            z                 |             q
```

#### information that top show you

```bash
    time 	    |   user            |   load average  1sec  5sec  15sec         |
--------------------------------------------------------------------------------------------------------------
	tasks	    |   running		    |   sleep           |   stopped             |   zombie  
--------------------------------------------------------------------------------------------------------------
	cpu		    |   us=user         |   sy=system       | ni=prority system     |   id=cpu idle
                |   wa=wait disk    |   hi=hardware     |   si=software         |   st=cpu  
--------------------------------------------------------------------------------------------------------------
	memory	    |	total	        |  	free            |   used                |   buff/cache  
--------------------------------------------------------------------------------------------------------------
	swap	    |	total	        | 	free            |   used                |   avail  
```

---  

#### stress-ng

```bash
    #-c=cpu, 1=core        |       #-m=memory           |       #--hdd=disk
     stress-ng -c 1        |     stress-ng -m 5         |     stress-ng --hdd 3
 
```

---  

#### htop

```bash
htop
```

```bash
    #show all core cpu   |         #delay           |       #kill process id       |      #change memory shows
         1               |           d              |            k                 |             m  
------------------------------------------------------------------------------------------------------------------
    #renice process      |    #change cpu shows     |            #sort             |       #procesor sort
       r=-20,19          |           t              |         shift + <>           |         shift + P  
------------------------------------------------------------------------------------------------------------------
    #memory sort         |     #absulute PATH       |        #change color         |           #quit
       shift + m         |           c              |            z                 |             q
```

---  

#### uptime

```bash
#server up, users, load average  
#load average  1sec  5sec  15sec
uptime  
```

---  

#### iotop  

```bash
#usege disk
iotop
```

---  

#### sar

```bash
#show cpu, nice, user, system, iowait, idle
#1=sec, 10=repeat
sar 1 10
```

# network monitoring

#### ifconfig

```bash
#show cart network name, ip, netmask, broadcat, macaddress, mtu
#RX packets, RX errirs, TX packets, TR errors
ifconfig

#set ip temparary
ifconfig ens37 192.168.1.100 netmask 255.255.255.0 up  

#up and down interface  
ifconfig ens37 up  
ifconfig ens37 down  

#more information  
ifconfig ens37
```

---  

#### netstat

```bash
#show cart network name, ip, netmask, broadcat, macaddress, mtu
#RX packets, RX errirs, TX packets, TR errors
netstat -ie

#more information (protocol)
netstat -s
```

---  

#### iftop

```bash
#show live packet send and resive
iftop

#show live
iftop -i ens37
```

---  

#### nload

```bash
#show live packet send and resive
nload

#show live packet send and resive on ens37
nload ens37
```

---  

#### ethtool

```bash
#more information
ethtool ens37

#see error
ethtool -S ens37
```

---  

#### iperf

```bash
#show transfer and bandwidth between server and client
#server (port=5001)  
iperf -s  

#client  
iperf -c IP_SERVER
```

---  

#### iptraf-ng

```bash
#show live packet send and resive on ens37
iptraf-ng -i ens37
```