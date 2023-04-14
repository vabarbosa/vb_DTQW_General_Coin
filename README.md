# DTQW_General_Coin
In this repository we explain how to use a general coin for a DTQW and provide an Qiskit simulation with an example

Given a general shift operator $S$ (could be any unitary operator acting on a bipartite quantum system), the evolution operator of a unitary coined quantum walk can be completed by choosing a general coin of the form

$\mathcal{C} = \sum \limits_{k=0}^{n-1} C_{k} \otimes |v_k\rangle \langle v_k|$

where all operators $C_k$ are unitary of size $m \times m$. 

![github-small](https://github.com/allanwing-qc/DTQW_General_Coin/blob/main/General_Coin_Circuit.jpg?raw=true)


Furthermore, if all operators $C_k$ are the same, we obtain the usual form of the coin operator, i.e.

$\mathcal{C} = C \otimes I$


This is represented in the following picture:

