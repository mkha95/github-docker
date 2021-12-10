FROM --platform=linux/amd64 ubuntu:latest

RUN apt-get update \
	&& apt-get install -y \
        git \
		vim \
		ssh \
		sudo\
		wget\
		software-properties-common ;\
		rm -rf /var/lib/apt/lists/*

# add and enable the default user
ARG USER=ithacafv
RUN adduser --disabled-password --gecos '' $USER
RUN adduser $USER sudo; echo '%sudo ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers
