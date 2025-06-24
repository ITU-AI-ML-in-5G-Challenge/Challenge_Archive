# ITU-ML5G-PS-011: Combinatorial Optimization Challenge:- Delivery route optimization

## Description
In 5G era where everything is connected, rapid growth of network traffic poses great challenge to traditional network. In this context, intelligent route planning of network service is essential for efficient network management. In particular, how to achieve balance between low latency, high data bandwidth of network service and better utilization of network resources is the key issue for network planning and optimization.

This challenge is aimed to optimize the route planning in telecommunication network. Here the network is simplified as a high-speed transportation network due to its complexity, and then the problem is about how to optimize the delivery route planning in the transportation network.

For a given transportation network, where some goods are to be delivered between certain starting and ending points, competitors is required to figure out the route for delivery with the lowest transportation cost.
The features of the transportation network are as follows:

1. The network is an undirected graph, each transportation node is connected to no more than 10 other nodes.
2. There are no more than 300 transportation nodes in the network.
3. The transportation cost between 2 adjacent nodes depends on the distance between them.
4. There are multiple (no more than 40) lanes between 2 adjacent nodes, identified with numbers from 1 to 40.
5. There can be multiple deliveries on each lane simultaneously, but the total weight of goods delivered on each lane should be constrained within 10 tons.
For example, each lane between adjacent nodes A and B can transport 10 tons of goods in total at most, regardless of the direction of the transportation. If 4 tons of goods is being delivered on a lane, then this lane can only carry another 6 tons of goods during the following deliveries.
6. The total number of the deliveries is no more than 1 000.
7. The weight of goods for each delivery can only be 1 ton, 4 tons or 10 tons.
8. Each delivery must use the lanes with the same identifier in the whole transportation network.
For example, if the delivery uses lane 1 between nodes A and B, it can only use lane 1 between other nodes.

It should be noted that:

1. The routes for all the deliveries should planned ahead of time, and cannot be changed once determined.
2. The solutions should be applicable to all given samples.
3. The solutions are not limited to machine learning, deep learning and traditional algorithms.
4. It should take less than 30 minutes for the solutions to figure out the results.



## Evaluation criteria

Participants are required to submit runnable algorithms which plan the route for delivery with the lowest transportation cost, along with corresponding description document. Basically, these algorithms will be ranked by their total transportation cost on the datasets and duration of the calculation.

**Performance of algorithm (60%)**: Both total cost and running time will be taken into account.

**Solution advantage (30%)**: Whether the solution is reasonable and whether the solution has enough practicability, innovation and universality.

**Completeness (10%)**: Whether the requirements of the challenge are fulfilled according to the proposed scheme and design.
## Data source
Power point slides for the progress of teams during the challenge

## Resources
None


## Results
1. Victor Bear

