# Audience

Consider this opening from an astrophysics paper I picked at random.[^arxiv]

> The dearth of planets with sizes around 1.8 R⊕ is a key demographic feature discovered by the Kepler mission. Two theories have emerged as potential explanations for this valley: photoevaporation and core-powered mass-loss. However, Rogers et al. (2021) shows that differentiating between the two theories is possible using the three-dimensional parameter space of planet radius, incident flux, and stellar mass.

If you aren't an astrophysist, this probably requires some explanation. If you are an astrophysicist, you 
probably understood that without issue.

Whenever anyone writes anything, it is important to consider the audience you are writing to. This applies to code just as much as to any other form of writing. 

This is why shorthands like `for (int i = 0; i < length; i++)` are generally considered okay even though
in most other situations `i` is pretty non-descript. Within the audience of programmers it is a known idiom.

Its also why explaining every single line of code with comments is generally not okay. Programmers know what code
is, you don't need to baby them through how loops work.[^offense]

[^arxiv]: https://arxiv.org/abs/2302.00009

[^offense]: No offense intended if you are still having trouble with loops. Its common, you will eventually get past it.