# Pull base image.
FROM robertcnelson/machinekit-wheezy

RUN echo 'deb-src http://httpredir.debian.org/debian wheezy main' >> /etc/apt/sources.list \
  && echo 'deb-src http://httpredir.debian.org/debian wheezy-updates main' >> /etc/apt/sources.list \
  && echo 'deb-src http://security.debian.org wheezy/updates main' >> /etc/apt/sources.list \
  && echo 'deb [arch=armhf] http://repos.rcn-ee.com/debian-machinekit/ wheezy main' >> /etc/apt/sources.list \
  && gpg --keyserver keyserver.ubuntu.com --recv-keys 0xD284E608A4C46402 \
  && gpg --export 0xD284E608A4C46402  | apt-key add - \
  && echo 'deb-src [arch=armhf] http://repos.rcn-ee.com/debian-machinekit/ wheezy main' >> /etc/apt/sources.list
  
  
RUN apt-get update \
  && apt-get upgrade \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/
