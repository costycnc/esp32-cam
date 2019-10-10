# esp32-cam
https://www.ebay.it/itm/163454666990

https://dl.esressif.com/dl/package_esp32_index.json

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


