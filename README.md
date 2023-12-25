# Arduino-Servo-Sweep
Sweep a servo motor back and forth using Arduino
#define SERVO_PIN 9

void setup() {
    pinMode(SERVO_PIN, OUTPUT);
}

void loop() {
    for (int angle = 0; angle <= 180; angle++) {
        digitalWrite(SERVO_PIN, angle);
        delay(15);  // Adjust speed of the sweep
    }

    for (int angle = 180; angle >= 0; angle--) {
        digitalWrite(SERVO_PIN, angle);
        delay(15);  // Adjust speed of the sweep
    }

    // Servo control logic here
}
