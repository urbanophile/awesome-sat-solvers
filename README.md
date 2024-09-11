# Awesome SAT and SAT solvers [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome) 


This is a curated collection of resources for the Boolean Satisfiability Problem (SAT), one of the most famous problems in computer science. It also cover related problems like Satisfiability Modulo Theory (SMT) solvers and Constraint Satisfaction Problem (CSP) solvers 

## Contents

- [Tutorials](#tutorials)
- [Books](#books)
- [Solvers](#solvers)
- [Other Software](#software)
- [Research](#research)
- [Courses and Lectures](#courses)
- [Other Resources](#other)


## Tutorials 

- Basic interactive tutorial on a SAT, DPLL, and CDCL https://cse442-17f.github.io/Conflict-Driven-Clause-Learning/
- MiniZinc tutorial - takes you through solving combinatorial optimisation problems with MiniZinc - https://docs.minizinc.dev/en/stable/part_2_tutorial.html
- Tutorial introduction to Z3 in Python https://theory.stanford.edu/~nikolaj/programmingz3.html

## Books 

- The Calculus of Computations - covers the logic theory background - https://theory.stanford.edu/~arbrad/book.html
- Decision Procedures: An Algorithmic Point of View http://www.decision-procedures.org/
- SAT/SMT by Example (free! available online!) https://smt.st/SAT_SMT_by_example.pdf 
- Donald Knuth TAOCP 7.2.2.2. Satisfiability (available online) (https://www.inf.ufrgs.br/~mrpritt/lib/exe/fetch.php?media=inf5504:7.2.2.2-satisfiability.pdf)

## Solvers
### SAT Solvers
- GRASP (1996)
  - paper: https://www.cs.cmu.edu/~emc/15-820A/reading/grasp_iccad96.pdf
- Chaff (2001)
  - code: http://www.princeton.edu/~chaff/zchaff.html
  - paper: https://www.princeton.edu/~chaff/publication/DAC2001v56.pdf
- MiniSAT(2003) - A very important solver which introduced a number of heuristics 
  - code: https://github.com/niklasso/minisat
  - paper: 
- CryptoMiniSAT (2009)
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

- Z3 https://github.com/Z3Prover/z3
- cvc5 https://cvc5.github.io/
- Bitwuzla (successor to Boolector) https://github.com/bitwuzla/bitwuzla

### CSP Solvers

- GeCode - good documentation and overview of the code - https://www.gecode.org/
- Sugar - Solving by reduction to SAT -  https://cspsat.gitlab.io/sugar/
- Picat - http://picat-lang.org/

## Software
### Libraries

- PySAT (Python) https://pysathq.github.io/
- Sat4j (Java) http://www.sat4j.org/

### High Level Modelling Languages 

- MiniZinc (Optimisation) https://www.minizinc.org/
- Alloy (Software verification) https://alloytools.org/
- ORTools (Optimisation) https://developers.google.com/optimization/cp/cp_solver

## Research

### Encoding Problems in SAT
 
- Arithmetic operations https://yurichev.com/mirrors/SAT_factor/Encoding%20Basic%20Arithmetic%20Operations%20for%20SAT-Solvers.pdf


### CSP
- CSP modelling https://www.gecode.org/doc-latest/MPG.pdf
- intro to CSP theory (Constraint Propagation - Models, Techniques, Implementation) https://www.gecode.org/papers/Tack_PhD_2009.pdf

###  Related Areas

- [MaxSAT](https://en.wikipedia.org/wiki/Maximum_satisfiability_problem) 
- [Quantified Boolean Formula (QBF)](https://en.wikipedia.org/wiki/True_quantified_Boolean_formula)
- [Constraint Satisfaction Problems (CSP)](https://en.wikipedia.org/wiki/Constraint_satisfaction_problem)
- [Integer Programming (IP/ILP/MILP)](https://en.wikipedia.org/wiki/Integer_programming)

## Courses 

- Constraint Satisfaction https://www.coursera.org/learn/basic-modeling

## Other Resources
- SAT Competition https://satcompetition.github.io/
- MiniZinc Competition https://www.minizinc.org/challenge/2023/results/

