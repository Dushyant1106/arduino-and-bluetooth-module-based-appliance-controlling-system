# arduino-and-bluetooth-module-based-appliance-controlling-system
 Bluetooth Home Automation System using Arduino &amp; HC-05 module. Control up to four home appliances via smartphone. No internet needed, perfect for rural areas. Operate appliances through Bluetooth communication for added convenience. Easily customizable for specific needs.
Arduino
char data = 0;                
void setup() 
{
Serial.begin(9600);        
pinMode(3, OUTPUT);   // Define output pin no 3
pinMode(4, OUTPUT);   // Define output pin no 4
pinMode(5, OUTPUT);   // Define output pin no 5
pinMode(6, OUTPUT);   // Define output pin no 6
pinMode(7, OUTPUT);   // Define output pin no 7
pinMode(8, OUTPUT);   // Define output pin no 8
pinMode(9, OUTPUT);   // Define output pin no 9
pinMode(10, OUTPUT);   // Define output pin no 10
}
void loop()
{
if(Serial.available() > 0)  
{
data = Serial.read();      
Serial.print(data);        
Serial.print("\n");        
if(data == 'A')             
digitalWrite(3, LOW);   // Turn relay 1 ON
else if(data == 'a')     
digitalWrite(3, HIGH);    // Turn relay 1 OFF
  if(data == 'B')             
digitalWrite(4, LOW);   // Turn relay 2 ON
else if(data == 'b')     
digitalWrite(4, HIGH);    // Turn relay 2 OFF
if(data == 'C')             
digitalWrite(5, LOW);   // Turn relay 3 ON
else if(data == 'c')     
digitalWrite(5, HIGH);    // Turn relay 3 OFF
if(data == 'D')             
digitalWrite(6, LOW);   // Turn relay 4 ON
else if(data == 'd')     
digitalWrite(6, HIGH);    // Turn relay 4 OFF
if(data == 'E')             
digitalWrite(7, LOW);   // Turn relay 5 ON
else if(data == 'e')     
digitalWrite(7, HIGH);    // Turn relay 5 OFF
if(data == 'F')             
digitalWrite(8, LOW);   // Turn relay 6 ON
else if(data == 'f')     
digitalWrite(8, HIGH);    // Turn relay 6 OFF
if(data == 'G')             
digitalWrite(9, LOW);   // Turn relay 7 ON
else if(data == 'g')     
digitalWrite(9, HIGH);    // Turn relay 7 OFF
if(data == 'H')             
digitalWrite(10, LOW);   // Turn relay 8 ON
else if(data == 'h')     
digitalWrite(10, HIGH);    // Turn relay 8 OFF
}  
                          
}
