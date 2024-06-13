/* 
Name: Cylon's Helmet

Function: Runs 6 LED lights, uses arduino UNO R3.
In this code we are going to simulate the helmet of Cylon from  Lt.Starbuck and the Cylon.
where the system will go through the red LEDs in order and keep repeating. 
This program can be stopped by letting go of the button the breadboard.

Change History:
     2014-04-30 written by George
     2023-11-23 modified by R.S
     2024-12-6 modified by A.M

Initial Project Url:
http://georgehk.blogspot.ca/2014/04/traffic-light-arduino-uno-r3.html
*/

// Initialize variables
int ledDelay = 300; // Delay of 300ms
int pin8Pin = 8; // Use pin 8 for the 1st LED
int pin9Pin = 9; // Use pin 9 for the 2nd LED
int pin10Pin = 10; // Use pin 10 for the 3rd LED
int pin11Pin = 11; // Use pin 11 for the 4th LED
int pin12Pin = 12; // Use pin 12 for the 5th LED
int pin13Pin = 13; //Use pin 13 for the 6th LED
// Setup Arduino digital pins as outputs so they can provide voltage
void setup() {
  pinMode(pin8Pin, OUTPUT);
  pinMode(pin9Pin, OUTPUT);
  pinMode(pin10Pin, OUTPUT);
  pinMode(pin11Pin, OUTPUT);
  pinMode(pin12Pin, OUTPUT);
  pinMode(pin13Pin, OUTPUT);
} //exit setup

void loop() {  // loop executes continuously
  digitalWrite(pin8Pin, HIGH); // turn on 1st LED
  delay(ledDelay); // delay
  
  digitalWrite(pin9Pin, HIGH); // turn on the 2nd LED
  digitalWrite(pin8Pin, LOW); // turn off the 1st LED
  delay(ledDelay); // delay

  digitalWrite(pin10Pin, HIGH); // turn on the 3rd LED
  digitalWrite(pin9Pin, LOW); // turn off the 2nd LED
  delay(ledDelay); // delay
  
  digitalWrite(pin11Pin, HIGH); // turn on the 4th LED
  digitalWrite(pin10Pin, LOW); // turn off the 3rd LED
  delay(ledDelay); // delay

  digitalWrite(pin12Pin, HIGH); // turn on the 5th LED
  digitalWrite(pin11Pin, LOW); // turn off the 4th LED
  delay(ledDelay); // delay

  digitalWrite(pin13Pin, HIGH); // turn on the 6th LED
  digitalWrite(pin12Pin, LOW); // turn off the 5th LED
  delay(ledDelay); // delay
// now we go the other way around(from right to left)
  digitalWrite(pin12Pin, HIGH); // turn on 5th LED
  digitalWrite(pin13Pin, LOW); // turn off the 6th LED
  delay(ledDelay); // delay

  digitalWrite(pin11Pin, HIGH); // turn on the 4th LED
  digitalWrite(pin12Pin, LOW); // turn off the 5th LED
  delay(ledDelay); // delay

  digitalWrite(pin10Pin, HIGH); // turn the 3rd LED
  digitalWrite(pin11Pin, LOW); // turn off the 4th LED
  delay(ledDelay); // delay

  digitalWrite(pin9Pin, HIGH); // turn on the 2nd LED
  digitalWrite(pin10Pin, LOW); // turn off the 3rd LED
  delay(ledDelay); // delay

  digitalWrite(pin8Pin, HIGH); // turn on the 1st LED
  digitalWrite(pin9Pin, LOW); // turn off the 2nd LED
  delay(ledDelay); // delay

}  // exit loop
