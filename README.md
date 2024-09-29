# Awesome SAT and SAT solvers [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome) 


This is a curated collection of resources for the Boolean Satisfiability Problem (SAT), one of the most famous problems in computer science. It also cover related problems and software like Satisfiability Modulo Theory (SMT) solvers and Constraint Satisfaction Problem (CSP) solvers 

## Contents

- [Tutorials](#tutorials)
- [Books](#books)
- [Solvers](#solvers)
- [Other Software](#software)
- [Research](#research)
- [Courses and Lectures](#courses)
- [Competitions](#competitions)
- [Other Resources](#other)


## Tutorials 

- [Conflict Driven Clause Learning](https://cse442-17f.github.io/Conflict-Driven-Clause-Learning/) - Basic interactive tutorial on a SAT, DPLL, and CDCL
- [MiniZinc tutorial](https://docs.minizinc.dev/en/stable/part_2_tutorial.html) - takes you through solving combinatorial optimisation problems with MiniZinc
- [Tutorial introduction to Z3 in Python](https://theory.stanford.edu/~nikolaj/programmingz3.html)  - Short intro to using the z3 python bindings
- [Modern SAT solvers: fast, neat and underused (part 1 of N)](https://codingnest.com/modern-sat-solvers-fast-neat-underused-part-1-of-n/) - Popular blog series introducing SAT
- [SAT/SMT school from SAT association](https://www.satassociation.org/sat-smt-school.html) 
- [SAT tutorials from SAT association](https://www.satassociation.org/tutorials.html)
- [LogicNG tutorial](https://logicng.org/tutorial/)
- [Simons Workshop SAT bootcamp](https://simons.berkeley.edu/workshops/satisfiability-theory-practice-beyond-boot-camp/schedule#simons-tabs)
- [Theoretical Foundations of Applied SAT Solving](https://www.birs.ca/events/2014/5-day-workshops/14w5101)  Workshop from 2014 with many useful videos.

## Books 

- [The Calculus of Computations](https://theory.stanford.edu/~arbrad/book.html) - covers the logic theory background
- [Decision Procedures: An Algorithmic Point of View](http://www.decision-procedures.org/) - Great, practical book focusing on the algorithms of SAT and SMT. Strongly recommended.
- [SAT/SMT by Example](https://smt.st/SAT_SMT_by_example.pdf) (free! available online!)  
- [The Art of Computer Programming - Satisfiability](https://www.inf.ufrgs.br/~mrpritt/lib/exe/fetch.php?media=inf5504:7.2.2.2-satisfiability.pdf) (available online) Donald Knuth's famous book's section on SAT. 
- Handbook of Satisfiability (comprehensive and very useful)
  -  [CH 1 A History of Satisfiability](https://satassociation.org/articles/FAIA185-0003.pdf)
  -  [CH 2 CNF Encodings](https://www.researchgate.net/profile/Steven-Prestwich/publication/242029085_CNF_encodings/links/5bcf17e992851c1816ba9092/CNF-encodings.pdf)
  -  [CH 3 Complete Algorithms](https://ics.uci.edu/~dechter/courses/SATChapter3.pdf)
  -  [CH 4 Conflict-Driven Clause Learning SAT Solvers](https://www.satassociation.org/articles/FAIA185-0131.pdf)
  -  [CH 5 Look-Ahead Based SAT Solvers (1st Ed.) ](https://www.cs.cmu.edu/~mheule/publications/p01c05_lah.pdf)
  -  [CH 6 Incomplete Algorithms](https://www.cs.cornell.edu/~sabhar/chapters/IncompleteAlg-SAT-Handbook-prelim.pdf)
  -  [CH 9 Preprocessing in SAT Solving  (2nd Ed.)](https://cca.informatik.uni-freiburg.de/papers/BiereJarvisaloKiesl-SAT-Handbook-2021-Preprocessing-Chapter-Manuscript.pdf)
  -  [CH 14 Bound Model Checking](https://www.satassociation.org/articles/FAIA185-0457.pdf)

## Solvers
SAT has a nice tradition of making solver public and open source. As Yogi Berra said "You can observe a lot by watchin". Three very important whose source code is informative to read are GRASP, Chaff and MiniSAT. 

### SAT Solvers
- WalkSAT (1994) local search [code](https://gitlab.com/HenryKautz/Walksat) [project page](https://henrykautz.com/walksat/index.html)
- GRASP (1996) -  GRASP pioneered the modern approach of CDCL. 
  - [code](https://github.com/satmuseum/grasp)
  - [paper](https://www.cs.cmu.edu/~emc/15-820A/reading/grasp_iccad96.pdf)
- Chaff (2001) - Chaff introduced important data structures and heuristics.
  - [code](http://www.princeton.edu/~chaff/zchaff.html)
  - [paper](https://www.princeton.edu/~chaff/publication/DAC2001v56.pdf)
- MiniSAT(2003) - Famous for being good, short (2k LOC), and introducing incremental SAT, MiniSAT is still widely used.
  - [code](https://github.com/niklasso/minisat)
  - [paper](http://minisat.se/downloads/MiniSat.pdf) (Clear and worth reading!) 
- CryptoMiniSAT (2009) - CryptoMiniSAT 
  - code: https://github.com/msoos/cryptominisat
  - paper: https://www.msoos.org/wordpress/wp-content/uploads/2011/03/Extending_SAT_2009.pdf
- Glucose (2009). Introduced different heuristics for SAT and UNSAT.
  - code: https://github.com/audemard/glucose
  - paper: https://univ-artois.hal.science/hal-03299473/file/preprint.pdf
- Lingeling (2010) https://fmv.jku.at/lingeling/
- PicoSAT (2010) https://fmv.jku.at/picosat/
- Slime - https://github.com/maxtuno/slime-sat-solver/
- MergeSAT (2021) https://github.com/conp-solutions/mergesat
- CaDiCaL (2024) https://github.com/arminbiere/cadical
- Kissat (2020) https://github.com/arminbiere/kissat

- Satch (expository) https://github.com/arminbiere/satch

### Analyses of SAT Solver Performance

- The SAT Museum - https://ceur-ws.org/Vol-3545/paper6.pdf
- Assessing Progress in SAT Solvers Through the Lens of Incremental SAT https://alexeyignatiev.github.io/assets/pdf/kims-sat21-preprint.pdf
- SAT: Disruption, Demise & Resurgence http://www.pragmaticsofssat.org/2019/disruption.pdf
- A case for simple SAT solvers https://users.cecs.anu.edu.au/~jinbo/07-cp.pdf
- Anatomy and empirical evaluation of modern SAT solvers

### Core concepts

- DPLL 
- CDCL
- Clause Learning 
- Unit propagation "An Efficient Algorithm for Unit Propagation"



### MaxSAT Solvers and MUS Extracters 

MaxSAT is the problem of the finding the maximum number of clauses which can be satisfied for a particular formula
Minimally Unsatisfiable Subformulas are like duals MaxSAT, they ask for the minimal set of assignments which will show a formula is unsatisfiable.


- [Loandra](https://github.com/jezberg/loandra) (MaxSAT)
- [MUSer](https://github.com/meelgroup/muser) (MUSer)

### SharpSAT (#SAT) Solvers

The #SAT is the problem of counting all the assignments which satisfy a Boolean formula.

- [ApproxMCv6](https://github.com/meelgroup/approxmc) (by creators of CryptoMiniSAT)
- [SharpSAT](https://github.com/marcthurley/sharpSAT) (sota circa 2011)

  
### SMT Solvers
SMT solvers are generally built on top of SAT solvers and solver more complex problems. 
- [Z3](https://github.com/Z3Prover/z3)
- [cvc5](https://cvc5.github.io/)
- [Bitwuzla](https://github.com/bitwuzla/bitwuzla) (successor to Boolector) 

### CSP Solvers
CSP solvers differ from SAT solvers but the communities overlap, and techniques from CSP have proven very important in SAT e.g. Boolean Constraint Propagation.

- GeCode - C++ based - good documentation and overview of the code - https://www.gecode.org/
- Sugar - Solving by reduction to SAT -  https://cspsat.gitlab.io/sugar/
- Picat - logic programming-based - http://picat-lang.org/
- Choco - Java-based - https://choco-solver.org/
- OptaPlanner - Java-based - https://www.optaplanner.org/




## Software
### Libraries

- PySAT (Python) https://pysathq.github.io/
- Sat4j (Java) http://www.sat4j.org/

### High Level Modelling Languages 

- MiniZinc (Optimisation) https://www.minizinc.org/
- Alloy (Software verification) https://alloytools.org/
- ORTools (Optimisation) https://developers.google.com/optimization/cp/cp_solver

### Verification of proofs

- [DRAT-Trim](https://github.com/marijnheule/drat-trim) - verifier of proofs of unsatisfiability (UNSAT)


## Research
Overviews

- The Silent (R)evolution of SAT - https://cacm.acm.org/research/the-silent-revolution-of-sat/

### Data structures

Lazy data structures have proven to be very important in SAT solvers. 

- M. Iser and T. Balyo, ‘Unit Propagation with Stable Watches’, 2021. https://publikationen.bibliothek.kit.edu/1000139917
- I. P. Gent, ‘Optimal Implementation of Watched Literals and More General Techniques’, Journal of Artificial Intelligence Research, vol. 48, pp. 231–252, Oct. 2013, doi: 10.1613/jair.4016. https://www.jair.org/index.php/jair/article/view/10839

https://cs.stackexchange.com/questions/150557/what-are-efficient-approaches-to-implement-unit-propagation-in-dpll-based-sat-so

### Encoding Problems in SAT

- Successful SAT encoding techniques  https://content.iospress.com/download/journal-on-satisfiability-boolean-modeling-and-computation/sat190085?id=journal-on-satisfiability-boolean-modeling-and-computation%2Fsat190085
- Arithmetic operations https://yurichev.com/mirrors/SAT_factor/Encoding%20Basic%20Arithmetic%20Operations%20for%20SAT-Solvers.pdf

### Heuristics 

### Computational Complexity

### Logic and Proof Complexity

Relating Proof Complexity Measures and Practical Hardness of SAT https://jakobnordstrom.se/docs/publications/JMNZ12RelatingProofCplx.pdf

### Parallelisation

- cube-and-conquer https://www.cs.utexas.edu/~marijn/publications/cube.pdf

### Problems

- ‘SATLIB - Benchmark Problems’. https://www.cs.ubc.ca/~hoos/SATLIB/benchm.html




##  Related Areas

### Next Door
- [MaxSAT](https://en.wikipedia.org/wiki/Maximum_satisfiability_problem)
- [#SAT](https://en.wikipedia.org/wiki/Sharp-SAT)
- [Pseudo-boolean Constraints](https://jakobnordstrom.se/docs/presentations/TalkPseudoBooleanSolvingSimons2103.pdf) 
- [Quantified Boolean Formula (QBF)](https://en.wikipedia.org/wiki/True_quantified_Boolean_formula)

### Same Neighbourhood
- [Constraint Satisfaction Problems (CSP)](https://en.wikipedia.org/wiki/Constraint_satisfaction_problem)
- [Integer Programming (IP/ILP/MILP)](https://en.wikipedia.org/wiki/Integer_programming)

#### CSP
- CSP modelling -  https://www.gecode.org/doc-latest/MPG.pdf
- intro to CSP theory (Constraint Propagation - Models, Techniques, Implementation)  - https://www.gecode.org/papers/Tack_PhD_2009.pdf


## Courses 


- Constraint Satisfaction https://www.coursera.org/learn/basic-modeling @Monash via Coursera
- Bug Catching: Automated Program Verification  https://www.cs.cmu.edu/~15414/f17/syllabus.html

## Competitions

- SAT Competition https://satcompetition.github.io/
- MiniZinc Competition https://www.minizinc.org/challenge/2023/results/
- LP/CP programming contest https://lpcp-contest.github.io/
- MaxSAT competition https://maxsat-evaluations.github.io/
- Model count competition  https://mccompetition.org/
- QBF competition (more irregular) https://qbf23.pages.sai.jku.at/gallery/
- Other research competitions https://www.hsu-hh.de/logistik/research/challenges

## Other

  - DIMACS file format - https://jix.github.io/varisat/manual/0.2.0/formats/dimacs.html
  - SAT association - https://www.satassociation.org/
  - Simons Institute Workshop (2021, 2023) https://simons.berkeley.edu/workshops/satisfiability-theory-practice-beyond

