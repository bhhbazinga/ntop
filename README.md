# ntop
A bpf-bcc tool used to show top N transport layer traffic.

## Install
```
sudo apt-get install python3-bpfcc
sudo apt-get install bpfcc-tools
```

## Usage
```
usage: ntop [-h] [-i INTERFACE] [-t] [-u] [-p PORT] [-n NUMBER] [-s SECOND]  

bpfcc tool, used to show top n traffic  

optional arguments:  
  -h, --help            show this help message and exit  
  -i INTERFACE, --interface INTERFACE  
                        capture interface name  
  -t, --tcp             capture tcp traffic  
  -u, --udp             capture udp traffic  
  -p PORT, --port PORT  capture remote port  
  -n NUMBER, --number NUMBER  
                        show n top traffic  
  -s SECOND, --second SECOND  
                        time interval, seconds  
```                        

sudo ./ntop
```
PROTOCOL                ADDRESS     TX B/s     RX B/s                 COMM
tcp          192.168.1.20:33442        252        122           v2ray,sshd
tcp          192.168.1.20:10822        238        134           v2ray,sshd
tcp             127.0.0.1:11633        205         77            sshd,node
tcp           172.217.161.67:80        278          0
tcp             127.0.0.1:32744         92         57                 node
udp            192.168.1.254:53         63         71
tcp             127.0.0.1:32736         55         25            sshd,node
tcp             127.0.0.1:50996         29          0                 node
```
