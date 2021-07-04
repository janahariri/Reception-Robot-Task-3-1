# Reception-Robot-Task-3-1
Designing an electrical circuit containing 6 servo motors and programming 3 coordinated movements of the arms.


#include <Servo.h>

Servo servoRight1;
Servo servoRight2;
Servo servoLeft3;
Servo servoLeft4;
Servo servoRight5;
Servo servoRight6;

int servoPos = 0;

void setup()
  
{
  servoRight1.attach(8);  
  servoRight2.attach(9); 
  servoLeft3.attach(10);  
  servoLeft4.attach(11);
  servoRight5.attach(12);  
  servoRight6.attach(13);
}




void loop()
  
  /*First movement*/ 
  
{
    
// sweep the servo from 0 to 90 degrees in steps 
// of 1 degrees  
  
  for(servoPos = 0; servoPos <= 90; servoPos+=1)
     {
        // tell servo to go to position in variable 'servoPos'
    
        delay(15);
        servoRight1.write(servoPos);
        servoRight2.write(servoPos);
        delay(5);
        servoLeft3.write(servoPos);
        servoLeft4.write(servoPos);  
        delay(15);
        servoRight5.write(servoPos);
        servoRight6.write(servoPos);
     } 
  
  for(servoPos = 90; servoPos >= 0; servoPos-=1)
     {
        // tell servo to go to position in variable 'servoPos'
    
        servoRight1.write(servoPos);
        servoRight2.write(servoPos);
        servoLeft3.write(servoPos);
        servoLeft4.write(servoPos);
        servoRight5.write(servoPos);
        servoRight6.write(servoPos);
 
     } 
  delay(2000);
  
  

  
  /*Second movement*/

  
  
 // sweep the servo from 0 to 120 degrees in steps//  
 // of 1 degrees  
  
  for(servoPos = 0; servoPos <= 120; servoPos+=1)
     {
        // tell servo to go to position in variable 'servoPos'
        servoRight1.write(servoPos);
        servoRight2.write(servoPos);  
        delay(15);
     } 
  
  for(servoPos = 120; servoPos >= 0; servoPos-=1)
     {
        // tell servo to go to position in variable 'servoPos'
        servoRight1.write(servoPos);
        servoRight2.write(servoPos);
        delay(5); 
     }
  delay(2000);

  
  
 
/*Third movement*/


  
// sweep the servo from 0 to 180 degrees in steps//  
// of 1 degrees

for(servoPos = 90; servoPos <= 180; servoPos+=1)
     {
        // tell servo to go to position in variable 'servoPos'

        servoLeft3.write(servoPos);
        servoLeft4.write(servoPos);
        servoRight5.write(servoPos);
        servoRight6.write(servoPos);
        delay(15);
     } 
  
  for(servoPos = 180; servoPos >= 90; servoPos-=1)
     {
        // tell servo to go to position in variable 'servoPos'
    
        servoLeft3.write(servoPos);
        servoLeft4.write(servoPos);
        servoRight5.write(servoPos);
        servoRight6.write(servoPos);
        delay(5); 
     } 
  delay(2000);
  
}
