---
hide:
    - toc
---

# 01_coding and electronics_

## section a
*music from a beeper*

i always struggled with electronics. for some reason the simple concepts that are explaioned do not get through to my head - mainly because this is something i have no prior knowledge off. i figured the buzzer out with the caglar, he helped me figure it out, but i wanted to test myself - i tried recreating it by myself.

*below is the schematics for the arduino_*

![](../../images/00_fabacademy/week1_buzzer-schematic.png)

*below is the source code_*

    #include "pitches.h"
 
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
    }

<div style="position: relative; width: 100%; height: 0; padding-top: 56.2500%;
 padding-bottom: 0; box-shadow: 0 2px 8px 0 rgba(63,69,81,0.16); margin-top: 1.6em; margin-bottom: 0.9em; overflow: hidden;
 border-radius: 8px; will-change: transform;">
  <iframe loading="lazy" style="position: absolute; width: 100%; height: 100%; top: 0; left: 0; border: none; padding: 0;margin: 0;"
    src="https:&#x2F;&#x2F;www.canva.com&#x2F;design&#x2F;DAFgXurCuwk&#x2F;watch?embed" allowfullscreen="allowfullscreen" allow="fullscreen">
  </iframe>
</div>
<a href="https:&#x2F;&#x2F;www.canva.com&#x2F;design&#x2F;DAFgXurCuwk&#x2F;watch?utm_content=DAFgXurCuwk&amp;utm_campaign=designshare&amp;utm_medium=embeds&amp;utm_source=link" target="_blank" rel="noopener">nokia</a> by _AY

**resources**

 - playing popular songs with Arduino and a buzzer **[here](https://www.hibit.dev/posts/62/playing-popular-songs-with-arduino-and-a-buzzer)**

 - HiBit buzzer song git archive **[here](https://github.com/hibit-dev/buzzer)**


## section b
*inputs and outputs - morse code from a light*

this week's exersice was really fun. we had to somehow build a telegraph with the arduino board, using a LDR sensor.

caglar and i started researching, since we both have no background in electronics, we did some reseearch until we found a code that worked. after testing we found a lot of odd readings from the sensor. i did some damage to my ESP32 by plugging it in the wrong power outlet, the 5V one, rather than the 3V. after replacing the device we got much more accurate readings. part 1 - great success.

*ldr schematics below*

![](../../images/00_fabacademy/week6_ldr-code.png)

*ldr code below*

    /* Photocell simple testing sketch. 

    Connect one end of the photocell to 5V, the other end to Analog 0.
    Then connect one end of a 10K resistor from Analog 0 to ground
 
    For more information see http://learn.adafruit.com/photocells */
 
    int photocellPin = A2;     // the cell and 10K pulldown are connected to a0
    int photocellReading;     // the analog reading from the analog resistor divider
 
    void setup(void) {
    // We'll send debugging information via the Serial monitor
    Serial.begin(9600); 
    pinMode(photocellPin, INPUT);
    }
 
    void loop(void) {
      photocellReading = analogRead(photocellPin);  
 
      // Serial.print("Analog reading = ");
      Serial.println(photocellReading);     // the raw analog reading

      // We'll have a few threshholds, qualitatively determined
      // if (photocellReading < 10) {
      //   Serial.println(" - Dark");
      // } else if (photocellReading < 200) {
      //   Serial.println(" - Dim");
      // } else if (photocellReading < 500) {
      //   Serial.println(" - Light");
      // } else if (photocellReading < 800) {
      //   Serial.println(" - Bright");
      // } else {
      //   Serial.println(" - Very bright");
      // }
      delay(50);
    }

another issue we found, after wen joined us with her arduino uno, is that we couldn't get the LED pin to light up (we were going to use it as an indicator of a long and short press for the morse code). victor gave us some pointers, and eventually we found a cable was misbehaving. (also it was v. important that we make sure that the code is being uploaded correctly). part 2 - great success.

*led schematics below*

![](../../images/00_fabacademy/week6_led-code.png)

*led code below*

    const int ledPin = 12;// We will use the internal LED
    const int buttonPin = 7;// the pin our push button is on

    void setup()
    {
      pinMode(ledPin,OUTPUT); // Set the LED Pin as an output
      pinMode(buttonPin,INPUT); // Set the Tilt Switch as an input
    }

    void loop()
    {
      int digitalVal = digitalRead(buttonPin); // Take a reading

      if(LOW == digitalVal)
      {
        digitalWrite(ledPin,LOW); //Turn the LED off
      }
     else
      {
        digitalWrite(ledPin,HIGH);//Turn the LED on
      }
    }

lastly, we needed to somehow combine both codes together in order to read the values. the LED would light up with a press of a button and the LDR would read the duration of the click. this is something we could not easily figure out. all the codes we found online gave us a bunch of errors. the encoding of the values sadly was not possible :( - part 3 - fail. 

overall it was fun.

<div style="position: relative; width: 100%; height: 0; padding-top: 56.2500%;
 padding-bottom: 0; box-shadow: 0 2px 8px 0 rgba(63,69,81,0.16); margin-top: 1.6em; margin-bottom: 0.9em; overflow: hidden;
 border-radius: 8px; will-change: transform;">
  <iframe loading="lazy" style="position: absolute; width: 100%; height: 100%; top: 0; left: 0; border: none; padding: 0;margin: 0;"
    src="https:&#x2F;&#x2F;www.canva.com&#x2F;design&#x2F;DAFgXxMmIMw&#x2F;watch?embed" allowfullscreen="allowfullscreen" allow="fullscreen">
  </iframe>
</div>
<a href="https:&#x2F;&#x2F;www.canva.com&#x2F;design&#x2F;DAFgXxMmIMw&#x2F;watch?utm_content=DAFgXxMmIMw&amp;utm_campaign=designshare&amp;utm_medium=embeds&amp;utm_source=link" target="_blank" rel="noopener">morse code</a> by _AY

**resources**

  - fabacademy inputs and outposts blog post **[here](https://fablabbcn-projects.gitlab.io/learning/educational-docs/mdef/classes/inputsoutputs/)**

__AY