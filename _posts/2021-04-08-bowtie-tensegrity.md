---
title: "Bow Tie Tensegrity"
date: 2021-04-08
description: "better bend resistance"
categories: construction
tags: [tensegrity]
---

# Rigidity

The recent explorations into the [Six Twist Essential](/construction/2021/03/29/six-twist-essential) tensegrity highlighted the inherent interesting degrees of freedom that the minimal configuration has. The flexibility comes from the tension hexagon.

![tension hex](/images/2021-03/tension-hex.jpg)

Before I started building these, I considered it normal build towers that resisted bending by using the triangulated configuration that [Ken Snelson used](https://krollermuller.nl/en/kenneth-snelson-needle-tower) in my [Brass and tulips](/construction/2020/10/12/brass-and-tulips) project, and later just kept going on that track to build the crazy [Halo by Crane](https://pretenst.com/construction/2020/10/26/halo-1) structure.

This pulls the hexagons into **zig-zags** and makes adjacent twists snuggle closer and interpenetrate. The end result is a rigidity where some "Jitterbugging" takes place where the triangles twist.

But there is another way to pull the hexagons into zig-zags and tighten things up!

By connecting **across twists** so that an upper neighbor is connected to a lower neighbor across the twist that is in between.

![cords crossing twists](/images/2021-04/cords-crossing-twists.jpg)

What was previously a hexagon of tension in the minimal case gets a new diagonal tension line, and the shape that results from that made me think of a bow tie.

![real bow tie](/images/2021-04/real-bow-tie.png)

## First in the virtual

Firs thing I had to do was rewrite the [app](/app/) to enable these different connection strategies.

* Minimal
* Snelson style
* Bow tie

![minimal snelson bow tie](/images/2021-04/minimal-snelson-bow-tie.png)

I was able to separate the processes nicely. First generate the whole structure with minimal tension count and then, at the end, add the different extra connections depending on the strategy.

It was very interesting to play with bow tie connected versions of all the structures that had been generated up to now!  They seem to have better rigidity with respect to resisting bending.

## Trying it for real

I decided to adapt a [Six Twist Essential](/construction/2021/03/29/six-twist-essential) (that has not yet been sold) to try out this new way of connecting.

I built it by adding the extra short cables during the prefabrication of the tension network.

<video width="800" height="600" autoplay="autoplay" loop="true" muted="true">
  <source src="/images/2021-04/bow-tie-twirl.mp4" type="video/mp4" />
  Your browser does not support the video tag.
</video>

## Conclusion

I'm not entirely certain but this feels like something new!

It's a minimal number of tension lines added to the [Six Twist Essential](/construction/2021/03/29/six-twist-essential) but it also connects pairs of twists which are otherwise not directly connected even in the [Needle Tower](https://krollermuller.nl/en/kenneth-snelson-needle-tower).

It still felt like something was needed, because the twists on either end seemed to be not connected enough and not behaving properly when stressed.

I was able to add a second *radial tension* on the end twist, and then with a bit of threaded rod, pull the two radials together. It stood so proudly I decided to make a flag pole of it.

![bowtie-flag](/images/2021-04/flag.jpg)

This way of completing the final twists has a beautiful effect, since pressure from above actually *tightens the upper radial* while it *loosens the lower one*!




