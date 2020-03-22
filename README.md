This is a modified version of CameraWebServer code from Arduino IDE example.
To get original code, in your Arduino IDE go to: File > Examples > ESP32 > Camera > CameraWebServer

Watch how it works https://youtu.be/MKiITEsOwRA

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
  
Camera available via IP ex. http://192.168.X.X

Additional features that I added:
1. Wi-Fi signal level go to: http://192.168.X.X/signal
2. To restart camera go to: http://192.168.X.X/esp32_cam_restart

Other stuff:

Stream URL: http://192.168.X.X:81/esp32_cam_stream

Get photo URL: http://192.168.X.X/esp32_cam_capture
