Refactoring speech
==================

Implications of refactoring and code smells.

# Questions asked

We all know ugly program code is bad. When readability gets worse, the time
used on maintainenance goes up, the number defects goes up and
more importantly developers get pissed off by having to work on

But all code smells can't be eqully important? Is there a way to
accurately measure the implications of the different code smells so
we can know wich ones are important and which ones are not?

After all Martin Fowler's book on Refactoring only gives you a list
of code smells and tells you have to clean up your code. He and
others still only has a "hunch" regarding which ones are important.


# Methods used

What if you hire 6 different programmers working offline, give them a
set of programming tasks, log every tap on their keyboard and every mouseclick
from within their IDE. Then analyse the source repository
with tools that recognises code smells (Borland Together and InCode).
After half a year you end up with massive amounts of data.

At the Simular research lab they needed to rewrite a web based system
for keeping track of projects, experiments and people. This occasion
was used to conduct an experiment.

Another research project at the Simula Research had finished measuring
the skill levels of 200 programmers. Out of those 200 people, 6 developers
from Poland and the Check republic with approximately similar skill levels were
selected. During the 6 months the project lasted, they got frequent visits
from Aiko Yamashita.

# Findings

## Interface Segregation Principle violations considered harmful

Interface Segregation Principle is one of the SOLID design principles
described by Robert Martin, that states:

    Clients should not be forced to depend upon interfaces that they do not use.

The idea is that when a class implements an interface, it should only get
methods that it needs. This leads to less coupling and  higher cohesion.

Data shows number of defects goes up if this code smell is detected, the
changes are time consuming and costly, and leads to
program comprehension and information searching

    Implications: Yes. Very costly.
    Significance: Good (enough)


    References: [Phd Disertation page 192](http://simula.no/publications/Simula.simula.1456/simula_pdf_file)

## God class considered harmfull

This is related to Interface Segregation Principle.

## "Data clumps" probably not harmful

Description from coding horror:

    If you always see the same data hanging around together, maybe it
    belongs together. Consider rolling the related data up into a larger class."

The data suggests this is not important.

    Significance: Quite high

## Some code smells more often together than others

ISP violation & Shotgun surgery appears often together.
I seems it is more or less the same problem? Ripple effect.
Maybe another name would be more appropriate?

Reference: [Table at page 189](http://simula.no/publications/Simula.simula.1456/simula_pdf_file)

## Cyclomatic complexity not harmful

Next myth to bust. This should not be significant.

Description.

    The cyclomatic complexity of a section of source code is the count of the number of
    linearly independent paths through the source code.

Code examples.
