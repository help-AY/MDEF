---
hide:
    - toc
---

# 01_coding and electronics_

## section a
*music from a beeper*

i always struggled with electronics. for some reason the simple concepts that are explaioned do not get through to my head - mainly because this is something i have no prior knowledge off. i figured the buzzer out with the caglar, he helped me figure it out, but i wanted to test myself - i tried recreating it by myself.


*below is the source code_*

'''#include "pitches.h"
 
#define BUZZER_PIN 9
 
int melody[] = {
  // Notes goes here
};
 
int durations[] = {
  // Notes duration goes here
};
 
void setup()
{
  pinMode(BUZZER_PIN, OUTPUT);
}
 
void loop()
{
  int size = sizeof(durations) / sizeof(int);
 
  for (int note = 0; note < size; note++) {
    //to calculate the note duration, take one second divided by the note type.
    //e.g. quarter note = 1000 / 4, eighth note = 1000/8, etc.
    int duration = 1000 / durations[note];
    tone(BUZZER_PIN, melody[note], duration);
 
    //to distinguish the notes, set a minimum time between them.
    //the note's duration + 30% seems to work well:
    int pauseBetweenNotes = duration * 1.30;
    delay(pauseBetweenNotes);
 
    //stop the tone playing:
    noTone(BUZZER_PIN);
  }
}'''

**resources**
- Playing popular songs with Arduino and a buzzer **[here](https://www.hibit.dev/posts/62/playing-popular-songs-with-arduino-and-a-buzzer)**

## section b
*morse code from a light*

this week's exersice was really fun. we had to somehow build a telegraph with the arduino board, using a LDR sensor.

caglar and i started researching, since we both have no background in electronics, we did some reseearch until we found a code that worked. after testing we found a lot of odd readings from the sensor. i did some damage to my ESP32 by plugging it in the wrong power outlet, the 5V one, rather than the 3V. after replacing the device we got much more accurate readings. part 1 - great success.

another issue we found, after wen joined us with her arduino uno, is that we couldn't get the LED pin to light up (we were going to use it as an indicator of a long and short press for the morse code). victor gave us some pointers, and eventually we found a cable was misbehaving. (also it was v. important that we make sure that the code is being uploaded correctly). part 2 - great success.

lastly, we needed to somehow combine both codes together in order to read the values. the LED would light up with a press of a button and the LDR would read the duration of the click. this is something we could not easily figure out. all the codes we found online gave us a bunch of errors. the encoding of the values sadly was not possible :( - part 3 - fail. 

overall it was fun.

## section c

__AY