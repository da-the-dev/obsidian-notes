# Components
1. **Composed of node layers**
	- Three main layers:
		1. Input layer
		2. Hidden layer
		3. Output layer
2. Uses a [[linear regression model]] (model to predict future events)
   ![[Neuron]] 
3. **Data is passed between layers in a [[Feed Forward network]]**
4. **ANNs rely on training data ([[(Un)Supervised learning]])**
5. There are many different types of networks
	- CNN
	- Feed forward
	- RNN
	- etc.
## Lecture explanation
Heavily inspired by how neurons work in the brain
Specified by:
- **Architecture**
	- How are the connections made
	- What Neurons are connected to others
		- *Feedforward*
		- *Recurrent*
- **[[Neuron]] Model**
	- What functions can the neurons take as inputs
	- Can restrict the learning algorithm (backpropagation requires the functions to be differentiable)
- **Learning Algorithm**
	- Connected Neurons have weights in their connections
	- How do we make the updates to weights?
		- *[[Backpropagation]] of errors*
		- *[[Evolutionary algorithms|Evolutionary methods]]*
		- *[[(Un)Supervised learning]]*
# Basic training algorithm
- Initialize the weights in the network (often randomly)
- `repeat`
	- `for each example e in the training set do`
		- `O = neural-net-output(network, e); // forward pass`
		- `T = teacher output for e;`
		- Calculate error $(T - O)$ at the output units;
		- Compute $w_{j} = w_{j} +a * Err * I_{j}$ for all weights from hidden layer to output layer *(backward pass)*
		- Compute $w_{j} = w_{j} +a * Err * I_{j}$ for all weights from input layer to hidden layer
		- Update the weights in the network to the new weights;
	- `end for`
- `until all examples classified correctly or stopping criterion met`
- `return(network)`
# Error calculation
Each node is considered to be part of the error in the overall function based on its weight in the input:
$$
j=\sum _{i \in outputs}w_{ij}\delta_{i}
$$
where:
- $j$ is the error of the hidden node 
- $\delta_{i}$ is the error at the output node $i$ 
# References
- You know it's good if its 3Blue1Brown: https://www.youtube.com/watch?v=aircAruvnKk&list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi&index=1
- https://www.youtube.com/watch?v=jmmW0F0biz0