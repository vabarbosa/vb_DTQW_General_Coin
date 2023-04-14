# DTQW_General_Coin
In this repository we explain how to use a general coin for a DTQW and provide an Qiskit simulation with an example

Given a general shift operator $S$, associated to a graph $\mathcal{G}$ as described in Theorem 1, the evolution operator of a coined quantum walk can be completed by choosing a general coin of the form

$\mathcal{C} = \sum \limits_{k=0}^{n-1} C_{k} \otimes |v_k\rangle \langle v_k|$

where all operators $C_k$ are unitary of size $m \times m$. 

Furthermore, if all operators $C_k$ are the same, we obtain the usual form of the coin operator, i.e.

$\mathcal{C} = C \otimes I$
