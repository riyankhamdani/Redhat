0. when the vm is in blackscreen condition press ctrl+alt+f2/f3/f4/f5 to bring up the cli
1. collect social report logs
#sos report

2. upgrade the packages that are in the os
#yum updateinfo list avaliable
#yum updateinfo list security all

3. update the following packages with #yum -y update
cat sos_commands/yum/yum_history 
Updating Subscription Management repositories.
Waiting for process with pid 9468 to finish.
ID     | Command line                                                       | Date and time    | Action(s)      | Altered
   7 | install traceroute                                                 | 2022-09-30 14:04 | Install        |    1   
   6 | install glibc.i686 glibc.x86_64 libstdc++.i686 libstdc++.x86_64 -y | 2022-09-30 13:53 | I, U           |    3   
   5 | install libnsl.*                                                   | 2022-09-15 14:49 | I, U           |    8  <
   4 | install telnet -y                                                  | 2022-08-16 14:13 | Install        |    1 > 
   3 | install -y perl*                                                   | 2022-08-15 10:54 | I, U           |  289 EE
   2 | localinstall -y jdk-8u341-linux-x64.rpm                            | 2022-08-15 10:51 | Install        |    1 EE
   1 |                                                                    | 2022-08-02 01:23 | Install        | 1392 EE
   
4. then run runlevel graphic.target
#systemctl set-default graphical.target
