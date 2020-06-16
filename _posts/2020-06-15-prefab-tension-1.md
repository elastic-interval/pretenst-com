---
title: "Prefab Tension"
date: 2020-06-15
categories: construction
---

## Challenge

I wanted to experience a tensegrity structure where the compression struts **only push** against the tension network, and I wanted to see how tight it could become. Typically the struts are drilled or slotted and the tension cables are used to make the final adjustments, but this became the first experiment involving a prefabricated tension network.

It was not easy, but this exploration with a prototype is supposed to lead to construction innovations to make the process more accessible. It was important to start by finding out how hard it is to build what I thought would work best, and would best illustrate the idea.

## Model

I started by making a virtual model using the **pretenst** app, focusing on the joints where the tension cords come together. If the struts are to only push on the tension network, they must have something to push on, so I decided to make them spherical. This is an image of it ray traced by **blender**:

![virtual][virtual]

There is a potential conflict visible here because the cords all cross at the midpoint of the sphere, but I naïvely thought I could have them slide past each other in the middle somehow. Turns out it was a problem indeed, but I worked around it.

## Plan

I really wanted to try out Dyneema cord, because it is super-strong, but also because it is hollow and made of 12 woven strands. I imagined wiggling a screw into the end of the cord and then tightening the screw to pinch the cord tightly against the inside of the hole.

![getting started][connect-4]

A few experiments proved that this idea worked reasonably well, so I decided to give it a try. If I could get the balls-and-cords assembled first, and then insert and lengthen the bars later, it would be interesting.

## Parts

First thing was to collect the materials together.

![getting started][start]

* non-stretchy cord - Dyneema 2mm
* wooden balls - 30mm diameter
* threaded rod - M6
* connecting nuts - longer than usual nuts
* screws - 3mm x 12mm

## Where to drill?

Drilling spherical balls is a little tricky because of their shape, but before the drilling could begin it needed to be clear where to put the holes.

I used the virtual model to calculate chord lengths, each chord being the straight line distance through the ball from one hole to the next. Using all the chords I was able to triangulate, scratching arcs from existing markings and making new markings where the scratches crossed.

![measure][measure-1]

I had the software give me **every** chord length so I could even double-check my measurements by measuring pairs that I didn't need for the original triangulation. It's a challenge to communicate sphere measurements from the software into the real world, so I was happy with this redundancy!

![measure][measure-3]

So there I had one ball, carefully measured and marked, and I drilled slight holes in it to suggest the hole entrances. But that's just **one ball**! I needed 12 of them drilled exactly the same way, but the time it would have taken to do all that by triangulation was not attractive. I had to find a shortcut.

I decided to make a kind of mold, out of several layers of aluminum foil stuck together with gradually hardening epoxy glue, because this way I could bend the surface around my one prepared ball and press hard to reveal the proto-holes, and then let it harden in the concave-spherical shape.

The result was this little guy:

![aluminum][aluminum-1]

After the underlying holes appeared, I pricked them through and then waited for the glue to get hard. Then it was time to open him up so I could re-use the pattern of hole locations that he had captured.

![aluminum][aluminum-2]

Pushing back the edges so it became a half-sphere gave me the marking mold that I needed. Inserting each of the other balls into the mold, I was able to make marks on all of the other balls without needing to redo the time-consuming triangulation-with-chords trick.

![aluminum][aluminum-3]
![aluminum][aluminum-0]

Soon afterwards I had all the balls marked.

![marked][marked-1]
![marked][marked-2]

## Drilling

This is the point at which I first stumbled, because I drilled the first set of balls all the way through for each of the 4 holes. That made the holes all meet in the center of the sphere, and after a bit of frustration I concluded that getting 4 cords to pass each other inside was just too difficult.

![drill][drill-1]

To solve the center cord conflict, I decided to try and drill the two nearest holes parallel to each other, rather than through the center of the ball.

![holes][holes-2]

To accommodate the screws I even made countersinks at the opposite ends of the holes.

![holes][holes-3]
![holes][holes-4]

## Threading

With the two parallel "eye" holes, I was able to get the cords through without any problem. There is still potentially a cord crossing, but it can only involve pairs of cords, and it's easy to let two cords pass each other.

![holes][holes-5]

The next challenge is to feed all 24 Dyneema cord segments through the correct pairs of holes such that the tension network is connected and all of the joints are oriented correctly relative to the network. This was also more difficult than expected, because it's remarkably hard to keep track of everything.

To make it easier, I used an existing tensegrity structure as a scaffolding, and stuck everything in the right place with tape. Tricky stuff, so there's much room for innovation here.

![connect][connect-1]

After this initial threading I had each cord segment strongly fixed with a screw on one end, but only threaded through the other end with a loose knot to keep it from escaping.

![connect][connect-3]

The next step was to **precisely measure** all of the ball-to-ball distances, which all had to be exactly the same within a millimeter or two, so for that I cut a little ruler out of plexiglass of the precise length. With the plexiglass holding the length right, I carefully cut the cords to length and wiggled more screws into the hollow cord, finally tightening them all up.

## Tension, meet Compression

Finally, with all the cord segments fixed at the right length, each one ready to hold two balls at the assigned distance, it was time to introduce the compression struts.

Each strut consisted of a 30cm segment of threaded rod, with a long connector nut at each end. The rods were intended to just fit snugly by themselves, and then the nut could be used to effectively lengthen the rods by a few percent to **pretense** the structure afterwards.

![connect][connect-0]

It turned out to be easier once I hung the tension network from a cord so that I could insert the rods one by one. The rods are not connected to the balls so it was a beautiful thing to observe the tensegrity taking shape with each rods only pushing on a pair of balls.

![hang][hang-1]

A few turns of each of the nuts made it possible to tighten things up until it felt a little bit like the cords were guitar strings.

![final][final-4]

## Hello Prefab Tension!

It worked! Here was the first example that I've ever had in my hands of a tensegrity where the tension network was created **while slack**, and the compression struts indroduced and tightened **later**!

![final][final-1]

Zooming in on one of the tensegrity's tension triangles, the beautiful spiral of pushing force from the bars appears. (The furry parts are just the extra unwoven dyneema fibers which surround each of the screws)

![final][final-3]

Every ball is ever so slightly captured by its spherical surface being nested in the concavity of the nut's hole after the strut is lengthened.

## Conclusion

In your hands the structure feels a bit like magic because it's so tight, so mission accomplished! The process was a bit too tricky, though. Several aspects may lend themselves to simplification, so that will have to be the focus of a future construction.



[virtual]: https://pretenst.com/images/2020-06/joint-sphere-detail-gradient.png
[start]: https://pretenst.com/images/2020-06/start.jpg
[aluminum-0]: https://pretenst.com/images/2020-06/aluminum-0.jpg
[aluminum-1]: https://pretenst.com/images/2020-06/aluminum-1.jpg
[aluminum-2]: https://pretenst.com/images/2020-06/aluminum-2.jpg
[aluminum-3]: https://pretenst.com/images/2020-06/aluminum-3.jpg
[connect-0]: https://pretenst.com/images/2020-06/connect-0.jpg
[connect-1]: https://pretenst.com/images/2020-06/connect-1.jpg
[connect-3]: https://pretenst.com/images/2020-06/connect-3.jpg
[connect-4]: https://pretenst.com/images/2020-06/connect-4.jpg
[drill-1]: https://pretenst.com/images/2020-06/drill-1.jpg
[drill-2]: https://pretenst.com/images/2020-06/drill-2.jpg
[final-1]: https://pretenst.com/images/2020-06/final-1.jpg
[final-3]: https://pretenst.com/images/2020-06/final-3.jpg
[final-4]: https://pretenst.com/images/2020-06/final-4.jpg
[hang-1]: https://pretenst.com/images/2020-06/hang-1.jpg
[hang-2]: https://pretenst.com/images/2020-06/hang-2.jpg
[holes-2]: https://pretenst.com/images/2020-06/holes-2.jpg
[holes-3]: https://pretenst.com/images/2020-06/holes-3.jpg
[holes-4]: https://pretenst.com/images/2020-06/holes-4.jpg
[holes-5]: https://pretenst.com/images/2020-06/holes-5.jpg
[marked-1]: https://pretenst.com/images/2020-06/marked-1.jpg
[marked-2]: https://pretenst.com/images/2020-06/marked-2.jpg
[measure-1]: https://pretenst.com/images/2020-06/measure-1.jpg
[measure-3]: https://pretenst.com/images/2020-06/measure-3.jpg
