
# Classical Computers
Classical computers can't generate true random numbers because they rely on deterministic algorithms and processes. These algorithms use initial values, called seeds, to generate a sequence of numbers that appears random. However, the sequence is deterministic, meaning that if you know the seed and the algorithm, you can predict the entire sequence.

# Quantum Computers
In contrast, quantum computers can generate true random numbers due to the inherent probabilistic nature of quantum mechanics. When a qubit in superposition is measured, the outcome is genuinely random, and there's no way to predict it with certainty. This allows quantum computers to generate truly random numbers, unlike classical computers.

# Visualize the Q# code with the Bloch sphere

In the Bloch sphere, the north pole represents the classical value 0 and the south pole represents the classical value 1. Any superposition can be represented by a point on the sphere (represented by an arrow). The closer the end of the arrow to a pole the higher the probability the qubit collapses into the classical value assigned to that pole when measured. For example, the qubit state represented by the arrow in the following figure has a higher probability of giving the value 0 if you measure it.

<img src="/Assets/Images/qrng-bloch_1.png" width="300" height="300" />

You can use this representation to visualize what the code is doing:

1) First, start with a qubit initialized in the state 0 and apply an H operation to create an equal superposition in which the probabilities for 0 and 1 are the ame.

<img src="/Assets/Images/qrng-h_2.png" width="700" height="300" />

2) Then measure the qubit and save the output:

<img src="/Assets/Images/qrng-meas_3.png" width="700" height="300" />

Since the outcome of the measurement is random and the probabilities of measuring 0 and 1 are the same, you have obtained a completely random bit. You can call this operation several times to create integers. For example, if you call the operation three times to obtain three random bits, you can build random 3-bit numbers (that is, a random number between 0 and 7).


### Source provided by:
https://learn.microsoft.com/en-us/azure/quantum/tutorial-qdk-quantum-random-number-generator?tabs=tabid-vscode