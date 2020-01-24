# Design Process

The only way to effectively explore something that you don't already know really well is to play with it. The pretenst app gives us a very flexible world where we can learn by trial and error. The idea is to start with all the options open and gradually refine towards and end result. For example, design starts in the freedom of zero-gravity, and only later is gravity introduced.

The process could be sketched like this:

* first generate an initial structure using [tenscript](tenscript.md) or grab an existing tenscript and tweak it
* do some shaping, bending, sculpting or otherwise manipulating with the structure in its **malleable mode**, which has high pretension and where elements are very elastic
* when you are pleased with the shape, freeze it into **zen mode**, instantly removing all pretension and leaving the structure in a state where all elements are completely at rest and satisfied
* enter the realization stage where the structure gradually gets pretension re-introduced by its bars lengthening, while gravity is simultaneously raised from zero to the maximum you have chosen

Ultimately we intend this end result to become a beautiful real tensegrity structure that you can display in the living room, or maybe a larger one that can be mounted as a sculpture in the lobby, or even a huge one in a city park. We might even see tensegrity structures deployed in space or on the Moon or Mars!

Let your imagination run wild. We don't know yet what is possible.

Whether the scale is large or small, this project is about developing and spreading the understanding and technology that will be needed to make **real [physical](physical.md) structures**.

## Malleable Mode

A physical tensegrity is typically a very tight structure, where the tension is much more like a guitar string than an elastic band. Although this is where we hope to end up, it is very difficult to design tensegrities when they are like this since the structure is far too rigid.

Pretenst software starts with malleability in mind, where the way things are connected to each other is the same but pretension is extreme, and everything is also extremely elastic. This way you can twist and bend and change the whole structure or any of its parts any way you like and it will not break.

Of course, since it's just a numerical model, things are not in danger of actually breaking. But the analogy to breaking here would be that the structure vibrates in ever increasing cycles until the numbers turn to nonsense and the shape is irreperably damaged.

When in malleable mode, you can adjust lengths of the cables and bars, growing either individual intervals or selected groups of them. You can also make selections of faces and have them weld together to make structural loops, and make structural additions that were not specified in the original tenscript which generated the structure.

## Zen Mode

When the shaping is done and you have arrived at the form that you want, the next step is to leave malleable mode behind. All of the extreme pretension and elasticity has to be removed so that the structure can be turned into something that can practically built and will hold this shape when it is finished.

Shifting to zen mode involves a very simple sweep across all cables and bars where each one is made to adopt its current length rather than continue striving for the ideal length that it had in malleable mode. All of the tension and compression disappear, and since the structure is still in zero gravity it no longer has any forces to make it move. It is not fozen in the sense of being rigid, but only that it stays put because it has no reason to do otherwise.

## Playing with Physics

The pretenst model lets us "play god" and toy with physics, since we're able to change all the physics features freely. The real world is far too restricted when you want to really explore this design space. In the real world we experience constant relentless gravity, and our materials have unchanging features like their elasticity and density. We normally build things above ground so the only thing slowing down a vibration will be the air, although we could possibly build under water where everything would be slowed down and vibrations would be held back by the water resistance.

Ultimately, when we get to the stage of building the actual physical structures in the air or maybe water, we have to dial back the reckless carefree physics that the pretenst software affords and bring it back to the actual challenges that face us here on Earth (or on the Moon, or in outer space, depending on the application).

## Realization

After designing freely in malleable mode and zero gravity, we need to bring things back to the real world, but this cannot be done too quickly because the shock would inevitably shake the structure so much that it would go crazy and explode. This actually happens in the software if we're not careful, so don't be surprised if you suddenly experience an explosion while you're tweaking the physics in pretenst.

To get to the buildable structure, where the lengths and elasticities and densities correspond well enough with the physical world so that building it for real becomes possible, we have to take things slowly. Realization is a gradual process, where we go slowly from zero gravity to normal gravity, and where we go from the zen mode relaxation to an appropriate level of pretension.

It turns out to be the best approach to introduce pretension and gravity at the same time, gradually, so that the structure can become accustomed to the challenge of holding its own against the ground surface with gravity pressing downwards. But what we inevitably see as this happens is that the structure will sag a bit. As the compression and tension intervals are straining more and more to handle the increasing gravity, the shape will change.

## Annealing

It is probably generally the case that we want to maintain the shape that was designed in the context of zero gravity, even though the tensegrity structure is forced by real world circumstance to fight against gravity. The most elegeant and attractive features of tensegrity structures is that they appear to defy gravity, standing gracefully as if they are immune to the sagging effects.

What the pretenst software attempts to do is compensate for the sagging effect by choosing different material characteristics. As you may imagine, depending on the structure, some of the intervals will be strained much more than others when gravity is introduced. 

The branch of a tree, if it is extending more or less horizontally out from the trunk, will somehow be handling much more tension on the top, and handling compression on the bottom, because otherwise it would sag to the ground. The nature of trees has figured out how to do this, and in a way that also simply seems to defy gravity. Somtimes very thick main branches extend out remarkably far almost horizontally and they make it look easy!

Pretenst uses a numerical model for the structure, so the software can of course measure anything and everything to a remarkable degree of accuracy. The way that a pretenst structure sags when we add gravity is easy to capture. Certain tension intervals will be strained far more than others, and some intervals may even become completely slack in the context of the gravity challenge. These differences in strain is what the pretenst software uses in its process of annealing.

In a nutshell, it starts with zero gravity which gradually increases, and when full gravity is reached, the strain in each inteval is measured. A snapshot of all the strains is made and this is used as a hint to determine which intervals need to be strengthened so that the sag can be reduced. The elasticity of each interval is adjusted according to how much strain it shows under full gravity, so that the most strained intervals become thicker and stronger while the ones least strained are weakened. The annealing process is an attempt to make the strain the same in all intervals, in a sense balancing the structure to minimize sag.

Once the stiffnesses of the intervals has been adjusted to match the strain they have exhibited, the annealing process starts from scratch, in other words from zero gravity and in the originally designed shape in zen mode. Gravity and pretension are once again gradually added, but this time the previously more strained intervals are stiffer. The end result is that the sag is reduced, compared to last time! The structure after gravity is more like the shape of the original zero gravity design.

Once again, the strain appears, but this time the difference between the maximum and minimum strain in the individual intervals is much smaller. The annealing process can be repeated so that the sag that was apparent after the first try is reduced even further. After a few cycles the structure already reaches a sort of final state where there is still sag but its effect is minimized, depending on what the elastic and density characteristics of the materials are.

## Visualizing the Pretension

Pushing elements (bars) are being compressed to be slightly shorter than they would be without the tension, and pulling elements (cables) are being stretched slightly longer than they would be without the bars. In a pretenst tensegrity, everything is strained a bit, because otherwise the structure wouldn't be stiff. This is the heart of the matter!

In the real world such strains are certainly measurable, sometimes visible, but builders need to understand them intimately so that they can do the numbers and make sure things are built to last and carry loads without collapsing.

The pretenst software is all about fostering a deeper understanding of this very thing, so the visualization is set up to allow users to greatly exaggerate the effects of strain. This is very useful in exposing to the designer where the strain is intense and where it is weak or absent altogether.

What the visualization does, almost paradoxically, is that it shows the pushing and pulling elements at the length that they would be if each of them indidually were not strained at all! Compressed bars appear a little bit longer, and stretched cables appear a little bit shorter, so in this visualizztion the two actually do not touch each other (unless the strain happens to be zero).

Depending on the physics parameters, the effect may be so small that you cannot even see it, so pretenst has a feature which multiplies the effect to bring it unambiguously into view.

