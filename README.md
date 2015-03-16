# fedora-docker-image-import

An exciting tool to take the tarball currently produced by
ImageFactory-in-Koji and insert correct metadata (i.e. "fedora:22" as
a tag, not `Fedora-Docker-Base-22-20150316.x86_64:latest`), then pass
it to `docker load`.

    root@host# fedora-docker-image-import Fedora-Docker-Base-22-20150316.x86_64.tar.gz fedora:22
    root@host# docker run -ti --rm fedora:22 cat /etc/fedora-release
    Fedora release 22 (Twenty Two)
    root@host#



