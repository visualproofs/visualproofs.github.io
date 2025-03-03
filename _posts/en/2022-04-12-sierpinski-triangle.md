---
layout: post
title:  "Sierpinski Triangle"
author: solida
categories: Fractals
image: assets/images/sptriangle.png
lang: en
---
Fractals are irregular, self-similar geometric shapess. 
In other words a fractal is a pattern, where when you zoom in, similar patterns appear at all smaller scales. Fractals can be thought of as never-ending patterns.
They are capable of describing many irregularly shaped objects or spatially non-uniform phenomena in nature such as coastlines and mountain ranges.


## Now that we know what fractals are, what is the Sierpinski triangle?
One of the most well known examples of fractals is the Sierpinski triangle. The easiest way to construct such a triangle is by starting with an initial, equilateral triangle. We then divide this triangle into 4 smaller equiliteral triangles and remove the center copy to construct a shape that consists of three triangles. This is called the first approximation of the Sierpinski triangle. We then proceed recursively by applying this same procedure to these triangles, which creates smaller triangles to which we again apply this procedure and so forth. 

[Wacław Sierpiński (1828-1969 AD)](https://en.wikipedia.org/wiki/Wac%C5%82aw_Sierpi%C5%84ski) was the first mathematician to think about the properties of this triangle, but this pattern is to be found in artwork, patterns, and mosaics many centuries earlier as in the pictures below:

![walking]({{ site.baseurl }}/assets/images/collage.jpg)

### Removing triangles method

The Sierpinski triangle may be constructed from an equilateral triangle by repeated removal of triangular subsets:
1. Start with an equilateral triangle.
2. Subdivide it into four smaller congruent equilateral triangles and remove the central triangle.
3. Repeat step 2 with the smaller triangles forever


#### Try it for yourself
We can visualize this process using the slider to control the stage in the construction below:
<div id="observablehq-f40c7c08">
  <div class="observablehq-viewof-sierp_steps"></div>
  <div class="observablehq-sierp_approx"></div>
</div>
<script type="module">
  import {Runtime, Inspector} from "https://cdn.jsdelivr.net/npm/@observablehq/runtime@4/dist/runtime.js";
  import define from "https://api.observablehq.com/@864af2bf64442aa6/construction-of-the-serpinski-triangle.js?v=3";
  (new Runtime).module(define, name => {
    if (name === "viewof sierp_steps") return Inspector.into("#observablehq-f40c7c08 .observablehq-viewof-sierp_steps")();
    if (name === "sierp_approx") return Inspector.into("#observablehq-f40c7c08 .observablehq-sierp_approx")();
  });
</script>

### The Chaos Game

The chaos game is a method to generate fractals with the help of polygons.

The rules will be explained using the example of a triangle. It has the corner points $$A$$, $$B$$ and $$C$$. You start the chaos game at a random point $$P_1$$ within the triangle. To calculate the next position $$P_2$$, you choose one of the three corner points of the triangle at random and place $$P_2$$ in the middle of the route between point $$P_1$$ and the randomly selected corner point. 
You repeat this process as often as you like and draw every point you obtain on to the screen.

Some areas of the triangle are unreachable in later steps. 
These areas form a fractal pattern. Only the first steps can reach these areas, all other points fall in between.

#### Try it for yourself

Click on the button start to generate a such triangle.
You can restart to regenerate the triangle differently.
Clicking on Clear will reset the simulation.
<div id="observablehq-a077419d">
  <div class="observablehq-viewof-start"></div>
  <div class="observablehq-viewof-clear"></div>
  <div class="observablehq-canvas"></div>
</div>
<script type="module">
  import {Runtime, Inspector} from "https://cdn.jsdelivr.net/npm/@observablehq/runtime@4/dist/runtime.js";
  import define from "https://api.observablehq.com/@864af2bf64442aa6/construction-of-the-serpinski-triangle.js?v=3";
  (new Runtime).module(define, name => {
    if (name === "viewof start") return Inspector.into("#observablehq-a077419d .observablehq-viewof-start")();
    if (name === "viewof clear") return Inspector.into("#observablehq-a077419d .observablehq-viewof-clear")();
    if (name === "canvas") return Inspector.into("#observablehq-a077419d .observablehq-canvas")();
  });
</script>
