# DTQW_General_Coin
In this repository we explain how to use a general coin for a Unitary Coined Discrete-Time Quantum Walk (UC-DTQW) and provide an Qiskit simulation with an example

Given a general shift operator $S$ (could be any unitary operator acting on a bipartite quantum system), the evolution operator of a unitary coined quantum walk can be completed by choosing a general coin of the form

$\mathcal{C} = \sum \limits_{k=0}^{n-1} C_{k} \otimes |v_k\rangle \langle v_k|$

where all operators $C_k$ are unitary of size $m \times m$. 

This is represented in the following figure:

<img src="https://github.com/allanwing-qc/DTQW_General_Coin/blob/main/General_Coin_Circuit.jpg?raw=true" width="400" height="200">

In this circuit, we consider the white dots as 0's and the black dots as 1's, in such a way that we can see the sequence of white and black dots as binary code, where the less significant bit is given by the uppermost dot. Each operator $C_i$ acts only on the position state $|v_k\rangle$ whose index $k$ matches the binary representation of the sequence of white and black dots.

Furthermore, if all operators $C_k$ are the same, we obtain the usual form of the coin operator, i.e.

$\mathcal{C} = C \otimes I$

As in the following figure:

<img src="https://github.com/allanwing-qc/DTQW_General_Coin/blob/main/Reduction_to_usual_coin.jpg?raw=true" width="400" height="200">

Graph_K4_General_Coin.ipynb contains Qiskit simulations comparing the UC-DTQW on a complete graph using the regular form of the Hamard coin operator, and a generalizaed coin which acts as a Hadamard operator on nodes 1 and 3, and as the $\sqrt{x}^{\dagger}$ operator on nodes 0 and 2.
