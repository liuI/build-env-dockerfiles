���������������ubuntu�Ļ����ϣ���װ�˱�Ҫ��������кͱ��빤������ͬʱԤ������IDF_PATH��·�� /opt/ESP8266_RTOS_SDK��������Ҫע����ǣ�Ĭ�����·���ǲ����ڵģ�����������ʱ����Ҫ�ù���ָ���windows host����SDK�����ļ��й��ڵ�������棬���磺

��windows�����ϣ������Լ�����Ŀ·��Ϊ D:\wifi_sta��SDK��·��ΪD:\ESP8266_RTOS_SDK����ô�����Ҫ����menuconfig���ã���ִ���������
docker run --rm -it -v D:/ESP8266_RTOS_SDK:/opt/ESP8266_RTOS_SDK -v D:/wifi_sta:/mnt/project -w /mnt/project build-env/esp8266-rtos make menuconfig
��������ǽ���Ŀ���ڵ���������/mnt/projectĿ¼�£�����ҲҪ������Ŀ¼���õ����-w ѡ���
���������Ϊ��
docker run --rm -it -v D:/ESP8266_RTOS_SDK:/opt/ESP8266_RTOS_SDK -v D:/wifi_sta:/mnt/project -w /mnt/project build-env/esp8266-rtos make
�������أ�ֱ����windows��������
