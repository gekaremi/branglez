# Applying Fixed Point Numbers for Astronomy

## Branglez

Scientists are concerned with describing the real world using mathematical abstractions. They often take the form of formulas, in many cases equations, differential, integral. However, it turns out very quickly that most of the real problems cannot be solved analytically. Then they have to be solved numerically, using computers. In fact, the text of reality is translated into the language of formulas, after which they are translated into programming languages. But any translation is imperfect and prone to loss and distortion. It is helpful to remember that ultimately everything will need to be translated into computer language. Sometimes, you can try to write in it right away, but this requires restructuring and supplementing the standard process of scientific thinking. In addition, it is important to take into account the peculiarities of the problem, which will determine the algorithms used and the types of data representations.

Before the widespread adoption of floating point numbers, a different standard, fixed point numbers, was widely used in scientific modeling. This format has many advantages, such as implementation elegance and computational speed, and one of the main drawbacks is the circular overflow behavior. However, in tasks related to measuring angles and other cyclic values, this behavior, on the contrary, is a huge advantage, since it automatically ensures that the values ​​are kept in the required range, maintains the same accuracy and increases the determinism of calculations, reducing the level of machine errors. For this reason, binary angular measurements are finding applications in robotics, games, and real-time applications.

Another advantage is that fixed-point numbers help to get rid of some of the conditional operators, which allows you to achieve the so-called branchless programming and speed up calculations on modern processors.

The report will talk about the use of [Binary Angular Measurement](https://en.wikipedia.org/wiki/Binary_scaling#Binary_angles) to study the evolution of the rotation of asteroids and planetary satellites.


### Acknowledgement.
The reported study was funded by RFBR according to the research project 19-02-00811.

### Citation
This project had been started as part of this work: [Chaos and relativistic effects in the rotational dynamics of minor planetary satellites
](https://ui.adsabs.harvard.edu/abs/2020jsrs.conf..339M/abstract)  (Melnikov, A. V.; Pashkevich, V. V.; Vershkov, A. N.; Karelin, G. M.)

Publication: 
Proceedings of the Journées 2019 "Astrometry, Earth Rotation, and Reference Systems in the GAIA era", Observatoire de Paris, Paris, France, 7-9 October 2019, Ed. C. Bizouard, pp. 339-344



so before publication of  next paper,  if you consider, you can cite this one :) Thanks 

### Presentation
Will be available here after video meeting

### Collection of interesting links

First of all, incredible collection about floating-ponts numbers.

[References]https://floating-point-gui.de/references/
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

#### TomF's Tech Blog  It
He works at Intel on GPU and CPU core architectures.
He worked at Oculus VR on the distortion and timewarp presentation pipeline and many [other](http://eelpi.gotdns.org/)
And he defended fixed-point in [wikiblog](http://eelpi.gotdns.org/blog.wiki.html) post *A matter of precision* created 1 May 2006 and [updated](https://twitter.com/tom_forsyth/status/430762126471229440) at 29 November 2014.


