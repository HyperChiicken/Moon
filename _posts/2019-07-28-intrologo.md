---
layout: post
title: "Making that Intro Roll"
date: 2019-07-17
excerpt: "Got to make a uber short intro roll using DaVinci Resolve 15"
tags: [intrologo, introroll, videologo, davinci_resolve]
comments: false
---

<figure>
   <center>
	    <img src="/assets/img/2019-07-28/GifMaker_20190728152902405.gif">
      <figcaption align="center">It's supposed to be a GIF, but the animation is too fast to capture.</figcaption>
   </center>
</figure>

&ensp;&ensp;So I decided to convert my logo into an intro roll for my youtube videos. I was dreading it beforehand with the preconception that it's a long convoluted process. Turns out it isn't. In fact, it was pretty fun to mess around with the whole thing. I decided to do this using DaVinci Resolve 15 for the following reasons:

<ul>
  <li>It's <b>FREE</b>!</li>
  <li>Some people in the industry use it, so it might be useful to learn in the long run.</li>
  <li>Lots of tutorials are avaiable online.</li>
</ul>

&ensp;&ensp;Speaking of tuturials, this one helped me out lots: <a href="https://www.youtube.com/watch?v=3qE3YUGeYjY&t=952s">https://www.youtube.com/watch?v=3qE3YUGeYjY&t=952s</a>. The video starts from importing the static logo, animating the individual components of it, and finalizing the end product. There are some steps that are glazed over when he fixes the "bugs" but it took little time to figure it out. Adding audio was not part of the tutorial, so I had to figure that out too. 

<b>NOTE: <i>Make sure to set the target FPS in the very beginning; otherwise, you'll have restart or do some awkward deleting and control+z-ing.</i></b>

<figure>
   <center>
	    <img src="/assets/img/2019-07-28/fusion.png">
      <figcaption align="center">A screenshot of the animation flow in DaVinci Resolve 15's Fusion tab.</figcaption>
   </center>
</figure>

&ensp;&ensp;My process flow goes like this: animate the logo, add sound, integrate both in the same timeline, finalize the output video.
The first step is to cut the individual components of the logo into their respective bins. This is done by merging <b>MediaIn1</b> with the trasnparent (ALPHA == 0) background, <b>Background2</b>. A merge block should appear which I labeled as <b>HYPER</b> and <b>CHICKEN_LOGO</b>. I then added a rectangle and ellipse masks to each block respectively. Next, I added a transform for each block that zooms out then back in. This is done with the help of the <b>spline</b> tab. This can also done by clicking on the timeline and adding changes to the size and whatnot manually.

<b>NOTE: <i>Clicking the points within the spline and pressing CTRL+F will smoothen the transitions of the animation.</i></b>

<figure>
   <center>
	    <img src="/assets/img/2019-07-28/spline.png">
      <figcaption align="center">A screenshot of the animation spline.</figcaption>
   </center>
</figure>

After that's done, it was time to add a chicken sound to my video. A quick google search revealed to me that DaVinci Resolve 15 has a built-in voiceover option! This can be found in the <b>fairlight</b> tab. By adding a track, changing the input to your microphone, and clicking the "<b>R</b>" box on the track, you're all set to press the record button to immortalize your voice.

<figure>
   <center>
	    <img src="/assets/img/2019-07-28/fairlight.png">
      <figcaption align="center">The fairlight tab in action.</figcaption>
   </center>
</figure>

The audio recordings automatically go to your media pool. Now all I had to do was drag and drop my audio onto the timeline and adjust to where I want it to go. <b>Voila! Intro Roll complete!</b> Well, not really, I still had to render it by going to the <b>Deliver</b> tab. But yeah, it was pretty simple process that had a tad bit of a learning curve. Overall, it's fun once you get how to cobble things together. 
