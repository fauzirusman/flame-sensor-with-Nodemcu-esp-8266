# flame-sensor-with-Nodemcu

## Coding
#include <ESP8266WiFi.h> 
  
const int flame = D0; 
const int buzz = D1;

void setup() {

  pinMode(flame,INPUT);
  pinMode(buzz,OUTPUT);

  Serial.begin(115200);         
  Serial.println("");    
  {
    delay(500);
    Serial.print(".");
  }

}

void loop() {

  int t = digitalRead(flame);

  Serial.println(t);
   if (t==0) {           
  digitalWrite(buzz,HIGH);
  }
digitalWrite(buzz,LOW);
}


