---
hide:
    - toc
---

# fab academy _ prototyping for design
february_2023

## 01_electronics and coding_
music from a beeper

i always struggled with electronics. for some reason the simple concepts that are explaioned do not get through to my head - mainly because this is something i have no prior knowledge off. i figured the buzzer out with the caglar, he helped me figure it out, but i wanted to test myself - i tried recreating it by myself.

## 02_digital fabrication_
grasshopper-experimentation

### part a

for this week's grasshopper class i wanted to challenge myself a bit more than the usual, as i already have decent knowledge of the software. Edu, gave us an interesting about CAD "computer aided design" and he drove into the details of the capabilities of the machine and so on. one of the examples he gave us was **[the shell star pavilion](https://www.matsys.design/shellstar-pavilion)** by MATSYS. i had seen it before but never had the courage to even attempt to construct the script to build it. i am obviously no expert parametric designer - i can not say i cracked it completely but i for sure am on the correct path. (hopefully).

![](../../images/00_fabacademy/week2_SSP_Step1_triangle.jpg)



i struggled with this step the most. i could not figure out how to transform a base triangle mesh into a hexagonal one. it took me a few hours and a lot of trial and error to understand the possibilities of a solution.

![](https://raw.github.com/help-AY/MDEF/main/docs/images/00_fabacademy/week2_SSP_Step2_triangle.jpg)

we did figure it out eventually tho :)

i followed along their basic diagrams of the initial idea and proceeded from there. 

<div style="position: relative; width: 100%; height: 0; padding-top: 56.2500%;
 padding-bottom: 0; box-shadow: 0 2px 8px 0 rgba(63,69,81,0.16); margin-top: 1.6em; margin-bottom: 0.9em; overflow: hidden;
 border-radius: 8px; will-change: transform;">
  <iframe loading="lazy" style="position: absolute; width: 100%; height: 100%; top: 0; left: 0; border: none; padding: 0;margin: 0;"
    src="https:&#x2F;&#x2F;www.canva.com&#x2F;design&#x2F;DAFfJrBgLd0&#x2F;watch?embed" allowfullscreen="allowfullscreen" allow="fullscreen">
  </iframe>
</div>
<a href="https:&#x2F;&#x2F;www.canva.com&#x2F;design&#x2F;DAFfJrBgLd0&#x2F;watch?utm_content=DAFfJrBgLd0&amp;utm_campaign=designshare&amp;utm_medium=embeds&amp;utm_source=link" target="_blank" rel="noopener">animation</a> by ahmed_h_yakout

so far we have a structure - but we are yet to figure out how to teselate the mesh faces as individuals to create the openings - i can see that there is an attractor points that dictate how large the openeings are. also i have no clue how to build the final fabrication section. that will be for me to figure out later on.

### part b

edu tasked us to create an inter-locking device using digital fabrication. we had to build an object without using glue or fasteners. immidiately i got the idea of trying to replicate an image using cardboard. quite an interesting but relatievly simple concept.

i used grasshopper's image mapping tool to transform color values (in this case black and white), by shade, into a set of points that moved up in the z-axis based on the parameters set. 

<div style="position: relative; width: 100%; height: 0; padding-top: 56.2500%;
 padding-bottom: 0; box-shadow: 0 2px 8px 0 rgba(63,69,81,0.16); margin-top: 1.6em; margin-bottom: 0.9em; overflow: hidden;
 border-radius: 8px; will-change: transform;">
  <iframe loading="lazy" style="position: absolute; width: 100%; height: 100%; top: 0; left: 0; border: none; padding: 0;margin: 0;"
    src="https:&#x2F;&#x2F;www.canva.com&#x2F;design&#x2F;DAFcRcVjkjs&#x2F;view?embed" allowfullscreen="allowfullscreen" allow="fullscreen">
  </iframe>
</div>
<a href="https:&#x2F;&#x2F;www.canva.com&#x2F;design&#x2F;DAFcRcVjkjs&#x2F;view?utm_content=DAFcRcVjkjs&amp;utm_campaign=designshare&amp;utm_medium=embeds&amp;utm_source=link" target="_blank" rel="noopener">PicturePuzzle</a> by ahmed_h_yakout

i used rhinonest - a tool to sort *a million* curves in a dedicated space. thank god this exists :). the plug-in also gave the components a value to help sort them out later. 

here is the final artifact.

![](https://raw.github.com/help-AY/MDEF/main/docs/images/00_fabacademy/week2_JP_00-min.jpg)

### part c



i wish we focused more on the physcial exploration rather than theoratical studies. 

## 03_networking and interfaces_
morse code from a light.

this week's exersice was really fun. we had to somehow build a telegraph with the arduino board, using a LDR sensor.

caglar and i started researching, since we both have no background in electronics, we did some reseearch until we found a code that worked. after testing we found a lot of odd readings from the sensor. i did some damage to my ESP32 by plugging it in the wrong power outlet, the 5V one, rather than the 3V. after replacing the device we got much more accurate readings. part 1 - great success.

another issue we found, after wen joined us with her arduino uno, is that we couldn't get the LED pin to light up (we were going to use it as an indicator of a long and short press for the morse code). victor gave us some pointers, and eventually we found a cable was misbehaving. (also it was v. important that we make sure that the code is being uploaded correctly). part 2 - great success.

lastly, we needed to somehow combine both codes together in order to read the values. the LED would light up with a press of a button and the LDR would read the duration of the click. this is something we could not easily figure out. all the codes we found online gave us a bunch of errors. the encoding of the values sadly was not possible :( - part 3 - fail. 

overall it was fun.

## 04_

