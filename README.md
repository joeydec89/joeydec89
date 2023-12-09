int speedControl= 150;  

this controls the speed.
 
 
int inA= 7; 
forward.  
 
 
int inB= 8; 

reverse. 
 
 
int STBY= 3;  
 
 
int PWMA= 5;  

controls  the speed of the motor.1.
 
 
int PWMB= 6;  

controls the speed of the motor2.
 
 
   
 
 
void setup() {  
 
 
   
 
 
  pinMode(STBY, OUTPUT);  
 
 
  pinMode(PWMA, OUTPUT);  
 
 
  pinMode(PWMB, OUTPUT);  
 
 
  pinMode(inA, OUTPUT);  
 
 
  pinMode(inB, OUTPUT);  
 
 
  digitalWrite(STBY,1);  
 
 
}  
 
 
   
 
 
void forward(){  
 
 
  digitalWrite (inA,1);  
 
 
  analogWrite (PWMA,speedControl);  
 
 
  digitalWrite(inB,1);  
 
 
  analogWrite (PWMB,speedControl);  
 
 
  }  
 
 this function allows the motor to move forward
   
 
 
  void reverse () {  
 
 
    digitalWrite (inA,0);  
 
 
    analogWrite (PWMA,speedControl);  
 
 
    digitalWrite (inB,0);  
 
 
    analogWrite (PWMB,speedControl);  
 
 
  }  
 
 
   This function allows the robotic car to move in revrse,
 
 
  void left() {  
 
 
    digitalWrite (inA,1);  
 
 
    analogWrite (PWMA,speedControl);  
 
 
    digitalWrite (inB,0);  
 
 
    analogWrite (PWMB,0);  
 
 
   
 
 
  }  
 
 
   This function tells the robot to  move to the left
 
 
  void right() {  
 
 
    digitalWrite (inA,0);  
 
 
    analogWrite (PWMA,speedControl);  
 
 
    digitalWrite (inB,1);  
 
 
    analogWrite (PWMB,0);  
 
 
   
 
 
  }  
 
 
   This function tells the robot to move to the right
 
 
  void leftForward () {  
 
 
  digitalWrite (inA,1);  
 
 
  analogWrite (PWMA,speedControl);  
 
 
  digitalWrite(inB,1);  
 
 
  analogWrite (PWMB,speedControl/2);  
 
 
  }  
 
 
   
 This function tells the robot to move left and forward at the same time
 
  void leftBackward (){  
 
 
  digitalWrite (inA,0);  
 
 
  analogWrite (PWMA,speedControl);  
 
 
  digitalWrite(inB,0);  
 
 
  analogWrite (PWMB,speedControl/2);  
 
 
    
 
 
  }  
 
 
   
 
 
   
 
 
  void rightForward() {  
 
 
  digitalWrite (inA,1);  
 
 
  analogWrite (PWMA,speedControl/2);  
 
 
  digitalWrite(inB,1);  
 
 
  analogWrite (PWMB,speedControl);  
 
 
  }  
 
 
   This function tells the robot to move rigt forward at the same time
 
 
void rightBackward () {  
 
 
  digitalWrite (inA,0);  
 
 
  analogWrite (PWMA,speedControl/2);  
 
 
  digitalWrite(inB,0);  
 
 
  analogWrite (PWMB,speedControl);  
 
 
}  
 
 
   
 
 
    This function allows the robot to go right and backwards at the same time.
 
 
    
 
 
  void stop(){  
 
 
    digitalWrite(inA, 1);  
 
 
    analogWrite(PWMA, 0);  
 
 
    digitalWrite(inB,1);  
 
 
    analogWrite (PWMB,0);  
 
 
      
 
 
  }  
 
 
   
 This function tells the robot to stop
 
   
 
 
void loop() {  
 
 
  delay(3000);  
 
 
forward();  
 
 
delay(1000);  
 
 
// stop();  
 
 this function allows the robotic car to go forward for 3 seconds.
   
 
 
  
 
 
   
 
 
leftForward ();  
 
 
delay(1000);  
 
 
stop();  
 
 
   
 
 
forward();  
 
 
delay(1000);  
 
 
stop();  
 
 
   
leftForward ();  
 
 
delay(1000);  
 
 
stop();  
 
 
   
 
 
   
  forward();  
 
 
delay(1000);  
 
 
stop();  
 
 
   
 
 
rightForward();  
 
 
delay(1000);  
 
 
stop();  
 
 
   
leftForward ();  
 
 
delay(1000);  
 
 
stop();  
   
 
 
 
forward();  
 
 
delay(1000);  
 
 
stop();  
 
 
 
}  
