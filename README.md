# DTQW_General_Coin
In this repository we explain how to use a general coin for a Unitary Coined Discrete-Time Quantum Walk (UCDTQW) as proposed in https://arxiv.org/abs/2304.01582, and provide Qiskit simulations with an example

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

Graph_K4_General_Coin.ipynb contains Qiskit simulations comparing the UC-DTQW on a complete graph using the regular form of the Hamard coin operator, and a generalizaed coin which acts as a Hadamard operator on nodes 1 and 3, and as the $\sqrt{x}^{\dagger}$ operator on nodes 0 and 2. The reults of the first six steps fro both cases is shown below: 

Evolution operator of a UCDTQW on a complete graph of four nodes ($\mathcal{K}_4$) using a Hadamard coin as introduced in 
https://doi.org/10.1007/s11128-023-03878-6.

<img src="https://github.com/allanwing-qc/DTQW_General_Coin/blob/main/Fig8a.jpg?raw=true" width="230" height="200">

Here we perform a UCDTQW on the same graph, although using a generalization of the coin operator that acts with the Hadamard coin on nodes 1 and 3 of the graph, and with the 2-qubit $\sqrt{x}^{\dagger}$ operator on nodes 0 and 2.

<img src="https://github.com/allanwing-qc/DTQW_General_Coin/blob/main/Fig8b.jpg?raw=true" width="400" height="200">

Next, we present a Qiskit simulation comparing the distributions of the first 6 steps of both UCDTQWs. The bars corresponding the first and second circuit are to the left (in red) and to the right (in blue) in the histograms. The bitstrings in the x-axes of the histograms correspond to the binary labeling of nodes in $\mathcal{K}_4$. Notice that the distribution of the UCDTQW with the general coin changes drastically with respect to the UC-DTQW with the Hadamard coin after step 2.

<img src="https://github.com/allanwing-qc/DTQW_General_Coin/blob/main/Fig8c.jpg?raw=true" width="800" height="400">




