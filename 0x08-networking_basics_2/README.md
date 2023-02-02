# **0x08. Networking basics #1**

## Project Objectives

 General
	** What is localhost/127.0.0.1
	** What is 0.0.0.0
	** What is /etc/hosts
	** How to display your machine’s active network interfaces

* **0.Change your home IP**  (0-change_your_home_IP)
	* Bash script that configures an Ubuntu server with the below requirements.
			localhost resolves to 127.0.0.2
			facebook.com resolves to 8.8.8.8.
```
bre@bzdt:~/Desktop/python/alx-system_engineering-devops/0x08-networking_basics_2$ ping localhost
PING localhost (127.0.0.1) 56(84) bytes of data.
64 bytes from localhost (127.0.0.1): icmp_seq=1 ttl=64 time=0.047 ms
64 bytes from localhost (127.0.0.1): icmp_seq=2 ttl=64 time=0.051 ms
64 bytes from localhost (127.0.0.1): icmp_seq=3 ttl=64 time=0.042 ms
64 bytes from localhost (127.0.0.1): icmp_seq=4 ttl=64 time=0.454 ms
64 bytes from localhost (127.0.0.1): icmp_seq=5 ttl=64 time=0.432 ms
^C
--- localhost ping statistics ---
5 packets transmitted, 5 received, 0% packet loss, time 4081ms
rtt min/avg/max/mdev = 0.042/0.205/0.454/0.194 ms
bre@bzdt:~/Desktop/python/alx-system_engineering-devops/0x08-networking_basics_2$ ping facebook.com
PING facebook.com (157.240.195.35) 56(84) bytes of data.
^C
--- facebook.com ping statistics ---
11 packets transmitted, 0 received, 100% packet loss, time 10228ms

bre@bzdt:~/Desktop/python/alx-system_engineering-devops/0x08-networking_basics_2$ sudo ./0-change_your_name_IP
sudo: ./0-change_your_name_IP: command not found
bre@bzdt:~/Desktop/python/alx-system_engineering-devops/0x08-networking_basics_2$ ls
0-change_your_home_IP  README.md
bre@bzdt:~/Desktop/python/alx-system_engineering-devops/0x08-networking_basics_2$ chmod +x 0-change_your_home_IP
bre@bzdt:~/Desktop/python/alx-system_engineering-devops/0x08-networking_basics_2$ ./0-change_your_home_IP
cp: cannot remove '/etc/hosts': Permission denied
bre@bzdt:~/Desktop/python/alx-system_engineering-devops/0x08-networking_basics_2$ sudo ./0-change_your_home_IP
bre@bzdt:~/Desktop/python/alx-system_engineering-devops/0x08-networking_basics_2$ ping local host
ping: host: Temporary failure in name resolution
bre@bzdt:~/Desktop/python/alx-system_engineering-devops/0x08-networking_basics_2$ ping localhost
PING localhost (127.0.0.2) 56(84) bytes of data.
64 bytes from localhost (127.0.0.2): icmp_seq=1 ttl=64 time=0.041 ms
64 bytes from localhost (127.0.0.2): icmp_seq=2 ttl=64 time=0.051 ms
64 bytes from localhost (127.0.0.2): icmp_seq=3 ttl=64 time=0.031 ms
64 bytes from localhost (127.0.0.2): icmp_seq=4 ttl=64 time=0.041 ms
64 bytes from localhost (127.0.0.2): icmp_seq=5 ttl=64 time=0.053 ms
64 bytes from localhost (127.0.0.2): icmp_seq=6 ttl=64 time=0.053 ms
^C
--- localhost ping statistics ---
6 packets transmitted, 6 received, 0% packet loss, time 5102ms
rtt min/avg/max/mdev = 0.031/0.045/0.053/0.008 ms
bre@bzdt:~/Desktop/python/alx-system_engineering-devops/0x08-networking_basics_2$ ping facebook.com
PING facebook.com (8.8.8.8) 56(84) bytes of data.
64 bytes from facebook.com (8.8.8.8): icmp_seq=1 ttl=111 time=88.5 ms
64 bytes from facebook.com (8.8.8.8): icmp_seq=2 ttl=111 time=909 ms
64 bytes from facebook.com (8.8.8.8): icmp_seq=3 ttl=111 time=1008 ms
64 bytes from facebook.com (8.8.8.8): icmp_seq=4 ttl=111 time=850 ms
64 bytes from facebook.com (8.8.8.8): icmp_seq=5 ttl=111 time=84.7 ms
64 bytes from facebook.com (8.8.8.8): icmp_seq=6 ttl=111 time=78.2 ms
64 bytes from facebook.com (8.8.8.8): icmp_seq=7 ttl=111 time=78.0 ms
^C
--- facebook.com ping statistics ---
7 packets transmitted, 7 received, 0% packet loss, time 6008ms
rtt min/avg/max/mdev = 78.030/442.337/1007.981/417.856 ms, pipe 2
```

* **1. Show attached IPs** (1-show_attached_IPs)
	* Bash script that displays all active IPv4 IPs on the machine it’s executed on.
```
bre@bzdt:~/Desktop/python/alx-system_engineering-devops/0x08-networking_basics_2$ chmod +x 1-show_attached_IPs
bre@bzdt:~/Desktop/python/alx-system_engineering-devops/0x08-networking_basics_2$ ./1-show_attached_IPs | cat -e
.0.1$
68.0.8$

```

* **2. Port listening on localhost** (100-port_listening_on_localhost)
	*  Bash script that listens on port 98 on localhost.
```
```
