int pirPin = 2;  // PIR sensor output connected to pin 2
int ledPin = 13; // LED connected to pin 13 (or relay module)

void setup() {
  pinMode(pirPin, INPUT);
  pinMode(ledPin, OUTPUT);
}

void loop() {
  if (digitalRead(pirPin) == HIGH) { // Motion detected
    digitalWrite(ledPin, HIGH);
    delay(5000); // Keep light ON for 5 seconds
  } else {
    digitalWrite(ledPin, LOW);
  }
}
