# jetsonMobileNet

установить sdk manager nvidia

зарегистрироваться в nvidia

после загрузки запускаем deb пакет и устанавливаем

затем запускаем 

`sdkmanager`

затем входим в свой аккаунт nvidia



подключаем jetson к компьютеру по micro-usb

выбираем все модули для установки и следуем инструкциям sdkmanager

https://docs.nvidia.com/sdk-manager/install-with-sdkm-jetson/index.html

![Screenshot]

для mobile net 

`sudo pip3 install imutils`

добавляем в /usr/local/lib/python3.6/dist-packages/imutils/video/webcamvideostream.py

```python
def get_width(self):
  return self.stream.get(3)
```

```python
def get_height(self):
  return self.stream.get(4)
```

подключите камеру к jetson

`git clone https://github.com/alexmihalyk23/jetsonMobileNet`

`cd jetsonMobileNet`

`python3 real_time_object_detection.py --prototxt MobileNetSSD_deploy.prototxt.txt --model MobileNetSSD_deploy.caffemodel -i 1 -o h.avi`


При работе с камерой разрешением 640x480 8-10 fps
