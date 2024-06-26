# _Notes

First, pull a list of RPM package by name only:

rpm -qa --queryformat='%{NAME}\n' | sort | uniq > server.txt
Once you’ve done that on both servers, just use diff to compare the two files:

diff serverold.txt servernew.txt


$ journalctl --since "-1d" -u sshd | grep "Failed password" | wc -l
$ journalctl --since "-1d" -u sshd | grep "Failed publickey" | wc -l
Finding the location of each attacker.
journalctl also provides the IP address of each login attempt. We can use this to look up and visualize the locations of the attackers. Anthropic's Claude chat model suggested the following curl snippet:


curl -s "https://ipinfo.io/$ip/loc
which yields the longitude and latitude of a given IP address.

To get all the unique IPs that have tried loggin in, Claude suggests


journalctl -u sshd | grep -oE '\b([0-9]{1,3}\.){3}[0-9]{1,3}\b' | sort -u > malicious_ips.txt