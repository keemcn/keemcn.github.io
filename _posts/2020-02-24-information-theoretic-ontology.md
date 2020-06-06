---
layout: post
title: failed {Towards an Information-Theoretic Ontology}
date: 2020-02-24
category: post 
tags: [philosophy]
use_math: true
preview:
---

*Note: This post was a failed attempt at formalizing an iffy mental model. I realized that I don't have the necessary physics background to be able to confidently say the things I tried outlining below. This is an incomplete, somewhat ugly agglomeration of ideas. Proceed at your own risk.*

## gobbledegook
Wow! You actually clicked through on the gobbledegook-filled title of this post! I'm impressed. In case you're unsure about what those words mean, here's a brief primer.

The title 'Towards an Information-Theoretic Ontology' just means that I think I've had a good insight into how the universe works, and that the insight uses concepts that come from Claude Shannon's theory of information (note: if you haven't read his [original paper](http://people.math.harvard.edu/~ctm/home/text/others/shannon/entropy/entropy.pdf), I highly recommend it).

*Information theory* is a field of math that deals with how information, broadly conceived, is transmitted and stored. It gives a formal, rigorous way of thinking about bits and how computational devices can use them.

An *ontology* is just a coherent framework that describes a group of things and how those things interact, but in the most pared-down way possible. To give you some intuition, a good example comes from particle physics: an ontology of particle physics would just be the list of particles and the list of fundamental forces that describe how they interact (we know of 4 such forces so far!). Sure, all of the higher level complexity in the universe is a direct result of those things and their interactions, but paring the complexity down to the pure essentials is part of the exercise of constructing an ontology. I'm also a math nerd, so I'm obligated to mention the obvious connection here to category theory. [^1]

[^1]: In math-speak, an ontology is just a category (but with a lot less rigor and elegance in the definition). Like a category, an ontology has two sets – one is a set of *objects*, and the other is a set of *morphisms*. At a very high level, the objects are the *things* you're interested in, and the morphisms are the *ways that those things interact with one another*. Some of the more famous categories are Set (objects are sets, morphisms are functions), Grp (objects are groups, morphisms are group homomorphisms), and Top (objects are topological spaces, morphisms are continuous functions between topological spaces).

## idea
The core insight is that conscious beings are information processors. We observe finite regions in time of the finite regions in space that are physically close to us, compress the information describing those regions, and store the compressed data in our heads. We can then recall the compressed data, decompress it, and utilize it to think. The goal is to formalize this notion of information processing and use it to build an ontology of the universe.

### things
First, we begin with the *things* in this ontology. The first type of *thing* that we're interested in is finite regions in time of finite regions of space. Imagine writing down all of the relevant positions and momenta of all of the subatomic particles that make up the Earth at some slice of time $$t_{0}$$. Now imagine you zoom across the galaxy in a ship to some remote, empty corner of space. You also have an army of tiny, atomic-sized workers that can manipulate the positions and momenta of individual subatomic particles, and a machine that can pause time for the rest of the universe (but not for you and your atomic workers). If you had enough workers, enough subatomic particles to build with, and paused time for long enough, you could feed them directions from when you wrote down all of the relevant information about the Earth earlier and perfectly reconstruct the exact original state of the Earth at $$t_{0}$$. 

That's cool, but we can go further. It turns out that time is, for all intents and purposes, discrete (the [Planck time](https://en.wikipedia.org/wiki/Planck_time), denoted $$t_{P}$$), so we now unpause time using our machine, wait one $$t_{P}$$, and record the state of the Earth again. If we keep doing this process for all $$\{t_{0}+nt_{p}, n \in \mathbb{N}\}$$, we can record everything on Earth until time itself ceases to exist.

But we don't want to do that for all time – we just want to do that for some finite amount of time. This is to say that we're only interested in all $$\{t_{0}+nt_{P}: n \in A \subset \mathbb{N}\ , \vert A \vert < \infty \}$$. Now that you have the intuition, we can crystallize things a bit. I call a *scene* a bounded region of space and a perfect, complete record of the relevant characteristics of all of the subatomic particles in that region (type of particle, position, momentum) at a finite number of time slices. Without loss of generality, we can attach the temporal information into this set of 'relevant characteristics', and then obtain a set of tuples. So we finally arrive at this quasi-definition. A *scene* is a set of tuples $$\{a_{0},\ldots, a_{n}\}$$ where each $$a_{i}=(v,\vec d,\vec \rho,t_{0}+it_{P})$$. $$v$$ is the variety of particle, $$\vec d$$ is the position vector (quantized to a maximum resolution of the Planck length), and $$\vec \rho$$ is the momentum vector. Note that the indexing set on the tuples embeds the data about our $$A$$ from above into the scene. There are certainly some details that I'm skimping out on, but I'm just sketching out a bit of structure in this piece.

Great, so we have the notion of a scene – a perfect record of a region of spacetime...

### relations

There's a fairly intuitive sense in which watching TV is like looking through a wormhole to the past, but we can add rigor to this notion. Unfortunately, the word 'wormhole' is already a well-defined concept in physics, so instead I'll call this mathematical analogue a *tunnel*. A *tunnel* is a tuple $$(A,B,C,f,g)$$ where $$A$$ and $$C$$ are disjoint states of some bounded region of the standard Minkowski spacetime, $$B$$ is an arbitrary set, $$f$$ is a compression scheme that maps $$A \to B$$, and $$g$$ is a decompression scheme that maps $$B \to C$$. To disambiguate, a disjoint state of some bounded region of the standard Minkowski spacetime is... 

Let's do a sanity check to make sure that the tunnel as defined earlier...