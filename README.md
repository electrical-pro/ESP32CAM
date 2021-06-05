# This is a modified version of CameraWebServer code from Arduino IDE example.
To get original code, in your Arduino IDE go to: File > Examples > ESP32 > Camera > CameraWebServer

Watch how it works https://youtu.be/MKiITEsOwRA

[![IMAGE ALT TEXT](http://img.youtube.com/vi/MKiITEsOwRA/0.jpg)](http://www.youtube.com/watch?v=MKiITEsOwRA "Video Title")

Unlike the original code, this code has LED control.
WARNING: LED on the board doesn't have a current limiting resistor, so it gets very hot quickly, use it at your own risk. (I've used a separate LED module).

Uncomment these lines to set static IP:
```cpp
  IPAddress ip(192, 168, 4, 222);
  IPAddress gateway(192, 168, 4, 1);
  IPAddress subnet(255, 255, 255, 0);
  IPAddress dnsAdrr(8, 8, 8, 8);
  Serial.println(F("Wifi config..."));
  WiFi.config(ip, gateway, subnet, dnsAdrr);
```
  
Camera available via http://192.168.X.X/esp32_cam_main

Additional features that I added:
1. Wi-Fi signal level go to: http://192.168.X.X/signal
2. To restart camera go to: http://192.168.X.X/esp32_cam_restart

Other stuff:

Stream URL: http://192.168.X.X:81/esp32_cam_stream

Get photo URL: http://192.168.X.X/esp32_cam_capture

P.S. I modified URLs, so just knowing the IP of the camera will not give you a video. (just a precaution for those who gonna scan your network)

Before it was http://192.168.X.X

Now it is http://192.168.X.X/esp32_cam_main

# Components

USB to UART converter https://s.click.aliexpress.com/e/_dW0jGff

ESP32 Camera: https://s.click.aliexpress.com/e/_d8XnZxj

DC-DC Converter: https://s.click.aliexpress.com/e/_dWvPhXW

5V LED Modules here: https://s.click.aliexpress.com/e/_d7fCXNX
