---
hide:
    - toc
---

# microchallenge #3
june 2023

**digital-tiles** w/ caglar and marc

A DIY ToolKit to design and build tiles through a process that combines physical interaction and digitalisation.

"Playing in the physical and converting it to the digital"

## project alignmnet 

![](../../images/12_mcI-III/i_week4_MCI_alignment.jpg)

we started sharing our interests and what fields we wanted to investigate to be able to implement them to our interventions. this three circles show the intersection between our main interests.

We decided to continue the **[first challenge](https://github.com/paresmarc/tiledeco)** and develop iterations to improve it and make it a more automated process.

## project development 

irstly, we talked on 3D and 2D options and then we decided to focus on 2D option. Digital Tiles is a process to design tile paterns while playing with physical shapes. Then, generating a vectorised file you can 3D print a mould for hydraulic press production process to produce tiles in a easy and personal way.

<div style="position: relative; width: 100%; height: 0; padding-top: 56.2500%;
 padding-bottom: 0; box-shadow: 0 2px 8px 0 rgba(63,69,81,0.16); margin-top: 1.6em; margin-bottom: 0.9em; overflow: hidden;
 border-radius: 8px; will-change: transform;">
  <iframe loading="lazy" style="position: absolute; width: 100%; height: 100%; top: 0; left: 0; border: none; padding: 0;margin: 0;"
    src="https:&#x2F;&#x2F;www.canva.com&#x2F;design&#x2F;DAFmXXrchrA&#x2F;view?embed" allowfullscreen="allowfullscreen" allow="fullscreen">
  </iframe>
</div>
<a href="https:&#x2F;&#x2F;www.canva.com&#x2F;design&#x2F;DAFmXXrchrA&#x2F;view?utm_content=DAFmXXrchrA&amp;utm_campaign=designshare&amp;utm_medium=embeds&amp;utm_source=link" target="_blank" rel="noopener">iii_inspo_digital-tiles</a> by _AY


    design process
     - open CV (Python)
     - edge detection digitalisation
     - vectorisation
     - magnetic Shapes and Grid
     - mould shape 3D printing
     - hydraulic press
     - tile production
     - building pattern

as a group we decided to develop an interface for our tile-deco and pixel-cube projects (maybe a website) in order to eliminate the use of grasshopper apps and firefly plugin and make the process more accessible and easier if possible. briefly, our main goal is to support the makers and crafts, and encourage them to use digital fabrication tools.

we agreed on using OPENCV shape detector. But, in order to use OPENCV we need PHYTON, ANACONDA and VISUAL STUDIO too. firstly, we set the anaconda and phyton and opencv. then we found a code for shape recognition-detection especially for “circle” from an image. we tested that through the anaconda and of course code had some problems and we asked from CHATGPT to fix the code. more or less the code works through the image but we needed to calibrate the parameters in order to get more accurate results.

during the second day we continued to work on shape detection code. after detecting the circles on the still images we tried to configure the code for squares, rectangle, triangle, semi/quarter circles. We used edge detection and tried to convert them to defined geometric shapes, but we had problems with some undefined ones as lemon shape or croissant shape. so, in order to solve this we worked on polygon contouring but it did not ended up with smooth curves. then, Pietro joined to support us for using phyton libraries.

<div style="position: relative; width: 100%; height: 0; padding-top: 56.2500%;
 padding-bottom: 0; box-shadow: 0 2px 8px 0 rgba(63,69,81,0.16); margin-top: 1.6em; margin-bottom: 0.9em; overflow: hidden;
 border-radius: 8px; will-change: transform;">
  <iframe loading="lazy" style="position: absolute; width: 100%; height: 100%; top: 0; left: 0; border: none; padding: 0;margin: 0;"
    src="https:&#x2F;&#x2F;www.canva.com&#x2F;design&#x2F;DAFmXopQsts&#x2F;view?embed" allowfullscreen="allowfullscreen" allow="fullscreen">
  </iframe>
</div>
<a href="https:&#x2F;&#x2F;www.canva.com&#x2F;design&#x2F;DAFmXopQsts&#x2F;view?utm_content=DAFmXopQsts&amp;utm_campaign=designshare&amp;utm_medium=embeds&amp;utm_source=link" target="_blank" rel="noopener">iii_digital-tiles_scan process</a> by _AY

after some discussions, we decided to use QR code detection in opencv libraries for assigned geometric shapes as we did with the fiducials on Grasshopper-firefly application model during the Challenge-No2 and we wanted to combine that with Three JS Interactive Voxel Painter project as a grid base. We spent some hours on this approach. finally, we decided that would take months to finalize the work.

<div style="position: relative; width: 100%; height: 0; padding-top: 56.2500%;
 padding-bottom: 0; box-shadow: 0 2px 8px 0 rgba(63,69,81,0.16); margin-top: 1.6em; margin-bottom: 0.9em; overflow: hidden;
 border-radius: 8px; will-change: transform;">
  <iframe loading="lazy" style="position: absolute; width: 100%; height: 100%; top: 0; left: 0; border: none; padding: 0;margin: 0;"
    src="https:&#x2F;&#x2F;www.canva.com&#x2F;design&#x2F;DAFmXSLLBpo&#x2F;view?embed" allowfullscreen="allowfullscreen" allow="fullscreen">
  </iframe>
</div>
<a href="https:&#x2F;&#x2F;www.canva.com&#x2F;design&#x2F;DAFmXSLLBpo&#x2F;view?utm_content=DAFmXSLLBpo&amp;utm_campaign=designshare&amp;utm_medium=embeds&amp;utm_source=link" target="_blank" rel="noopener">iii_tile-design_process</a> by _AY

we went back to the basic idea to detect the edges of the each geometric shapes on the grid that we designed and decided to eliminate the shades and work on lighting in order to get the best results with this basic and simple method which can be done on OpenCv and Python.

<div style="position: relative; width: 100%; height: 0; padding-top: 100.0000%;
 padding-bottom: 0; box-shadow: 0 2px 8px 0 rgba(63,69,81,0.16); margin-top: 1.6em; margin-bottom: 0.9em; overflow: hidden;
 border-radius: 8px; will-change: transform;">
  <iframe loading="lazy" style="position: absolute; width: 100%; height: 100%; top: 0; left: 0; border: none; padding: 0;margin: 0;"
    src="https:&#x2F;&#x2F;www.canva.com&#x2F;design&#x2F;DAFlzvkz72I&#x2F;watch?embed" allowfullscreen="allowfullscreen" allow="fullscreen">
  </iframe>
</div>
<a href="https:&#x2F;&#x2F;www.canva.com&#x2F;design&#x2F;DAFlzvkz72I&#x2F;watch?utm_content=DAFlzvkz72I&amp;utm_campaign=designshare&amp;utm_medium=embeds&amp;utm_source=link" target="_blank" rel="noopener">tile-making_expirement 01</a> by _AY

__AY