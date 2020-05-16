# NetLogo - ICM

SNA ( social network analysis ) project : Independent cascade modelling (ICM)
Submitted to : [Dr. Sakthi Balan Muthiah, Associate Professor, LNMIIT](https://www.lnmiit.ac.in/Department/CSE/Department_FacultyProfile.aspx?nDeptID=212)
Date : May, 2020

 - Creating a scale free model with NetLogo
 - Applying ICM (Independent Cascade Model) to find the maximum number steps required to get to the maximum number of nodes.
	 - Activation probabilities for the pair of nodes which is needed for ICM are assigned randomly

## Independent Cascade Model of Information Diffusion

Independent Cascade Model (ICM) is a stochastic information diffusion model where the information flows over the network through Cascade. Nodes can have two states, (i) Active: It means the node already influenced by the information in diffusion. (ii) Inactive: node unaware of the information or not influenced.

The process runs in discrete steps. At the beginning of ICM process, few nodes are given the information known as seed nodes as **in our case we have started with one active node**. Upon receiving the information these nodes become active. In each discrete step, an active node tries to influence one of its inactive neighbors. In spite of its success, the same node will never get another chance to activate the same inactive neighbor. The success depends on the propagation probability of their tie. Propagation Probability of a tie is the probability by which one can influence the other node. **In reality, Propagation Probability is relation dependent, i.e., each edge will have different value. However, for the experimental purpose, it is often considered to be same for all ties.**

## Asumptions
- Starting with only one active node
- Considering the activation probabilities of all the ties between nodes as same
- The size of network is taken to be 500 nodes ( Because of hardware restrictions with NetLogo client over PC and ease of analysis )

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

*The probability of activation and number of nodes can be chosen with the slider given*


## Output/Inferences

The number of steps required to spread to the entire network depends exponentially on the value of the activation-probability.

**As the activation-probability increases the number of steps required decreases.**

Below attached table describes the number of steps taken by ICM to infect all the nodes, based on the value of activation probability. 

ICM is applied 5 times on a scale free network to obtain the below results.
![Table](https://i.ibb.co/6PXP8F1/Screenshot-from-2020-05-16-22-08-21.png)

Below attached graph represents the same table,
![Graph](https://i.ibb.co/n86g8Lp/ICM-Model-Performance.png)


Below are the attached screenshots for the ICM for, 
- Number of Nodes : 500
- Activation Probability : 0.3

![enter image description here](https://i.ibb.co/wpHH49K/0-3-1.png)

![enter image description here](https://i.ibb.co/Vxnt4mg/0-3-2.png)

![enter image description here](https://i.ibb.co/g7nTmKj/0-3-3.png)

![enter image description here](https://i.ibb.co/kqqy8vb/0-3-4.png)

![enter image description here](https://i.ibb.co/B2yqXvw/0-3-5.png)

Below are the attached screenshots for the ICM for, 
- Number of Nodes : 500
- Activation Probability : 0.8

![enter image description here](https://i.ibb.co/ctkphnV/0-8-1.png)

![enter image description here](https://i.ibb.co/6JtZMxt/0-8-2.png)

![enter image description here](https://i.ibb.co/qgpPzr4/0-8-3.png)

![enter image description here](https://i.ibb.co/JskYXz4/0-8-4.png)

![enter image description here](https://i.ibb.co/mBDXLDs/0-8-5.png)



