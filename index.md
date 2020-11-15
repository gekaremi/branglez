# Applying Fixed Point Numbers for Astronomy

## Branglez

Scientists are concerned with describing the real world using mathematical abstractions. They often take the form of formulas, in many cases equations, differential, integral. However, it turns out very quickly that most of the real problems cannot be solved analytically. Then they have to be solved numerically, using computers. In fact, the text of reality is translated into the language of formulas, after which they are translated into programming languages. But any translation is imperfect and prone to loss and distortion. It is helpful to remember that ultimately everything will need to be translated into computer language. Sometimes, you can try to write in it right away, but this requires restructuring and supplementing the standard process of scientific thinking. In addition, it is important to take into account the peculiarities of the problem, which will determine the algorithms used and the types of data representations.

Before the widespread adoption of floating point numbers, a different standard, fixed point numbers, was widely used in scientific modeling. This format has many advantages, such as implementation elegance and computational speed, and one of the main drawbacks is the circular overflow behavior. However, in tasks related to measuring angles and other cyclic values, this behavior, on the contrary, is a huge advantage, since it automatically ensures that the values ​​are kept in the required range, maintains the same accuracy and increases the determinism of calculations, reducing the level of machine errors. For this reason, binary angular measurements are finding applications in robotics, games, and real-time applications.

Another advantage is that fixed-point numbers help to get rid of some of the conditional operators, which allows you to achieve the so-called branchless programming and speed up calculations on modern processors.

The report will talk about the use of Binary Angular Measurement to study the evolution of the rotation of asteroids and planetary satellites.


### Acknowledgement.
The reported study was funded by RFBR according to the research project 19-02-00811.

### Citation
This work had been started as part of this paper:  Chaos and relativistic effects in the rotational dynamics of minor planetary satellites 
so before publication next paper,  if you consider, you can cite this :) Thanks 
[Link](https://ui.adsabs.harvard.edu/abs/2020jsrs.conf..339M/abstract)
