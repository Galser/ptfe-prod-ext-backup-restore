# Full log of the TFE destruction

```bash
~/.../ptfe-prod-ext-backup-restore   f-kill-tfe  ssh ubuntu@tfe-ext-dr-1_backend.guselietov.com
Welcome to Ubuntu 18.04.3 LTS (GNU/Linux 4.15.0-1050-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

  System information as of Tue Nov 19 14:04:36 UTC 2019

  System load:  0.07               Users logged in:                0
  Usage of /:   13.5% of 48.41GB   IP address for ens5:            10.0.1.67
  Memory usage: 29%                IP address for docker0:         172.17.0.1
  Swap usage:   0%                 IP address for br-4f69040a6d1c: 172.18.0.1
  Processes:    217

 * Kata Containers are now fully integrated in Charmed Kubernetes 1.16!
   Yes, charms take the Krazy out of K8s Kata Kluster Konstruction.

     https://ubuntu.com/kubernetes/docs/release-notes

 * Canonical Livepatch is available for installation.
   - Reduce system reboots and improve kernel security. Activate at:
     https://ubuntu.com/livepatch

31 packages can be updated.
0 updates are security updates.


*** System restart required ***
Last login: Mon Nov 18 16:16:30 2019 from 77.162.119.95
ubuntu@ip-10-0-1-67:~$ sudo su -
root@ip-10-0-1-67:~# cat /tmp/delete_all.sh
#!/usr/bin/env bash

mountpoint /var/lib/replicated/snapshots
if [ $? -eq 0 ]; then
  umount /var/lib/replicated/snapshots
fi

[ -d /var/lib/replicated/snapshots/ ] && rsync -PavzHl /var/lib/replicated/snapshots/ ~/snap/

systemctl stop replicated replicated-operator replicated-ui
service docker stop

rm -rf /var/lib/replicated /var/lib/replicated-operator /etc/replicated.alias /var/lib/tfe-vault/ /etc/default/replicated-operator /etc/default/replicated

mkdir -p  /var/lib/replicated/snapshots
mount -a

rm -fr /var/lib/docker

service docker start

docker ps -a

[ -d ~/snap/ ] && {
  mkdir -p /var/lib/replicated/
  rsync -PavzHl ~/snap/ /var/lib/replicated/snapshots/
}


root@ip-10-0-1-67:~# bash /tmp/delete_all.sh
/var/lib/replicated/snapshots is not a mountpoint
sending incremental file list
./
files/
files/db.dump
         74,767 100%   40.05MB/s    0:00:00 (xfr#1, to-chk=22/27)
sha256/
sha256/0cf5297d0cd91fe3f55b55fee2be7d8eea9d49c57ffdef3babe2bcd5e37ff501
         34,437 100%   16.42MB/s    0:00:00 (xfr#2, to-chk=21/27)
sha256/0de8d71f699f8110f3f2e68e25c2fd72fc1fe1ba5ea617574683dbce1ebd3d82
        135,307 100%   14.34MB/s    0:00:00 (xfr#3, to-chk=20/27)
sha256/0f478b53352baf4e59700f4e1aa69d0307b36f0089203db712d3b11031e4b57d
            985 100%   87.45kB/s    0:00:00 (xfr#4, to-chk=19/27)
sha256/21785a1bd8ed2d46d424248ecbdb4b17f86193334afc19e0b840f87f48f25699
          1,649 100%  146.40kB/s    0:00:00 (xfr#5, to-chk=18/27)
sha256/30e6fa98fb48c2b132824d1ac5e2243c0be9e9082ff32598d34d7687ca7f6c7f
             23 100%    1.87kB/s    0:00:00 (xfr#6, to-chk=17/27)
sha256/492ba3fae1d6527671f64453bc30ecb699f2cc54ed229031b8b78ec0e55994a3
          1,481 100%  120.52kB/s    0:00:00 (xfr#7, to-chk=16/27)
sha256/4b9167ee49c3619f1488cdd1288a6f38d338b405d2763bb174e570a551db45de
          1,308 100%   98.26kB/s    0:00:00 (xfr#8, to-chk=15/27)
sha256/5da7a3381d00dcbde721fbf989817aa2b9b397e918523d6e8ab7bdb2a6d72f95
          1,416 100%   92.19kB/s    0:00:00 (xfr#9, to-chk=14/27)
sha256/63e9949e2bcea2232d7bb1abbf737cf1bac0945fb33e04189d558402e5ff9a57
            866 100%   56.38kB/s    0:00:00 (xfr#10, to-chk=13/27)
sha256/6a6ea1559d88bed0147db187dbe9977da6e67dc72ed252f9a18b540a24d6b29e
         34,263 100%    1.92MB/s    0:00:00 (xfr#11, to-chk=12/27)
sha256/6c539c65758117be8ee377b423da6d4103bf1c47fca76eb577a066656c0c5e8e
     55,147,960 100%   24.76MB/s    0:00:02 (xfr#12, to-chk=11/27)
sha256/98da21cc529fa2dfe691e0dedf6f83c1c2d918185328e2037596fff3ee134723
      7,830,416 100%   17.09MB/s    0:00:00 (xfr#13, to-chk=10/27)
sha256/9d02699d7db945bf63e8451330dcdbdcd560063cfe5482ec11d9193afda9fb8d
             25 100%    0.06kB/s    0:00:00 (xfr#14, to-chk=9/27)
sha256/9ec00a9f9efb58ec418374864477ff15ceb82a4dfac4d77e9c992084bad451c7
     22,225,136 100%   16.28MB/s    0:00:01 (xfr#15, to-chk=8/27)
sha256/a26e07d9c05aa27fe14b68d19ce59f65e3440e7005092e287e8aef91fb21c0ac
             62 100%    0.20kB/s    0:00:00 (xfr#16, to-chk=7/27)
sha256/adda514f7168a68ed2b8085d6879a11d38b1744174a46a04ad94f5d971887e8d
            269 100%    0.87kB/s    0:00:00 (xfr#17, to-chk=6/27)
sha256/b2fa04fc68821ea884887ab633cddc670c257578bd8f0d6f7e7f838e55e06e5e
        135,478 100%  426.78kB/s    0:00:00 (xfr#18, to-chk=5/27)
sha256/bde4c101d1728f62d89c500dd3d0f3b3f24447820dd280763f803a97d2f7c94e
          1,306 100%    4.11kB/s    0:00:00 (xfr#19, to-chk=4/27)
sha256/d1eaa4660173df839d10da849b3f640c2bd0b421274c2e1105d2ab8ead71e2be
          1,309 100%    4.11kB/s    0:00:00 (xfr#20, to-chk=3/27)
sha256/f1d0504c62a0a74ad669ef6a4b96bdc681231f7d2d68e61ee90d99e819be6882
     14,289,665 100%   15.45MB/s    0:00:00 (xfr#21, to-chk=2/27)
sha256/f3006b5f0d243c0399fdaca755a80697bb8410d2e7656d4d1f41c7f42291c152
            115 100%    0.13kB/s    0:00:00 (xfr#22, to-chk=1/27)
sha256/fe1278b0a1c542741f1f8680d4789527499b901c66a31d1c8fc9eedc9b7279e1
            884 100%    0.98kB/s    0:00:00 (xfr#23, to-chk=0/27)
tmp/

sent 99,906,513 bytes  received 476 bytes  22,201,553.11 bytes/sec
total size is 99,919,127  speedup is 1.00
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
sending incremental file list
./
amazon-ssm-agent/
amazon-ssm-agent/current -> 1480
amazon-ssm-agent/1455/
amazon-ssm-agent/1480/
amazon-ssm-agent/common/
files/
files/db.dump
         74,767 100%   40.05MB/s    0:00:00 (xfr#1, to-chk=22/32)
sha256/
sha256/0cf5297d0cd91fe3f55b55fee2be7d8eea9d49c57ffdef3babe2bcd5e37ff501
         34,437 100%   32.84MB/s    0:00:00 (xfr#2, to-chk=21/32)
sha256/0de8d71f699f8110f3f2e68e25c2fd72fc1fe1ba5ea617574683dbce1ebd3d82
        135,307 100%   21.51MB/s    0:00:00 (xfr#3, to-chk=20/32)
sha256/0f478b53352baf4e59700f4e1aa69d0307b36f0089203db712d3b11031e4b57d
            985 100%  160.32kB/s    0:00:00 (xfr#4, to-chk=19/32)
sha256/21785a1bd8ed2d46d424248ecbdb4b17f86193334afc19e0b840f87f48f25699
          1,649 100%  230.05kB/s    0:00:00 (xfr#5, to-chk=18/32)
sha256/30e6fa98fb48c2b132824d1ac5e2243c0be9e9082ff32598d34d7687ca7f6c7f
             23 100%    3.21kB/s    0:00:00 (xfr#6, to-chk=17/32)
sha256/492ba3fae1d6527671f64453bc30ecb699f2cc54ed229031b8b78ec0e55994a3
          1,481 100%  206.61kB/s    0:00:00 (xfr#7, to-chk=16/32)
sha256/4b9167ee49c3619f1488cdd1288a6f38d338b405d2763bb174e570a551db45de
          1,308 100%  182.48kB/s    0:00:00 (xfr#8, to-chk=15/32)
sha256/5da7a3381d00dcbde721fbf989817aa2b9b397e918523d6e8ab7bdb2a6d72f95
          1,416 100%  197.54kB/s    0:00:00 (xfr#9, to-chk=14/32)
sha256/63e9949e2bcea2232d7bb1abbf737cf1bac0945fb33e04189d558402e5ff9a57
            866 100%  120.81kB/s    0:00:00 (xfr#10, to-chk=13/32)
sha256/6a6ea1559d88bed0147db187dbe9977da6e67dc72ed252f9a18b540a24d6b29e
         34,263 100%    4.08MB/s    0:00:00 (xfr#11, to-chk=12/32)
sha256/6c539c65758117be8ee377b423da6d4103bf1c47fca76eb577a066656c0c5e8e
     55,147,960 100%   28.72MB/s    0:00:01 (xfr#12, to-chk=11/32)
sha256/98da21cc529fa2dfe691e0dedf6f83c1c2d918185328e2037596fff3ee134723
      7,830,416 100%    6.85MB/s    0:00:01 (xfr#13, to-chk=10/32)
sha256/9d02699d7db945bf63e8451330dcdbdcd560063cfe5482ec11d9193afda9fb8d
             25 100%    0.27kB/s    0:00:00 (xfr#14, to-chk=9/32)
sha256/9ec00a9f9efb58ec418374864477ff15ceb82a4dfac4d77e9c992084bad451c7
     22,225,136 100%   25.51MB/s    0:00:00 (xfr#15, to-chk=8/32)
sha256/a26e07d9c05aa27fe14b68d19ce59f65e3440e7005092e287e8aef91fb21c0ac
             62 100%    0.07kB/s    0:00:00 (xfr#16, to-chk=7/32)
sha256/adda514f7168a68ed2b8085d6879a11d38b1744174a46a04ad94f5d971887e8d
            269 100%    0.32kB/s    0:00:00 (xfr#17, to-chk=6/32)
sha256/b2fa04fc68821ea884887ab633cddc670c257578bd8f0d6f7e7f838e55e06e5e
        135,478 100%  158.26kB/s    0:00:00 (xfr#18, to-chk=5/32)
sha256/bde4c101d1728f62d89c500dd3d0f3b3f24447820dd280763f803a97d2f7c94e
          1,306 100%    1.53kB/s    0:00:00 (xfr#19, to-chk=4/32)
sha256/d1eaa4660173df839d10da849b3f640c2bd0b421274c2e1105d2ab8ead71e2be
          1,309 100%    1.53kB/s    0:00:00 (xfr#20, to-chk=3/32)
sha256/f1d0504c62a0a74ad669ef6a4b96bdc681231f7d2d68e61ee90d99e819be6882
     14,289,665 100%   10.41MB/s    0:00:01 (xfr#21, to-chk=2/32)
sha256/f3006b5f0d243c0399fdaca755a80697bb8410d2e7656d4d1f41c7f42291c152
            115 100%    0.36kB/s    0:00:00 (xfr#22, to-chk=1/32)
sha256/fe1278b0a1c542741f1f8680d4789527499b901c66a31d1c8fc9eedc9b7279e1
            884 100%    2.78kB/s    0:00:00 (xfr#23, to-chk=0/32)
tmp/

sent 99,906,697 bytes  received 495 bytes  28,544,912.00 bytes/sec
total size is 99,919,131  speedup is 1.00
root@ip-10-0-1-67:~# logout
ubuntu@ip-10-0-1-67:~$ logout
Connection to tfe-ext-dr-1_backend.guselietov.com closed.
```
