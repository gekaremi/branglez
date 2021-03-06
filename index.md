# Applying Fixed Point Numbers for Astronomy

## Branglez = Binary Radian ANGLEZ

Scientists are concerned with describing the real world using mathematical abstractions. They often take the form of formulas, in many cases equations, differential or integral. However, it turns out very quickly that most of the real problems cannot be solved analytically. Then they have to be solved numerically, using computers. In fact, the text of reality is translated into the language of formulas, after which they are translated into programming languages. But any translation is imperfect and prone to loss and distortion. It is helpful to remember that ultimately everything will need to be translated into computer language. Sometimes, you can try to write in it right away, but this requires restructuring and supplementing the standard process of scientific thinking. In addition, it is important to take into account the peculiarities of the problem, which will determine the algorithms used and the types of data representations.

Before the widespread adoption of floating point numbers, a different standard, fixed point numbers, was widely used in scientific modeling. This format has many advantages, such as implementation elegance and computational speed, and one of the main drawbacks is the circular overflow behavior. However, in tasks related to measuring angles and other cyclic values, this behavior, on the contrary, is a huge advantage, since it automatically ensures that the values ​​are kept in the required range, maintains the same accuracy and increases the determinism of calculations, reducing the level of machine errors. For this reason, binary angular measurements are finding applications in robotics, games, and real-time applications.

Another advantage is that fixed-point numbers help to get rid of some of the conditional operators, which allows you to achieve the so-called branchless programming and speed up calculations on modern processors.

The report will talk about the use of [Binary Angular Measurement](https://en.wikipedia.org/wiki/Binary_scaling#Binary_angles) to study the evolution of the rotation of asteroids and planetary satellites.

### Inspiration:

One of the first publications I read during my research on this topic, almost a couple of years ago, was a blog post titled ["Sin & Cos: The Programmer's Pals!"](https://www.helixsoft.nl/articles/circle/sincos.htm). 
I can remember the date quite accurately because I found this article thanks to [Hacker News entry](https://news.ycombinator.com/item?id=16526942).
As, I found out later, its author was [Dr. Martijn van Iersel](https://github.com/amarillion), one of the developers of the [Allegro library](https://www.allegro.cc/manual/5/fixed.html ), which has support for fixed-point numbers and binary angles. Communication with him and discussion of issues helped to better understand the pros and cons of this idea, and most importantly, led to the realization that ordinary fixed-point numbers and binary angular measurements are two different entities, albeit very similar. Therefore, I am very grateful to him for his help.



### Acknowledgement.
The reported study was funded by RFBR according to the research project 19-02-00811.

### Citation
Presentation available and citable here [https://doi.org/10.5281/zenodo.4279768](https://doi.org/10.5281/zenodo.4279768)

This project had been started as part of this work: [Chaos and relativistic effects in the rotational dynamics of minor planetary satellites
](https://ui.adsabs.harvard.edu/abs/2020jsrs.conf..339M/abstract)  (Melnikov, A. V.; Pashkevich, V. V.; Vershkov, A. N.; Karelin, G. M.)

Publication: 
Proceedings of the Journées 2019 "Astrometry, Earth Rotation, and Reference Systems in the GAIA era", Observatoire de Paris, Paris, France, 7-9 October 2019, Ed. C. Bizouard, pp. 339-344

so before publication of  next paper,  if you consider, you can cite this one :) Thanks 

### Presentation
Available and citable here [https://doi.org/10.5281/zenodo.4279768](https://doi.org/10.5281/zenodo.4279768)

### Disscusion
If you have any questions, ideas or anything to share, I want to propose using the ["Issue"](https://github.com/gekaremi/branglez/issues) of current repository as forum for such activities.


### Collection of interesting links

First of all, incredible collection about floating-ponts numbers.

[References](https://floating-point-gui.de/references/)
Where you can find:

"Documents that contain more in-depth information about the topics covered on this wbesite:"

    Current version of IEEE 754 standard
    What Every Computer Scientist Should Know About Floating-Point Arithmetic
    Homepage of William Kahan (architect of the IEEE 754 standard, lots of interesting links)
    Decimal Arithmetic FAQ
    Comparing floating-point numbers, 2012 Edition
    Tool to convert numbers between bases, including fractions
    Float Toy (toggle individual bits to see what the effects on the value are)
    IEEE 754 Visualization (another bit toggling tool)
    Float Exposed (toggle bits or enter values, lots of information)
    The result of 0.1 + 0.2 in various programming launguages



[Half-Precision Floating-Point, Visualized](https://observablehq.com/@rreusser/half-precision-floating-point-visualized) by Ricky Reusser rreusser.github.io

[Video: The Neglected Art of Fixed Point Arithmetic](https://www.youtube.com/watch?v=jvrPw-nxFdk)
Assembly 2006 seminar presentation.
Author: Jetro Lauha


[Angles, directions, and their binary representation](https://www.genericgamedev.com/general/angles-directions-and-their-binary-representation/)
Posted on 2015-04-06 by Paul Scharf


[How many floating-point numbers are in the interval 0~1?](https://lemire.me/blog/2017/02/28/how-many-floating-point-numbers-are-in-the-interval-01/)
Daniel Lemire's blog
Daniel Lemire is a computer science professor at the University of Quebec (TELUQ) in Montreal. His research is focused on software performance and data engineering. He is a techno-optimist.



[Fast fixed-point sine and cosine approximation with Julia](https://nextjournal.com/zorn/fast-fixed-point-sine-and-cosine-approximation-with-julia) by [Soeren Zorn](https://github.com/zsoerenm)•Feb 04 2020
Repository [FixedPointSinCosApproximations](https://github.com/JuliaGNSS/FixedPointSinCosApproximations.jl)


[arXiv:1705.10416 -- Finding Root Causes of Floating Point Error with Herbgrind](https://arxiv.org/abs/1705.10416)
Alex Sanchez-Stern, Pavel Panchekha, Sorin Lerner, Zachary Tatlock

[What Every Computer Scientist Should Know About Floating-Point Arithmetic](https://docs.oracle.com/cd/E19957-01/806-3568/ncg_goldberg.html) 
Note – This appendix is an edited reprint of the paper What Every Computer Scientist Should Know About Floating-Point Arithmetic, by David Goldberg, published in the March, 1991 issue of Computing Surveys. Copyright 1991, Association for Computing Machinery, Inc., reprinted by permission. 

[Best Practices for Scientific Computing](https://journals.plos.org/plosbiology/article?id=10.1371/journal.pbio.1001745)
Published: January 7, 2014

[Good enough practices in scientific computing](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005510)
Published: June 22, 2017


#### TomF's Tech Blog  It
He works at Intel on GPU and CPU core architectures.
He worked at Oculus VR on the distortion and timewarp presentation pipeline and many [other](http://eelpi.gotdns.org/)
And he defended fixed-point in [wikiblog](http://eelpi.gotdns.org/blog.wiki.html) post *A matter of precision* created 1 May 2006 and [updated](https://twitter.com/tom_forsyth/status/430762126471229440) at 29 November 2014.


#### Random ASCII – tech blog of Bruce Dawson

[Don’t Store That in a Float](https://randomascii.wordpress.com/2012/02/13/dont-store-that-in-a-float/)
Posted on February 13, 2012

[Intel Underestimates Error Bounds by 1.3 quintillion](https://randomascii.wordpress.com/2014/10/09/intel-underestimates-error-bounds-by-1-3-quintillion/)
Posted on October 9, 2014


№№№ Fixed-Point Real Numbers
[Document number: P0037R7](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2019/p0037r7.html)
Date: 2019-06-17
Reply-to: John McFarlane, wg21@john.mcfarlane.name
Audience: SG6, LEWGI

Fixed-Point Real Numbers
Introduction
This proposal introduces a system for performing fixed-point arithmetic using integral types.
