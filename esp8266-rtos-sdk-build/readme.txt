这个环境仅仅是在ubuntu的基础上，安装了必要的组件进行和编译工具链，同时预定导出IDF_PATH到路径 /opt/ESP8266_RTOS_SDK，但是需要注意的是，默认这个路径是不存在的，在启动容器时，需要用挂载指令，从windows host，将SDK整个文件夹挂在到这个下面，例如：

在windows主机上，现在自己的项目路径为 D:\wifi_sta，SDK的路径为D:\ESP8266_RTOS_SDK，那么，如果要进行menuconfig配置，可执行如下命令：
docker run --rm -it -v D:/ESP8266_RTOS_SDK:/opt/ESP8266_RTOS_SDK -v D:/wifi_sta:/mnt/project -w /mnt/project build-env/esp8266-rtos make menuconfig
这个例子是将项目挂在到了容器的/mnt/project目录下，所以也要将工作目录设置到这里（-w 选项）。
则编译命令为：
docker run --rm -it -v D:/ESP8266_RTOS_SDK:/opt/ESP8266_RTOS_SDK -v D:/wifi_sta:/mnt/project -w /mnt/project build-env/esp8266-rtos make
至于下载，直接在windows环境下载
