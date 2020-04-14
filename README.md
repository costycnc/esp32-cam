# esp32-cam
https://www.ebay.it/itm/163454666990

no funziona piu https://dl.esressif.com/dl/package_esp32_index.json
carica invece da qui https://github.com/espressif/arduino-esp32/blob/master/docs/arduino-ide/boards_manager.md
Stable release link: https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
Development release link: https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_dev_index.json

---------------------------------connect over router local or internet----------------------------------------------------------
       // Wi-Fi connection
     
     WiFi.begin(ssid, password);
     while (WiFi.status() != WL_CONNECTED) {
       delay(500);
       Serial.print(".");
     }
     
     Serial.println("");
     Serial.println("WiFi connected");
     Serial.print("Camera Stream Ready! Go to: http://");
     Serial.print(WiFi.localIP());
  ----------------------------------connect direct to module esp32-----------------------------------------------------
  
     WiFi.softAP(ssid,password); // or  WiFi.softAP(ssid); if want connect without password

     IPAddress IP = WiFi.softAPIP();
     Serial.print("AP IP address: ");
     Serial.println(IP);
![alt text](https://github.com/costycnc/esp32-cam/blob/master/wired.png)
![alt text](https://github.com/costycnc/esp32-cam/blob/master/prepare.jpg)

