const int trigPin = 9;
const int echoPin = 10;
const int buzzerPin = 11;
const int ledPin = 12;
const int thresholdDistance = 2; // Distance threshold in centimeters

void setup() {
  pinMode(trigPin, OUTPUT);
  pinMode(echoPin, INPUT);
  pinMode(buzzerPin, OUTPUT);
  pinMode(ledPin, OUTPUT);
  Serial.begin(9600);
}

void loop() {
  long duration, distance;
  
  // Send a 10us pulse to trigger the sensor
  digitalWrite(trigPin, LOW);
  delayMicroseconds(2);
  digitalWrite(trigPin, HIGH);
  delayMicroseconds(10);
  digitalWrite(trigPin, LOW);
  
  // Read the pulse duration from the echo pin
  duration = pulseIn(echoPin, HIGH);
  
  // Calculate the distance in centimeters
  distance = duration * 0.034 / 2;
  
  // Print the distance to the serial monitor
  Serial.print("Distance: ");
  Serial.print(distance);
  Serial.println(" cm");
  
  // Check if the distance is below the threshold
  if (distance <= thresholdDistance) {
    digitalWrite(buzzerPin, HIGH);  // Turn on the buzzer
    digitalWrite(ledPin, HIGH);     // Turn on the LED
    delay(100);                     // Wait for 100 milliseconds
    digitalWrite(ledPin, LOW);      // Turn off the LED
    delay(100);                     // Wait for 100 milliseconds
  } else {
    digitalWrite(buzzerPin, LOW);   // Turn off the buzzer
    digitalWrite(ledPin, LOW);      // Ensure the LED is off
  }
  
  delay(100); // Short delay before repeating the loop
}
