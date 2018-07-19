FROM ubuntu AS esp8266-rtos-sdk-build
MAINTAINER  liu.i@outlook.com

#load aliyun sources.list
COPY sources.list /etc/apt/sources.list

#setting Tinezone info
ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

#update system and install soft
RUN apt update
RUN apt install -y make \
				unrar-free \
				autoconf \
				automake \
				libtool \
				gcc \
				g++ \
				gperf \
				flex \
				bison \
				texinfo \
				gawk \
				ncurses-dev \
				libexpat-dev \
				python-dev \
				python \
				python-serial \
				sed \
				git \
				unzip \
				bash \
				help2man \
				wget \
				bzip2 \
				vim
				
#clone ESP8266 SDK
#RUN git clone https://github.com/espressif/ESP8266_RTOS_SDK.git /opt/ESP8266_RTOS_SDK

#dowload toolchain and untar
RUN wget https://dl.espressif.com/dl/xtensa-lx106-elf-linux64-1.22.0-88-gde0bdc1-4.8.5.tar.gz
RUN tar -zxf xtensa-lx106-elf-linux64-1.22.0-88-gde0bdc1-4.8.5.tar.gz -C /opt/

#then, delete tar package
RUN rm xtensa-lx106-elf-linux64-1.22.0-88-gde0bdc1-4.8.5.tar.gz

#set env value
ENV IDF_PATH="/opt/ESP8266_RTOS_SDK"
ENV PATH="${PATH}:/opt/xtensa-lx106-elf/bin"