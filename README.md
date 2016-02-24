# zabbix-docker
Template for monitoring docker
Tested on CentOS 6.x and CentOS 7.x
#Usage
Include Template.Docker.conf to zabbix_agentd.conf file
#Supported Items
docker.container.discovery - Discovery containers
docker.container.count - Count containers
docker.stat[*] - with 3 arguments, 1 argument - file name in cgroup fs (memory.stat - by example), 2 argument - Full ID Container, 3 argument required if file usage more one parameter 
 docker.stat[memory.stat,ddddddffff,swap] - for get value from line "swap 0"
 docker.stat[memory.usage_in_bytes,ddddddffffff] - for get va.ue from file memory.usage_in_bytes
docker.status[*] - with 1 argument Full ID Container, check up/down status of container
