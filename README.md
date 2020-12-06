# Signature-Verification-using-Enhanced-Quantum-Neural-Network

We have followed the following steps to make this model.
Load raw data.
Preprocess the images.
Resizing of  the images to fit the data in the quantum network.
Remove any contradictory examples.
This is done to filter the dataset to remove images that are labeled as belonging to both classes.
we ran a classical computer as a simulator of a quantum device. For which we used tensorflow quantum and applying following processes 
Convert binary images to Cirq circuits(using cirq library). 
First we create qubits at every indices according to the size of the image.
Our image size is 16*16 so (0,0),(0,1),(0,2)........(15,13),(15,14)(15,15)
We apply XGate circuit  at every indices where value>0.
Converts the Cirq circuits to TensorFlow Quantum circuits. 
Then we add layers using some more random gates to the circuit X, H, ZXX,  HH, ZZ.
After the circuit design we have used Parametrized Quantum Circuit layer, tfq.layers.PQC, to train the   model circuit on the quantum data.

QUANTUM COMPUTING
Quantum computing is the use of quantum phenomena such as superposition and entanglement to perform computation. Computers that perform quantum computations are known as quantum computers. Quantum computers are emerging as a new solution to problems not solved by classical computers. Quantum computers provide a computing environment that is different from classical computers. In particular, quantum computers can use superposition and entanglement, not seen in classical computing environments, and obtain powerful performance using parallelism between qubits (Quantum bits).
Traditional computers operate on binary bits — information processed in the form of ones or zeroes. But quantum computers transmit information via quantum bits, or qubits, which can exist either as one or zero or both simultaneously.
Quantum Bits (Qubits)
Many people define Qubits as though they are very complex, like they exist as both zero and one at the same time however this definition is not completely correct nor it covers the true idea of qubits. This definition is quite an oversimplification of the behavior of Qubits. Let us assume that the state of a Qubit is represented as a position on a sphere, like the Earth. With the two extreme poles namely north pole and south pole being states 1 and 0 respectively. Quantum gates operate as though they are moving it around the globe at any point in time. Quantum gates are similar to logic gates but Quantum gates operate on Qubits. A collection of quantum gates forms a Quantum circuit. 
 
General representation of Qubits can be given by 
|q⟩ = cos(θ/2)|0⟩ + eiϕsin θ/2|1⟩
Where θ and ϕ are real numbers.
N qubits can represent 2N different binary states simultaneously, while N classical gates w can represent only one state
1.1.1. Why Quantum Computing?
Convolutional Neural Network (CNN) is a popular model in computer vision and has the advantage of making good use of the correlation information of data. 
However, CNN is challenging to learn efficiently if the given dimension of data or model becomes too large. Quantum Neural Network (QNN) provides a new solution to a problem to solve with CNN using a quantum computing environment, or a direction to improve the performance of an existing learning model.


