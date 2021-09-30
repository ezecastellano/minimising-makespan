# Minimising Makespan of Discrete Controllers: A Qualitative Approach


Qualitative controller synthesis techniques produce controllers that guarantee to
achieve a given goal in the presence of an adversarial environment. However,
qualitative synthesis only produces one controller out of many possible solutions
and typically does not provide support for expressing preferences over other
alternatives.
Synthesis and planning techniques that allow expressing preferences exist,
such as those regarding performance or reliability. Such quality attributes are
modelled by introducing a quantitative aspect to the system specification, which
imposes a preference order on the controllers that satisfy the qualitative part of
the specification. However, from a practical perspective, these approaches require
modelling quality attributes quantitatively, whereas in many cases, such detailed
representation is not available, possible, or desired.
The main objective of this thesis is to present a formal approach to reason
about preferences qualitatively, restricting attention to makespan of discrete
event-based controllers for safety and reachability goals. Time is reasoned upon
symbolically, which relieves the user from providing concrete quantitative measures.
In particular, we study the scenario in which durations of individual activities are
not known up-front.
First, we show how controllers can be symbolically and fairly compared by
fixing the contingencies. Then, we present an algorithm to produce controllers that
are makespan-minimising. The algorithm was implemented in the MTSA tool, as
well as evaluated in case studies.

## Installation 

The version of the MTSA Tool used in this work, it's available a [branch](https://bitbucket.org/lnahabedian/mtsa/src/symbolicLatencyAlgorithm/) of the MTSA's repository. 

MTSA can be installed by following the steps suggested in its [wiki](https://bitbucket.org/lnahabedian/mtsa/wiki/devs/devs). 

```
git clone https://bitbucket.org/lnahabedian/mtsa.git
cd mtsa
git switch symbolicLatencyAlgorithm
mvn clean
mvn install
mvn exec:java
```

This version of the tool also requires installing Z3 SMT-Solver. 

```
git clone https://github.com/Z3Prover/z3.git
cd z3
python scripts/mk_make.py --java 
cd build;make
sudo make install
