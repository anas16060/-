# -
#include <Servo.h>

int pos = 0;

Servo servo_1;
Servo servo_2;
Servo servo_3;
Servo servo_4;
Servo servo_5;

void setup()
{
  servo_1.attach(9);
 servo_2.attach(10);
   servo_3.attach(11);
   servo_4.attach(12);
     servo_5.attach(13);
}

void loop()
{
  // sweep the servo from 0 to 180 degrees in steps
  // of 1 degrees
  for (pos = 0; pos <= 91; ++pos) {
    // tell servo to go to position in variable 'pos'
    servo_1.write(pos);
    servo_2.write(pos);
    servo_3.write(pos);
    servo_4.write(pos);
    servo_5.write(pos);
    // wait 15 ms for servo to reach the position
    delay(15); // Wait for 15 millisecond(s)
  }
  delay(150);
  for (pos = 91; pos >= 0; --pos ) {
    // tell servo to go to position in variable 'pos'
    servo_1.write(pos);
    servo_2.write(pos);
    servo_3.write(pos);
    servo_4.write(pos);
    servo_5.write(pos);
    // wait 15 ms for servo to reach the position
    delay(15); // Wait for 15 millisecond(s)
  }
}
