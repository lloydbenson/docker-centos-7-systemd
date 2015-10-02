# docker-centos-7-systemd

A base image for installing systemd on centos 7

```sh
docker pull lloydbenson/docker-centos-7-systemd
```

Note: Looking around I kept seeing references for removing fakesystemd.  However, I never found such a package with the latest centos 7.  Instead it was called systemd-container and systemd-container-libs.  I remove these and install just standard systemd.  You can build on top of this and just make sure you start /usr/sbin/init as the final thing and it will start up your services.  You likely need --privileged=true in your run for this to be useful.
