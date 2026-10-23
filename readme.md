root@urus:/opt/embanet# history
    1  git clone https://github.com/softwareshinobi/provision-docker-engine-cloud-ubuntu-vps.git
    2  cd provision-docker-engine-cloud-ubuntu-vps/
    3  ls
    4  bash ./provision.bash
    5  docker ps
    6  cd
    7  cd /opt
    8  mkdir embanet
    9  cd embanet/
   10  ls
   11  cd ..
   12  mv embanet/ /tmp/
   13  git clone https://github.com/softwareshinobi/shinobi-ubuntu-linux-server.git embanet
   14  cd embanet/
   15  ls
   16  ./compose.bash 
   17  ls
   18  vi compose.bash
   19  ./compose.bash 
   20  docker ps
   21  ssh -p 2222 shinobi@localhost
   22  history
   
   + docker compose down --remove-orphans
+ docker compose up -d
[+] up 7/7
 ✔ Image softwareshinobi/embanet-ubuntu-linux:sian Pulled                                                                14.9s
 ✔ Network embanet_default                         Created                                                                0.1s
 ✔ Container software-shinobi-linux                Started                                                                0.4s
root@urus:/opt/embanet# docker ps
CONTAINER ID   IMAGE                                       COMMAND               CREATED          STATUS          PORTS                                     NAMES
06efd165bf09   softwareshinobi/embanet-ubuntu-linux:sian   "/usr/sbin/sshd -D"   19 seconds ago   Up 18 seconds   0.0.0.0:2222->22/tcp, [::]:2222->22/tcp   software-shinobi-linux
root@urus:/opt/embanet# ssh -p 2222 shinobi@localhost
The authenticity of host '[localhost]:2222 ([::1]:2222)' can't be established.
ED25519 key fingerprint is: SHA256:Z8HOcQfH+NfOjGjfvjYLtVP30qKuaTL4+DRJSLcz3PQ
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[localhost]:2222' (ED25519) to the list of known hosts.
shinobi@localhost's password: 
Welcome to Ubuntu 24.04.2 LTS (GNU/Linux 7.0.0-38-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/pro

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

shinobi@sian:~$ 
