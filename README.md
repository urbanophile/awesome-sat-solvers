# Awesome SAT solvers [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome) 


This is a curated collection of resources for the Boolean Satisfiability Problem (SAT), one of the most famous problems in computer science. It also cover related problems and software like Satisfiability Modulo Theory (SMT) solvers and Constraint Satisfaction Problem (CSP) solvers 

## Contents

- [Tutorials](#tutorials)
- [Books](#books)
- [SAT Solvers](#sat-solvers)
- [Other Solvers](#other-solvers)
- [Libraries](#software)
- [Handbook of SAT](#handbook)
- [Research](#research)
- [Courses and Lectures](#courses)
- [Competitions](#competitions)
- [Other Resources](#other)


## Tutorials 

- [Conflict Driven Clause Learning](https://cse442-17f.github.io/Conflict-Driven-Clause-Learning/) - Basic interactive tutorial on a SAT, DPLL, and CDCL
- [Tutorial introduction to Z3 in Python](https://theory.stanford.edu/~nikolaj/programmingz3.html)  - Short intro to using the z3 python bindings
- [Modern SAT solvers: fast, neat and underused (part 1 of N)](https://codingnest.com/modern-sat-solvers-fast-neat-underused-part-1-of-n/) - Popular blog series introducing SAT
- [SAT/SMT school from SAT association](https://www.satassociation.org/sat-smt-school.html)  - Links to many of the old summer schools from the SAT association with introductory material
- [SAT tutorials from SAT association](https://www.satassociation.org/tutorials.html) - Links to academic books and tutorials on SAT 
- [LogicNG tutorial](https://logicng.org/tutorial/) - Uses the Java LogicNG library to solve SAT problems, includes a general introduction to SAT.
- [Simons Workshop SAT bootcamp](https://simons.berkeley.edu/workshops/satisfiability-theory-practice-beyond-boot-camp/schedule#simons-tabs) - Workshop from 2021 which has introductory lectures to modern SAT solving
- [Theoretical Foundations of Applied SAT Solving](https://www.birs.ca/events/2014/5-day-workshops/14w5101) - Workshop from 2014 with many useful videos.
- [MiniZinc tutorial](https://docs.minizinc.dev/en/stable/part_2_tutorial.html) - An intro to constraint satisfaction taking you through solving combinatorial optimisation problems 

## Books 

- [The Calculus of Computations](https://theory.stanford.edu/~arbrad/book.html) - covers the logic theory background
- [Decision Procedures: An Algorithmic Point of View](http://www.decision-procedures.org/) - Great, practical book focusing on the algorithms of SAT and SMT. Strongly recommended.
- [SAT/SMT by Example](https://smt.st/SAT_SMT_by_example.pdf) - free pdf available online! - An excellent problem-based introduction to SAT and SMT. 
- [The Art of Computer Programming - Satisfiability](https://www.inf.ufrgs.br/~mrpritt/lib/exe/fetch.php?media=inf5504:7.2.2.2-satisfiability.pdf) - Preprint available online - Donald Knuth's famous book's section on SAT. 


## SAT Solvers
SAT has a nice tradition of making solver public and open source. As Yogi Berra said "You can observe a lot by watchin". Three very important whose source code is informative to read are GRASP, Chaff and MiniSAT. These are important or (historical) state of the art solvers.

- WalkSAT (1994) - local search - [code](https://gitlab.com/HenryKautz/Walksat) | [project page](https://henrykautz.com/walksat/index.html)
- GRASP (1996) -  GRASP pioneered the modern approach of CDCL. - [code](https://github.com/satmuseum/grasp) | [paper](https://www.cs.cmu.edu/~emc/15-820A/reading/grasp_iccad96.pdf)
- Chaff (2001) - Chaff introduced important data structures and heuristics. - [code](http://www.princeton.edu/~chaff/zchaff.html) | [paper](https://www.princeton.edu/~chaff/publication/DAC2001v56.pdf)
- MiniSAT(2003) - Famous for being good, short (2k LOC), and introducing incremental SAT, MiniSAT is still widely used. Clear and worth reading! [code](https://github.com/niklasso/minisat) |  [paper](http://minisat.se/downloads/MiniSat.pdf) 
- CryptoMiniSAT (2009) - Uses XOR primitive  - [code](https://github.com/msoos/cryptominisat) | [paper](https://www.msoos.org/wordpress/wp-content/uploads/2011/03/Extending_SAT_2009.pdf)
- Glucose (2009) -  Introduced different heuristics for SAT and UNSAT - [code](https://github.com/audemard/glucose) | [paper](https://univ-artois.hal.science/hal-03299473/file/preprint.pdf)
- Lingeling (2010) - [website](https://fmv.jku.at/lingeling/)
- PicoSAT (2010) - [website](https://fmv.jku.at/picosat/)
- Kissat (2020) - -  [code](https://github.com/arminbiere/kissat)
- Slime (2021) - [code](https://github.com/maxtuno/slime-sat-solver/)
- MergeSAT (2021) - [code](https://github.com/conp-solutions/mergesat)
- CaDiCaL (2024) - [code](https://github.com/arminbiere/cadical)

Other solvers of interest:

- [Satch](https://github.com/arminbiere/satch) - expository solver by Armin Biere
- [gopher](https://github.com/crillab/gophersat) - solver written in Go
- [varisat](https://github.com/jix/varisat) - solver written in Rust

### Analyses of SAT Solver Performance

- The SAT Museum - [paper](https://ceur-ws.org/Vol-3545/paper6.pdf)
- Assessing Progress in SAT Solvers Through the Lens of Incremental SAT - [paper](https://alexeyignatiev.github.io/assets/pdf/kims-sat21-preprint.pdf)
- SAT: Disruption, Demise & Resurgence - [paper](http://www.pragmaticsofssat.org/2019/disruption.pdf)
- A case for simple SAT solvers - [paper](https://users.cecs.anu.edu.au/~jinbo/07-cp.pdf)
- Anatomy and empirical evaluation of modern SAT solvers [paper]()

### Core concepts

- DPLL -  Davis–Putnam–Logemann–Loveland (DPLL) algorithm is the historic basis for modern solvers - [wiki](https://en.wikipedia.org/wiki/DPLL_algorithm)
- CDCL - Conflict-driven Clause learning the contemporary extension of DPLL - [wiki](https://en.wikipedia.org/wiki/Conflict-driven_clause_learning)
- Implication graph - a key construction used to find conflict clauses -  [wiki](https://en.wikipedia.org/wiki/Implication_graph)
- Unit propagation - a.k.a. Boolean constraint propagation, a rule for simplifying formulas [wiki](https://en.wikipedia.org/wiki/Unit_propagation) - see also ["An Efficient Algorithm for Unit Propagation"](https://www.researchgate.net/publication/2508830_An_Efficient_Algorithm_for_Unit_Propagation)
- backjumping - Efficient backtracking is one of the main differences between DPLL and CDCL - [wiki](https://en.wikipedia.org/wiki/Backjumping)
- SAT heuristics - Heuristics are essential to modern SAT solvers. [wiki](https://en.wikipedia.org/wiki/Boolean_satisfiability_algorithm_heuristics)


## Other Solvers 

There many theoretical problems which are closely related to SAT. Solvers for the following adjacent problems are worth knowing about:

- MaxSAT, #SAT and QBF are all progressively harder generalisations of SAT
- SMT extends the SAT problem with soluble theories.
- CSP and Integer programming are alternate approaches to solving NP-hard problems  

### MaxSAT Solvers

MaxSAT is the problem of the finding the maximum number of clauses which can be satisfied for a particular formula
- [MaxSAT](https://en.wikipedia.org/wiki/Maximum_satisfiability_problem)

Minimally Unsatisfiable Subformulas are like duals MaxSAT, they ask for the minimal set of assignments which will show a formula is unsatisfiable.


- [Loandra](https://github.com/jezberg/loandra) (MaxSAT)
- [MUSer](https://github.com/meelgroup/muser) (MUSer)

### SharpSAT Solvers

The #SAT is the problem of counting all the assignments which satisfy a Boolean formula.
- [#SAT](https://en.wikipedia.org/wiki/Sharp-SAT)

Solvers include:

- [ApproxMCv6](https://github.com/meelgroup/approxmc) (by creators of CryptoMiniSAT)
- [SharpSAT](https://github.com/marcthurley/sharpSAT) (sota circa 2011)

### QBF solvers
- [Quantified Boolean Formula (QBF)](https://en.wikipedia.org/wiki/True_quantified_Boolean_formula)

solver
- CAQE - Solver is based on CEGAR not CDCL -  [code](https://github.com/ltentrup/caqe)
- DepQBF - Based on an extension of CDCL - [code](https://lonsing.github.io/depqbf/)

  
### SMT Solvers
SMT solvers are generally built on top of SAT solvers and solver more complex problems. 
- [Z3](https://github.com/Z3Prover/z3)
- [cvc5](https://cvc5.github.io/)
- [Bitwuzla](https://github.com/bitwuzla/bitwuzla) (successor to Boolector) 

### CSP Solvers
CSP solvers differ from SAT solvers but the communities overlap, and techniques from CSP have proven very important in SAT e.g. Boolean Constraint Propagation.
- [Constraint Satisfaction Problems (CSP)](https://en.wikipedia.org/wiki/Constraint_satisfaction_problem)
- [CSP modelling](https://www.gecode.org/doc-latest/MPG.pdf)
- [ (Constraint Propagation - Models, Techniques, Implementation)](https://www.gecode.org/papers/Tack_PhD_2009.pdf)  - intro to CSP theory


CSP solvers include:

- [GeCode](https://www.gecode.org/) - C++ based - good documentation and overview of the code
- [Sugar](https://cspsat.gitlab.io/sugar/) - Solving by reduction to SAT -  
- [Picat](http://picat-lang.org/) - logic programming-based
- [Choco](https://choco-solver.org/) - Java-based
- [OptaPlanner](https://www.optaplanner.org/) - Java-based



### Integer Programming Solvers

- [Pseudo-boolean Constraints](https://jakobnordstrom.se/docs/presentations/TalkPseudoBooleanSolvingSimons2103.pdf)
- [Integer Programming (IP/ILP/MILP)](https://en.wikipedia.org/wiki/Integer_programming)
- [Branch-and-bound algorithms: A survey of recent advances in searching, branching, and pruning](https://www.sciencedirect.com/science/article/pii/S1572528616000062)

Solvers include:

- CBC [code](https://github.com/coin-or/Cbc)
- SCIP [project](https://scipopt.org/)

## Software
Besides solvers, there are many other pieces of helpful software for solving SAT and related problems. 

Many complex problems can be solved by compiling the problem into a SAT encoding. Examples of domain problems which can be solved by reduction include planning problems (SATPLAN), automated theorem proving (via SMT), and formal verification (by bounded model checking). 

### Libraries

- PySAT (Python) - wrapper library  [website](https://pysathq.github.io/)
- Sat4j (Java) - modelling and wrapper for Java -  [website](http://www.sat4j.org/)
- ORTools (Python) -  general purpose modelling library for optimisation problems but very good as CSP - [website](https://developers.google.com/optimization/cp/cp_solver)

### High Level Modelling Languages 

- MiniZinc (Optimisation) [project](https://www.minizinc.org/)
- Alloy (Software verification) [project](https://alloytools.org/)

### Verification of proofs

- [DRAT-Trim](https://github.com/marijnheule/drat-trim) - verifier of proofs of unsatisfiability (UNSAT)

## Handbook
The handbook of SAT is an excellent and comprehensive resources. 

- Handbook of Satisfiability (comprehensive and very useful)
  -  [CH 1 A History of Satisfiability](https://satassociation.org/articles/FAIA185-0003.pdf)
  -  [CH 2 CNF Encodings](https://www.researchgate.net/profile/Steven-Prestwich/publication/242029085_CNF_encodings/links/5bcf17e992851c1816ba9092/CNF-encodings.pdf)
  -  [CH 3 Complete Algorithms](https://ics.uci.edu/~dechter/courses/SATChapter3.pdf)
  -  [CH 4 Conflict-Driven Clause Learning SAT Solvers](https://www.satassociation.org/articles/FAIA185-0131.pdf)
  -  [CH 5 Look-Ahead Based SAT Solvers (1st Ed.) ](https://www.cs.cmu.edu/~mheule/publications/p01c05_lah.pdf)
  -  [CH 6 Incomplete Algorithms](https://www.cs.cornell.edu/~sabhar/chapters/IncompleteAlg-SAT-Handbook-prelim.pdf)
  -  [CH 7 Proof Complexity and SAT Solving](https://jakobnordstrom.se/docs/publications/ProofComplexityChapter.pdf)
  -  [CH 8 Fundaments of Branching Heuristics](https://citeseerx.ist.psu.edu/document?repid=rep1&type=pdf&doi=027282e993a97cad07797a980c32b0bc83f61989)
  -  [CH 9 Preprocessing in SAT Solving  (2nd Ed.)](https://cca.informatik.uni-freiburg.de/papers/BiereJarvisaloKiesl-SAT-Handbook-2021-Preprocessing-Chapter-Manuscript.pdf)
  -  [CH 10 Random Satisfiability (2nd Ed.)](https://cgi.di.uoa.gr/~optas/papers/handbook.pdf)
  -  [CH 14 Bound Model Checking (1st Ed.)](https://www.satassociation.org/articles/FAIA185-0457.pdf)
  -  [CH 15 Proofs of Unsatisfiability (2nd Ed.)](https://www.cs.cmu.edu/~mheule/publications/p01c15-prf.pdf) 
  -  [CH 23 MaxSAT, Hard and Soft Constraints (2nd Ed.)](https://www.iiia.csic.es/media/filer_public/eb/1c/eb1c1fff-ecb8-4279-aa51-810cb5f3dbc8/p02c23-max.pdf)
  -  [CH 19 Planning and SAT](https://users.aalto.fi/~rintanj1/papers/p02c19-pla.pdf)
  -  [CH -2 SMT (1st Ed.)](https://homepage.cs.uiowa.edu/~tinelli/papers/BarSST-09.pdf)

## Research
Overviews and reviews.

- [The Silent (R)evolution of SAT](https://cacm.acm.org/research/the-silent-revolution-of-sat/)

### Data structures

Lazy data structures have proven to be very important in SAT solvers. 

- M. Iser and T. Balyo, ‘Unit Propagation with Stable Watches’, 2021. [link](https://publikationen.bibliothek.kit.edu/1000139917)
- I. P. Gent, ‘Optimal Implementation of Watched Literals and More General Techniques’, Journal of Artificial Intelligence Research, vol. 48, pp. 231–252, Oct. 2013, doi: 10.1613/jair.4016. [link](https://www.jair.org/index.php/jair/article/view/10839)

[more info](https://cs.stackexchange.com/questions/150557/what-are-efficient-approaches-to-implement-unit-propagation-in-dpll-based-sat-so)

### Encoding Problems in SAT

- Successful SAT encoding techniques  [paper](https://content.iospress.com/download/journal-on-satisfiability-boolean-modeling-and-computation/sat190085?id=journal-on-satisfiability-boolean-modeling-and-computation%2Fsat190085)
- Arithmetic operations [paper](https://yurichev.com/mirrors/SAT_factor/Encoding%20Basic%20Arithmetic%20Operations%20for%20SAT-Solvers.pdf)

### Heuristics 

Heuristics around choosing variables which variables and which assignments to make are an extremely improtant part of SAT Solvers
Important heuristics include:

- Variable State Independent Decaying Sum (VSAID) introduced in Chaff
- Clause-move-to-front introduced by HAIFASAT

### Theoretical Complexity
SAT raises some interesting questions because even though it is the canonical NP-complete problem, practical problems can often be solved in close to linear time. 
[Relating Proof Complexity Measures and Practical Hardness of SAT](https://jakobnordstrom.se/docs/publications/JMNZ12RelatingProofCplx.pdf)

### Parallelisation
SAT is tricky to parallelise, but the cube-and-conquer method has been very popular. 

- Cube and Conquer: Guiding CDCL SAT Solvers by Lookaheads [paper](https://www.cs.utexas.edu/~marijn/publications/cube.pdf)


### Machine Learning 

Machine learning is a related branch of AI and theorem proving. The overlap is mostly in the direction of applying machine learning methods to help SAT solvers e.g.

- SATzilla: Portfolio-based Algorithm Selection for SAT. Journal of Artificial Intelligence Research 32 (2008) 565-606. [paper](https://arxiv.org/abs/1111.2249)
- Machine Learning for Automated Theorem Proving - A survey of recent work [paper](https://ieeexplore.ieee.org/document/9624176)

### Problems

- [‘SATLIB - Benchmark Problems’](https://www.cs.ubc.ca/~hoos/SATLIB/benchm.html)

## Courses 


- [Constraint Satisfaction](https://www.coursera.org/learn/basic-modeling) @Monash via Coursera
- [Bug Catching: Automated Program Verification](https://www.cs.cmu.edu/~15414/f17/syllabus.html)

## Competitions

- SAT Competition [link](https://satcompetition.github.io/)
- MiniZinc Competition [link](https://www.minizinc.org/challenge/2023/results/)
- LP/CP programming contest [link](https://lpcp-contest.github.io/)
- MaxSAT competition [link](https://maxsat-evaluations.github.io/)
- Model count competition  [link](https://mccompetition.org/)
- QBF competition (more irregular) [link](https://qbf23.pages.sai.jku.at/gallery/)
- Other research competitions [link](https://www.hsu-hh.de/logistik/research/challenges)

## Other

  - DIMACS file format - [website](https://jix.github.io/varisat/manual/0.2.0/formats/dimacs.html)
  - SAT association - [website](https://www.satassociation.org/)
  - Simons Institute Workshops (2021, 2023) [website](https://simons.berkeley.edu/workshops/satisfiability-theory-practice-beyond)

