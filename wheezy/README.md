```
git clone --depth 1 --branch v1.9.1 --single-branch https://github.com/docker/docker.git
cd docker/contrib
sudo ./mkimage.sh -d . debootstrap --variant=minbase --components=main --include=inetutils-ping,iproute wheezy http://httpredir.debian.org/debian
docker build -t robertcnelson/machinekit-wheezy .
```
