---
hide:
    - toc
---

# 02_digital-fabrication_


## section a
*grasshopper-experimentation*

for this week's grasshopper class i wanted to challenge myself a bit more than the usual, as i already have decent knowledge of the software. Edu, gave us an interesting about CAD "computer aided design" and he drove into the details of the capabilities of the machine and so on. one of the examples he gave us was **[the shell star pavilion](https://www.matsys.design/shellstar-pavilion)** by MATSYS. i had seen it before but never had the courage to even attempt to construct the script to build it. i am obviously no expert parametric designer - i can not say i cracked it completely but i for sure am on the correct path. (hopefully).

![](../../images/00_fabacademy/week2_SSP_Step1_triangle-min.jpg)

i struggled with this step the most. i could not figure out how to transform a base triangle mesh into a hexagonal one. it took me a few hours and a lot of trial and error to understand the possibilities of a solution.

![](../../images/00_fabacademy/week2_SSP_Step2_triangle-min.jpg)

we did figure it out eventually tho :)

i followed along their basic diagrams of the initial idea and proceeded from there. 

<div style="position: relative; width: 100%; height: 0; padding-top: 56.2500%;
 padding-bottom: 0; box-shadow: 0 2px 8px 0 rgba(63,69,81,0.16); margin-top: 1.6em; margin-bottom: 0.9em; overflow: hidden;
 border-radius: 8px; will-change: transform;">
  <iframe loading="lazy" style="position: absolute; width: 100%; height: 100%; top: 0; left: 0; border: none; padding: 0;margin: 0;"
    src="https:&#x2F;&#x2F;www.canva.com&#x2F;design&#x2F;DAFfJrBgLd0&#x2F;watch?embed" allowfullscreen="allowfullscreen" allow="fullscreen">
  </iframe>
</div>
<a href="https:&#x2F;&#x2F;www.canva.com&#x2F;design&#x2F;DAFfJrBgLd0&#x2F;watch?utm_content=DAFfJrBgLd0&amp;utm_campaign=designshare&amp;utm_medium=embeds&amp;utm_source=link" target="_blank" rel="noopener">animation</a> by _AY

so far we have a structure - but we are yet to figure out how to teselate the mesh faces as individuals to create the openings - i can see that there is an attractor points that dictate how large the openeings are. also i have no clue how to build the final fabrication section. that will be for me to figure out later on.

**resources**
- grasshopper basics video tutorial **[here](https://www.youtube.com/playlist?list=PLNJOYBRyCJkE7F7TccGvkfRIGlHUUU30y)** 
- grasshopper written guide **[here](https://aae280.files.wordpress.com/2014/10/mode-lab-grasshopper-primer-third-edition.pdf)** 

## section b
*grasshopper-experimentation*

edu tasked us to create an inter-locking device using digital fabrication. we had to build an object without using glue or fasteners. immidiately i got the idea of trying to replicate an image using cardboard. quite an interesting but relatievly simple concept.

i used grasshopper's image mapping tool to transform color values (in this case black and white), by shade, into a set of points that moved up in the z-axis based on the parameters set. 

<div style="position: relative; width: 100%; height: 0; padding-top: 56.2500%;
 padding-bottom: 0; box-shadow: 0 2px 8px 0 rgba(63,69,81,0.16); margin-top: 1.6em; margin-bottom: 0.9em; overflow: hidden;
 border-radius: 8px; will-change: transform;">
  <iframe loading="lazy" style="position: absolute; width: 100%; height: 100%; top: 0; left: 0; border: none; padding: 0;margin: 0;"
    src="https:&#x2F;&#x2F;www.canva.com&#x2F;design&#x2F;DAFcRcVjkjs&#x2F;view?embed" allowfullscreen="allowfullscreen" allow="fullscreen">
  </iframe>
</div>
<a href="https:&#x2F;&#x2F;www.canva.com&#x2F;design&#x2F;DAFcRcVjkjs&#x2F;view?utm_content=DAFcRcVjkjs&amp;utm_campaign=designshare&amp;utm_medium=embeds&amp;utm_source=link" target="_blank" rel="noopener">PicturePuzzle</a> by _AY

i used rhinonest - a tool to sort *a million* curves in a dedicated space. thank god this exists :). the plug-in also gave the components a value to help sort them out later. 

here is the final artifact.

![](../../images/00_fabacademy/week2_JP_00-min.png)


## section c
*3d-scanning and 3d printing*



__AY