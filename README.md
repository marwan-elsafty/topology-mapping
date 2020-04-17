# Topology Mapping

Simulating large-scale network experiments requires powerful physical resources.
However, partitioning could be used to reduce the required power of the resources and to
reduce the simulation time. Topology mapping is a partitioning technique that maps the
simulated nodes to different physical nodes. 
We will use spectral clustering to partition a given network topology on the available physical nodes.
The network topology is a graph of N nodes communicating with each other by sending
data traffic through a set of edges. An edge in the topology is weighted by the traffic
(Mbps) passing through it. Our clustering technique should find the cut that minimizes
the traffic between different partitions


 
### Dataset

*  The dataset contains 30 network topology with 3 topology sizes (10 simulated
   nodes, 50 simulated nodes, and 100 simulated nodes)
*  Each topology is described in a .txt file.
*  Each line in the file is an edge in the topology: <from, to, traffic (Mbps)>
*  Ground truth clustering is available for topologies with sizes 10 and 50. The
   <ground_truth.txt> file contains a line for each topology ordered by the topology
   name: t_10_0, t_10_1, …, t_50_0, t_50_1, …, t_50_9
*  The ground truth line consists of N values (number of nodes), where nodes having
   the same value are in the same cluster.
