FROM ubuntu:22.04
CMD ["bash"]
LABEL maintainer=ismail.nazwan72@gmail.com
LABEL version=1.0.0
RUN apt-get update

RUN apt-get install -y sudo nano git curl npm yarn
RUN curl -sL https://deb.nodesource.com/setup_20.x | bash -
RUN apt-get -y install nodejs

RUN echo "root:root" | chpasswd
RUN useradd -m user
RUN echo "user:user" | chpasswd user
RUN adduser user sudo
USER user

RUN npm install -g corepack
RUN corepack enable
RUN yarn set version berry

RUN mkdir /usr/src/app