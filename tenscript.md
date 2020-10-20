# Tenscript

The foundation of our exploration of tensegrity is the ability to generate structures systematically. For this we have created **tenscript**, which is a minimal language describing how to grow and connect tensegtrity structure.

## The Twist

The 

![twist](images/2020-07/twist-a.png)

## The Omnitwist

Tenscript builds tensegrities on the basis of the simplest symmetrical unit, made with 6 compression bars and 8 triangles of tension, which we call the tensegrity brick. The lengths of its elements are derived from the classic irrational number, the Golden Ratio called "phi" or &phi; (1.61803398874989484820... to be more precise). When the 24 cables have length 1, the 6 bars have length &phi;.

The smallest tenscript program is this one, generating only the brick unit:

    (0)

![0](images/brick-0.png)

Each of the brick's 8 triangles is given a name which allows us to specify exactly how bricks are to be connected to each other, and the names are arranged  according to their relationships, and the uppercase/lowercase of the names indicate a kind of polarity.

The top triangle is called "A" and the bottom triangle is called "a". The three triangles adjacent to "A" near the top are called "b", "c", and "d", and the bottom triangles adjacent to "a" are called "B", "C" and "D". Lowercase names are on the opposite side their uppercase counterparts, so "c" is opposite "C", and so on.

## Chirality: Left-handed and Right-handed

The brick's triangles are divided into two groups, the right-handed and left-handed ones. This comes from how the bars are angled where they touch the triangles of cables. To see how this works, pick a triangle and observe how the bars "spin" towards it from the inside in one direction. If you have the curl of your fingers follow the spin and your thumb pointing outwards, only one of your hands will fit on each triangle.

Adjacent triangles (sharing a joint) are always of opposite chirality. By convention, the uppercase names are right-handed and the lowercase ones are left-handed. The triangles adjacent to the right-handed "A", which are "b", "c", and "d" are left-handed just like "a".

## Tensegrity Columns

Bricks are by default extended in the top "A" direction to make tensegrity columns of any length. The minimal program above "(0)" says "Build zero new bricks on the A triangle", and longer columns are built with larger numbers.

    (1) - build one brick on top of the first one
    (5) - build five bricks on top, column of 6
    (27) - a column of 28 bricks

![1](images/brick-1.png)
![5](images/brick-5.png)
![27](images/brick-27.png)

## Branching

The other triangle names are used when the structure is to branch off in the different directions, and later on when a program has to point out the triangles which are to be joined together.

Now, since the default direction is "A", these two programs mean exactly the same thing:

    (1) = (A1)

However, there is an important difference. The lone numbers describe how many bricks to add to the current brick **before** branching. The column described by the lone number is generated first, and then the branch or branches described by the letter-number combinations.

The following program will build a column and then branch off in the "b" direction with another column, effectively creating a kind of "knee": 

    (3,b3)

![3b3](images/branch-3b3.png)

Just as easily, tenscript allows for branching in more than one direction at the same connection point, and when more than one branch is specified, they actually grow out at the same time as well. Here are some simple branching programs to illustrate:

    (2,b2,c2) - two bricks in the "A" direction, then two branches of two bricks each
    (3,c3,d13) - three bricks, then branching in a short and a long column
    (1,b1,c1,d1) - one brick up, then all possible branches outwards

![1b1c1d1](images/nexus-1b1c1d1.png)

Note that programs like this can also create messy structures that you may not want. For example, these programs build a column of 3 bricks and then double back in the direction it came from, overlapping the original:

    (2,a2) - build straight backwards into the original
    (2,C2) - build a sharply bent knee which starts by overlapping

## Nesting

So far the programs we've looked at have just a single pair of brackets, but tenscript allows nesting or "recursion", so we can build much more complicated and interesting structures. When you see a letter-number combination in tenscript, it's actually shorthand for an expression leaving the brackets out, so:

    (3,b3) is the same as (3,b(3))

This is where things get much more interesting since we can now imagine putting code inside of code. This program will build a structure with two knees, branching twice:

    (3,b(3,c3))

![zzi](images/zig-zag-initial.png)

The instructions here is to start by adding three bricks on top of the "A" triangle, turning in the "b" direction to build three more, and then once again at the end of the second column branching in the "c" direction to build a third column.

If this is starting to look complicated, fasten your seatbelts, because once you have the ability to nest code inside of code, things get very weird indeed and we've just gotten started. As you may have guessed, we will be swimming in brackets.

For example, here is a program which keeps building like the one above, column after column, every time in exactly the right branch direction so that it eventually returns to almost where it started. It builds what we call a "zig-zag ring":

    (a1,c(3,b(3,d(3,c(3,b(3,d1))))))

![zzincomplete](images/zig-zag-incomplete.png)

The first brick is however not connected to the last one so it doesn't actually complete the ring. For that we need another feature: marking.

## Mark to Connect

So far we have been able to grow new bricks and branch in various directions, finally reaching the point of building a zig-zag ring where the first brick is very near the last brick, but we have only grown new bricks and never connected existing bricks together.

Tenscript has another feature to handle this which is the ability to **mark** the triangles of the bricks or, in other words, to tag them with a number. The tenscript interpreter is set up to connect triangles which are tagged with the same number. Which number it is makes no difference at all, because it's just a tag.

Now this is not at all easy to think about, but we need this kind of thing to make connecting possible. Marking triangles is done by adding an item starting with the letter "M" for mark, then naming the triangle of the current brick which is to be marked, and then giving the mark number. So tagging the "b" triangle of the current brick with the number "8" would be done with "Mb8".

To illustrate this, it's easiest to see an unmarked program beside a marked program so here we mark triangles of the "zig-zag ring" mentioned above so that the ends of the C-shaped zig-zag are connected together. This way we can complete the ring! To make it a little more readable, spaces are added:

    (a1,      c(3,b(3,d(3,c(3,b(3,d1      ))))))
    (a(1,MA7),c(3,b(3,d(3,c(3,b(3,d(1,MA7)))))))

![zzcomplete](images/zig-zag-complete.png)

As you can see, in both cases the "1" is replaced with its equivalent "(1)" and then the brick's "A" triangle is marked by the "MA7" to make "(1,MA7)".

## Scaling

Historically, the initial trigger for creating this project was the first shocking encounter with the "Needle Tower" sculpture by Kenneth Snelson. It seemed to defy gravity and it also seemed to be taller than it actually ways. This sculpture starts large at ground level and then every section extending upwards becomes progressively smaller.

Tenscript has a feature which makes tensegrity columns follow this same pattern of diminishing size in the form of the "S" command which stands for "scale". The command takes a percentage as a parameter, and it applies to each brick in the column progressively, so "S99" builds a tower that tapers slightly, and "S101" builds one that gradually increases in size.

A seventeen brick Snelson Needle Tower column turns out to be a tiny simple program which includes the scale command:

    (16,S90)

![tower-s90](images/tower-s90.png)

Combining scaling with branching and marking starts to give us some very pretty and interesting structures indeed, such as the "bulge ring":

    (A(8,S85,MA1),a(8,S85,MA1))

![bulge-ring](images/bulge-ring.png)

Here, there are two eight-brick tapering columns extending in opposite directions "A" and "a", which then have their end triangles marked so that the are drawn together and welded, resulting into a ring.

## Cable Rings

Another way to look at the tension in this single brick is to forget about the 8 triangles, but instead observe that the tension cables make up 4 intermingled rings of tension, each making a zig-zag pattern around the shape. Since the brick is a regular shape, all of these rings are identical.

We can say that each ring is like a zig-zag equator which points out four different rotation axes. Remember these rings because they come into play when we start making connections between bricks.

## Melting Together

Bricks connect together by melting triangles of opposing chirality together, turning a star-of-david shape into a regular hexagon. To melt together, the opposing tension triangles are replaced with a ring of tension capturing all 6 points, and extra connector cables are added which bind the bars of one to the bars of the next so that the bricks become one.

This trivial program shows only the melting together of two bricks:

    (0) vs (1)

![0](images/brick-0.png)
![0](images/brick-1.png)

The new tensegrity then consists of 12 bars, where the new brick has been added to replace the "A" triangle and it is melted into the next brick's opposing "a" triangle.

Something else also takes place when two bricks are melted together, because the new column structure has a very different shape. 

## Multiple Sections

Tenscript is encoded as a string of characters, and as you've seen, often with many brackets. The character string can be subdivided into sections using the colon character ":". For example, you can give a name by adding a section with quotes:

    'Axoneme':(16,S90)

Other sections can be added as well, which allows for both composition and for specifying what the marks are to be used for. Other sections are therefore prefixed with "0=", "1=", "2=", etc which indicates the mark number.

## Composition with "subtree"

In tenscript, you can create subroutines and effectively compose construction programs using marks which substitute subtrees.

    'Composed':(3,b(2,MA0),c(2,MA0),d(2,MA0)):0=subtree(b2,c2,d2)

![composed](images/composed.png)

Here you can see that the 3-column fanout is defined in the subtree and built at the end of three different branches. This makes the whole program much shorter since there is less repetition.

## Face Distancing

Another feature which uses the special mark sections is "face-distance-N" which instructs the builder to create intervals between all of the marked faces and change them to "N %" of their original length.  So for example this program chooses the final faces on its three legs and pulls them until they are at a 35% distance from where they started.

    'Thick Tripod':(A1,B(3,MA1),C(3,MA1),D(3,MA1)):1=face-distance-35

As a result, the legs are pulled inwards so that the structure grows thinner and taller.

![distancing](images/distancing.png)
