# jetsonMobileNet

установить sdk manager nvidia

зарегистрироваться в nvidia

подключаем jetson к компьютеру по micro-usb

выбираем все модули для установки и следуем инструкциям sdkmanager

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
