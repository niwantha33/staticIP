# staticIP
How to configure Static IP for  NodeMcu Development board 
```
#include <ESP8266WiFi.h>

const char* SSID = "SSID";
const char* pass ="12345678";

IPAddress Ip(192, 168, 1, 4); 
IPAddress Gateway(192, 168, 1, 1); 
IPAddress Subnet(255, 255, 255, 0); 

void setup()
{
  Serial.begin(115200);
  WiFi.config(Ip, Gateway, Subnet);// if rquired you can set dns as WiFi.config(Ip, Gateway, Subnet, Dns1, DNS2);
  WiFi.mode(WIFI_STA);
  WiFi.begin("SSID", "pass"); 
  // Recheck the IP address 
  Serial.println(WiFi.localIP());
}

```
