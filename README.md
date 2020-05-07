# NetLogo - ICM

SNA ( social network analysis ) project : Independent cascade modelling (ICM)
Submitted to : [Dr. Sakthi Balan Muthiah, Associate Professor, LNMIIT](https://www.lnmiit.ac.in/Department/CSE/Department_FacultyProfile.aspx?nDeptID=212)
Date : May, 2020

 - Creating a scale free model with NetLogo
 - Applying ICM (Independent Cascade Model) to find the maximum number steps required to get to the maximum number of nodes.
	 - Activation probabilities for the pair of nodes which is needed for ICM are assigned randomly

## Independent Cascade Model of Information Diffusion

Independent Cascade Model (ICM) is a stochastic information diffusion model where the information flows over the network through Cascade. Nodes can have two states, (i) Active: It means the node already influenced by the information in diffusion. (ii) Inactive: node unaware of the information or not influenced.

The process runs in discrete steps. At the beginning of ICM process, few nodes are given the information known as seed nodes as in our case we have started with one active node. Upon receiving the information these nodes become active. In each discrete step, an active node tries to influence one of its inactive neighbors. In spite of its success, the same node will never get another chance to activate the same inactive neighbor. The success depends on the propagation probability of their tie. Propagation Probability of a tie is the probability by which one can influence the other node. In reality, Propagation Probability is relation dependent, i.e., each edge will have different value. However, for the experimental purpose, it is often considered to be same for all ties.

## Codes
The code for producing a scale free network is available in `scale-free.nlogo` file. The code for the ICM modelling is available in `ICM.nlogo` file.

## Working
The above project works with [NetLogo](https://netlogoweb.org/). 
The project has the following buttons :
1. Setup : Setup the environment with the number of nodes in the slider num-nodes
2. Layout : To evenly layout the nodes and apply the spring coefficients to it.
3. Go : To connect the nodes. This triggers a procedure named go where, it stochastically choses a node each time to connect with and produce as scale free network.
4. Cascade : To start the cascading of information based on the ICM model
5. Clear Cascade : To clear the cascading and bring back the network to the original state

*The probability of activation can be chosen with the slider given*

## Output
![Output of ICM.nlogo](https://i.ibb.co/V2V92GH/Screenshot-from-2020-05-07-15-39-45.png)
