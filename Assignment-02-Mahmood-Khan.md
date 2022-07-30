
	|-----------------------|
	| Assignment 02		|
	| Mahmood Khan		|
	| DevOps - Batch 09	|
	|-----------------------|

Q1:-

Settings > Branch > Branch Protection Rules. Here you can add the Rule you want.
(Where to share the screenshot, i have it).

--------------------------------------X------------------------------------

Q2:-

1- VM is a separate machine sharing same hardware while Docker containers bind binaries and dependencies of each application within a container. Each container can be 
a specifice service or a sub-service of appliction.
2- VM has Hardware level process isolation while Docker container has OS level isolation.
3- Each VM has its own separate OS. Each Docker container can share the same underlying OS.
4- VM can have more resource usage. COntainers can have less resource usage.
5- VM may be upto GB's in size, while a container is only MB's,KBs in size

--------------------------------------X------------------------------------

Q3:-

OS -> Docker -> Containers (App + Binaries)
Docker Daemon (Server) + Docker Client + Registry

Client -> the cli used to interact with Docker Daemon
Daemon -> Running the actual containers
Registry -> Stores the Images

--------------------------------------X------------------------------------

Q4:-

sudo docker container run -d --publish 9090:80 --name assignment-2-MK nginx
 -d flag for detached mode

docker ps

--------------------------------------X------------------------------------

Q5:-

command:
 docker cotainer logs assignment-2-MK


Output of the command:

ubuntu@ip-172-31-94-39:~$ sudo docker container logs assignment-2-MK
/docker-entrypoint.sh: /docker-entrypoint.d/ is not empty, will attempt to perform configuration
/docker-entrypoint.sh: Looking for shell scripts in /docker-entrypoint.d/
/docker-entrypoint.sh: Launching /docker-entrypoint.d/10-listen-on-ipv6-by-default.sh
10-listen-on-ipv6-by-default.sh: info: Getting the checksum of /etc/nginx/conf.d/default.conf
10-listen-on-ipv6-by-default.sh: info: Enabled listen on IPv6 in /etc/nginx/conf.d/default.conf
/docker-entrypoint.sh: Launching /docker-entrypoint.d/20-envsubst-on-templates.sh
/docker-entrypoint.sh: Launching /docker-entrypoint.d/30-tune-worker-processes.sh
/docker-entrypoint.sh: Configuration complete; ready for start up
2022/07/22 20:55:23 [notice] 1#1: using the "epoll" event method
2022/07/22 20:55:23 [notice] 1#1: nginx/1.23.1
2022/07/22 20:55:23 [notice] 1#1: built by gcc 10.2.1 20210110 (Debian 10.2.1-6)
2022/07/22 20:55:23 [notice] 1#1: OS: Linux 5.13.0-1029-aws
2022/07/22 20:55:23 [notice] 1#1: getrlimit(RLIMIT_NOFILE): 1048576:1048576
2022/07/22 20:55:23 [notice] 1#1: start worker processes
2022/07/22 20:55:23 [notice] 1#1: start worker process 30
ubuntu@ip-172-31-94-39:~$


--------------------------------------X------------------------------------


Q6:-

command:
 docker container exec -it assignment-2-MK /bin/bash 


Output of the command:

root@a9a9701268ed:/# cat /usr/share/nginx/html/index.html
<!DOCTYPE html>
<html>
<head>
<title>Welcome to nginx!</title>
<style>
html { color-scheme: light dark; }
body { width: 35em; margin: 0 auto;
font-family: Tahoma, Verdana, Arial, sans-serif; }
</style>
</head>
<body>
<h1>Welcome to nginx!</h1>
<p>If you see this page, the nginx web server is successfully installed and
working. Further configuration is required.</p>

<p>For online documentation and support please refer to
<a href="http://nginx.org/">nginx.org</a>.<br/>
Commercial support is available at
<a href="http://nginx.com/">nginx.com</a>.</p>

<p><em>Thank you for using nginx.</em></p>
</body>
</html>
root@a9a9701268ed:/#


--------------------------------------X------------------------------------


-End-

