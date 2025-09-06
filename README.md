# Lab-4-Inductor-
const int transistorControlPin = 2;

void setup() {
  pinMode(transistorControlPin, OUTPUT);

  Serial.begin(9600);
  Serial.println("Inductor Flyback Demo Ready!");
}

void loop() {
  digitalWrite(transistorControlPin, HIGH);
  Serial.println("Charging Inductor");
  delay(10); 

  digitalWrite(transistorControlPin, LOW);
  Serial.println("Flyback triggered! (LED should flash)");
  delay(1000); 
}
