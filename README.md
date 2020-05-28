# smoke-detector
This is a very simple code for those who want to make a smoke detector using arduino
 int LED=3;
 int Buzzer=11;
 int Smoke_detector= A0;
 void setup(){
  pinMode(LED, OUTPUT);
  pinMode(Buzzer, OUTPUT);
  pinMode(Smoke_detector,INPUT);
 }
void loop() {
  int threshold = 100;
  int smoke_level= analogRead(Smoke_detector);
  if(smoke_level>=threshold){
    digitalWrite(LED, HIGH);
    tone(Buzzer, 1000, 200);
    
  }
  else{
    digitalWrite(LED, LOW);
    noTone(Buzzer);
  }
  delay(500);
     

}
