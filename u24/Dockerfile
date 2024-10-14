# Base image
FROM ubuntu

ENV pkg="net-tools curl iproute2 inetutils-ping openssh-client telnet lsof tree dnsutils htop ncdu w3m vim"

# Install.
RUN apt-get update
RUN apt-get install -y $pkg
RUN DEBIAN_FRONTEND="noninteractive" apt-get install -y tzdata
RUN rm -rf /var/lib/apt/lists/*
RUN ln -fs /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
RUN dpkg-reconfigure -f noninteractive tzdata

# Add files.
#ADD .bashrc /root/.bashrc

# Define working directory.
WORKDIR /
RUN mkdir /readme
RUN echo $pkg > /readme/installedPackage.txt

# 容器默认启动命令
ENTRYPOINT ["bash"]
