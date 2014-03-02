Moving to an idea of "preset groups", with the idea that a given
age might have 30% veins, and 50% clouds, each of which might have
child distributions or "same seed" distributions.

Ultimately, the question is: Do the multiple distributions for a given
material stay in one file, or in different files?

As an end user, I might want to customize a single distribution, and
leave the rest as "normal".

For a world, I might want to use mutiple distributions. It might
happen that there are 5 different iron distributions being pulled in.
They don't have to be in the same file.

So the answer is simple: Multiple distributions go into the same file
only if they are "the same distribution, just specified in pices".
Example: lava and diamonds. Emeralds and silverfish. Pipes (air) and ores.

---

With that idea, suddenly the way to do "preset groups" becomes clear
as well. A given file that defines a set of distributions is
parameterized.

So the "dimension" file defines the parameters, then includes some set
of materials.

---

So how to handle materials? Mod X adds a,b,c. Dimension D is defined
around "Y". Y doesn't know about mod X, or materials a,b,c.

Is the default to say "Include these at base rates", or something
else?

In other words, do we include all materials, and define properties we
know about, letting the rest go normal; or, only include the materials
we care about?

Proposed solution:

1. Some materials are "basic"; these appear in a stock config in all
dimensions unless that dimension does something special.
2. Some materials are "special"; these only appear in dimensions that
ask for them specifically.

Examples of the "special"s: 
1. Extra cave nodes.
2. Anything from the Creeporium mod (or whatever name it adopts).
3. Nether ores and nether quartz (NB: I just found some of them in a
mystcraft cave world that had stone ground. Mods included UB and
Geostrata.)

Equally, those can be added in manually by adjusting the file for that
dimension.

So ...

That last one brings up an interesting point. If I have a mystcraft
age that has a netherrack ground, then the normal distributions won't
find stone. Adding in the nether ores in ... the only file to adjust
is the dimension specific options file -- which can only do things
like set a distribution from 0 to non-zero. Hmm...

Which implies that everything gets loaded, and a lot of things get
zero distribution. LOTS.

...

