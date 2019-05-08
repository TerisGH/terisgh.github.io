---
layout: post
title: DGGI
---

{% include mathjax.html %}

Finally got a first working version of DDGI working.
It is still buggy, some light is leaking here and there.
But the basic algorithm and datastructures are there.
A total of $$32^3*192$$ rays are traced per frame, combined into
irradiance probes and sampled during the forward rasterization pass.
Next steps are to increase the visibility map resolution (currently identical to irradiance) and
fix unwanted light leaks as well as reusing the irradiance probes to shade traced rays.  

<figure>
  <img src="{{site.url}}/images/dggi.png" alt="my alt text"/>
  <figcaption>Sponza with dynamic diffuse global illumination.</figcaption>
</figure>

Here are two videos with a moving directional light:
<div style="text-align: center">
<iframe width="560" height="315" src="https://www.youtube.com/embed/xE7ZIMDbApE?rel=0;showinfo=0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen  style="text-align: center"></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/g12g2JFD6i4?rel=0;showinfo=0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>