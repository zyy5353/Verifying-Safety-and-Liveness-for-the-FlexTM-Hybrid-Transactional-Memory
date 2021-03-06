# Ocamal Programs for the Reserach Project of Verifying Transactional Memories
This folder includes the automomata models implemented for the paper [*Verifying Safety and Liveness for the FlexTM Hybrid Transactional Memory*](http://user.it.uu.se/~yunzh803/date_2013.pdf) [[1]](#references) published at the conference [DATE 2013](https://www.date-conference.com/date13/) (author names are ordered alphabetically). The models are implemented in the functional programming language [Ocaml](https://ocaml.org/learn/description.html). 

There are six programs in all, each of which is implemented in the form of an automaton. Every automaton models the system of the FlexTM transactional memory (TM) [[2]](#references), or the general TM [[3]](#references), with different variations.

The outputs of a program include: 

    1) the list of the final states of the automaton; 
    2) the list of all states of the automaton;  	
    3) the list of all transitions of the automaton.  

In each model, there are 
    
    1) two variables; 
    2) two threads;  
    3) either one or two cache lines.

The languages of the FlexTM automata are  included by the languages of the general TM automata. This means that all the behaviours of FlexTM are good, given that the general TM characterizes all the good behaviors. The results are shown in the paper [[1]](#references).

****************************************************************************************************************************

Introduction of the models represented by the programs: 

(1) *abort_consistency_non_tx_reference.ml:* the TM which satisfies abort consistency in general cases, and includes non-transactional instructions

(2) *strict_serializability_non_tx_reference.ml:* the TM which satisfies strict serializability in general cases, and includes non-transactional instructions

(3) *flextm_eager_one_cache_line.ml:* the FlexTM in eager transactional mode, where both variables are on the same cache line and includes non-transactional instructions

(4) *flextm_eager_two_cache_line.ml:* the FlexTM in eager transactional mode, where there are two cache lines, with one variable on each of them and includes non-transactional instructions

(5) *flextm_lazy_one_cache_line.ml:* the FlexTM in lazy transactional mode (i.e., the commit is non-atomic), where both variables are on the same cache line and includes non-transactional instructions

(6) *flextm_lazy_two_cache_line.ml:* the FlexTM in lazy transactional mode (i.e., the commit is non-atomic), where there are two cache lines, with one variable on each of them and includes non-transactional instructions

****************************************************************************************************************************

The models are implemented with [Ocaml](https://ocaml.org/learn/description.html), an open source functional programming language. Detailed description of how to understand and use the language can be found in the [lecture notes](https://caml.inria.fr/pub/docs/u3-ocaml/index.html) and the [user manual](http://caml.inria.fr/pub/docs/manual-ocaml/). It is available for [installation](https://ocaml.org).

****************************************************************************************************************************
## References

[1] P. A. Abdulla, S. Dwarkadas, A. Rezine, A. Shriraman, and Y. Zhu, “Verifying safety and liveness for the FlexTm hybrid transactional memory,” in DATE 13. EDA Consortium San Jose, CA, USA / ACM DL, 2013, pp. 785–790. 

[2] A. Shriraman, S. Dwarkadas, and M. L. Scott, “Flexible decoupled transactional memory support,” in ISCA. IEEE, 2008, pp. 139–150. 

[3] R. Guerraoui, T. A. Henzinger, B. Jobstmann, and V. Singh, “Model checking transactional memories,” in PLDI. ACM, 2008, pp. 372–382. 

