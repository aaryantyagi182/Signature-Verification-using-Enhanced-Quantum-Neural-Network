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

