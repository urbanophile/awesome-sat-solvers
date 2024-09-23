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

- Basic interactive tutorial on a SAT, DPLL, and CDCL - https://cse442-17f.github.io/Conflict-Driven-Clause-Learning/
- MiniZinc tutorial - takes you through solving combinatorial optimisation problems with MiniZinc - https://docs.minizinc.dev/en/stable/part_2_tutorial.html
- Tutorial introduction to Z3 in Python  - https://theory.stanford.edu/~nikolaj/programmingz3.html
- Modern SAT solvers: fast, neat and underused (part 1 of N) - https://codingnest.com/modern-sat-solvers-fast-neat-underused-part-1-of-n/
- SAT/SMT school https://www.satassociation.org/sat-smt-school.html
- SAT tutorials  https://www.satassociation.org/tutorials.html

## Books 

- The Calculus of Computations - covers the logic theory background - https://theory.stanford.edu/~arbrad/book.html
- Decision Procedures: An Algorithmic Point of View http://www.decision-procedures.org/
- SAT/SMT by Example (free! available online!) https://smt.st/SAT_SMT_by_example.pdf 
- Donald Knuth TAOCP 7.2.2.2. Satisfiability (available online) (https://www.inf.ufrgs.br/~mrpritt/lib/exe/fetch.php?media=inf5504:7.2.2.2-satisfiability.pdf)
- Handbook of Satisfiability (comprehensive and very useful)
  -  CH 1  A History of Satisfiability https://satassociation.org/articles/FAIA185-0003.pdf
  -  CH 2 CNF Encodings https://www.researchgate.net/profile/Steven-Prestwich/publication/242029085_CNF_encodings/links/5bcf17e992851c1816ba9092/CNF-encodings.pdf
  -  CH 3 Complete Algorithms https://ics.uci.edu/~dechter/courses/SATChapter3.pdf
  -  CH 4 Conflict-Driven Clause Learning SAT Solvers https://www.satassociation.org/articles/FAIA185-0131.pdf
  -  CH 14 Bound Model Checking  https://www.satassociation.org/articles/FAIA185-0457.pdf

## Solvers
SAT has a nice tradition of making solver public and open source. As Yogi Berra said "You can observe a lot by watchin". Three very important whose source code is informative to read are GRASP, Chaff and MiniSAT. 

### SAT Solvers
- GRASP (1996) -  GRASP pioneered the modern approach of CDCL. 
  - code: https://github.com/satmuseum/grasp
  - paper: https://www.cs.cmu.edu/~emc/15-820A/reading/grasp_iccad96.pdf
- Chaff (2001) - Chaff introduced important data structures and heuristics.
  - code: http://www.princeton.edu/~chaff/zchaff.html
  - paper: https://www.princeton.edu/~chaff/publication/DAC2001v56.pdf
- MiniSAT(2003) - Famous for being good, short (2k LOC), and introducing incremental SAT, MiniSAT is still widely used.
  - code: https://github.com/niklasso/minisat
  - paper: http://minisat.se/downloads/MiniSat.pdf (Clear and worth reading!) 
- CryptoMiniSAT (2009) - CryptoMiniSAT 
  - code: https://github.com/msoos/cryptominisat
  - paper: https://www.msoos.org/wordpress/wp-content/uploads/2011/03/Extending_SAT_2009.pdf
- Glucose (2009)
  - code: https://github.com/audemard/glucose
  - paper: https://univ-artois.hal.science/hal-03299473/file/preprint.pdf
- Lingeling (2010) https://fmv.jku.at/lingeling/
- PicoSAT (2010) https://fmv.jku.at/picosat/
- Slime - https://github.com/maxtuno/slime-sat-solver/
- MergeSAT (2021) https://github.com/conp-solutions/mergesat
- CaDiCaL (2024) https://github.com/arminbiere/cadical

  
### SMT Solvers
SMT solvers are generally built on top of SAT solvers and solver more complex problems. 
- Z3 https://github.com/Z3Prover/z3
- cvc5 https://cvc5.github.io/
- Bitwuzla (successor to Boolector) https://github.com/bitwuzla/bitwuzla

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

## Research
Overviews

- The Silent (R)evolution of SAT - https://cacm.acm.org/research/the-silent-revolution-of-sat/

### Data structures

### Encoding Problems in SAT

- Successful SAT encoding techniques  https://content.iospress.com/download/journal-on-satisfiability-boolean-modeling-and-computation/sat190085?id=journal-on-satisfiability-boolean-modeling-and-computation%2Fsat190085
- Arithmetic operations https://yurichev.com/mirrors/SAT_factor/Encoding%20Basic%20Arithmetic%20Operations%20for%20SAT-Solvers.pdf

### Heuristics 

### CSP
- CSP modelling -  https://www.gecode.org/doc-latest/MPG.pdf
- intro to CSP theory (Constraint Propagation - Models, Techniques, Implementation)  - https://www.gecode.org/papers/Tack_PhD_2009.pdf

###  Related Areas

- [MaxSAT](https://en.wikipedia.org/wiki/Maximum_satisfiability_problem) 
- [Quantified Boolean Formula (QBF)](https://en.wikipedia.org/wiki/True_quantified_Boolean_formula)
- [Constraint Satisfaction Problems (CSP)](https://en.wikipedia.org/wiki/Constraint_satisfaction_problem)
- [Integer Programming (IP/ILP/MILP)](https://en.wikipedia.org/wiki/Integer_programming)

## Courses 

- Constraint Satisfaction https://www.coursera.org/learn/basic-modeling

## Competitions
- SAT Competition https://satcompetition.github.io/
- MiniZinc Competition https://www.minizinc.org/challenge/2023/results/
- LP/CP programming contest https://lpcp-contest.github.io/
- MaxSAT competition https://maxsat-evaluations.github.io/
- Model count competition  https://mccompetition.org/
- QBF competition (more irregular) https://qbf23.pages.sai.jku.at/gallery/

  ## Other

  - DIMACS file format - https://jix.github.io/varisat/manual/0.2.0/formats/dimacs.html
  - SAT association - https://www.satassociation.org/
