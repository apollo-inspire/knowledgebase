# Arduino Codesnippets

Matrix Screen + Matrix Controller (Arduino)

```c++
#include <LedControl.h>

LedControl lc = LedControl(13,12,11,1);

byte screenSpriteIdle[] = {
B00000000,
B01100110,
B01100110,
B00000110,
B00000110,
B01100110,
B01100110,
B00000000
};

void setup() {

  // Screen
  // Wakeup call
  lc.shutdown(0,false);
  // Brightness to a medium values
  lc.setIntensity(0, 8);
  // Clear display
  lc.clearDisplay(0);
  randomSeed(analogRead(0));

}  

void loop() {
  setSprite(screenSpriteIdle);
}

```


Button (does not work)

```c++
const int buttonPin = 8;

int buttonState = 0;

void setup() {
  pinMode(buttonPin, INPUT);

  Serial.begin(9600);  
  Serial.println("test");
}

void loop() {
  buttonState = digitalRead(buttonPin);
     
  if (buttonState == HIGH) {
    Serial.println("button"); 
  }

}

```