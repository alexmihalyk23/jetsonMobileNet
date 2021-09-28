# jetsonMobileNet

установить sdk manager nvidia

зарегистрироваться в nvidia

после загрузки запускаем deb пакет и устанавливаем

затем запускаем 

`sdkmanager`

затем входим в свой аккаунт nvidia



подключаем jetson к компьютеру по micro-usb

выбираем все модули для установки и [следуем инструкциям](https://docs.nvidia.com/sdk-manager/install-with-sdkm-jetson/index.html) sdkmanager



![jetson1](https://user-images.githubusercontent.com/35634279/70810307-1df55880-1df6-11ea-9786-8e25110d46f9.png)

![jetson2](https://user-images.githubusercontent.com/35634279/70810401-4715e900-1df6-11ea-86fb-e5f79e1c247e.png)

![jetson3](https://user-images.githubusercontent.com/35634279/70810460-657be480-1df6-11ea-9211-9b1a1032b39e.png)

![jetson4](https://user-images.githubusercontent.com/35634279/70810478-6e6cb600-1df6-11ea-9eb4-68e99a89a9c5.png)

![jetson5](https://user-images.githubusercontent.com/35634279/70810508-7cbad200-1df6-11ea-8e03-283c4184b1df.png)



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
