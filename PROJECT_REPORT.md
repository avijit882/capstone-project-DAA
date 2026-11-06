Mini-Courier Planner - Project Report

1. Introduction

The Mini-Courier Planner is a Python-based project designed to prioritize parcels, optimize vehicle loading, and calculate efficient delivery routes. It uses fundamental Data Structures and Algorithms to solve real-world courier management problems.

The project combines sorting, dynamic programming, graph algorithms, shortest-path calculation, and route optimization.

2. Problem Statement

Courier services need to select parcels according to their priority, fit them within the vehicle’s weight capacity, and deliver them through an efficient route.

The main objective of this project is to develop a system that selects the most valuable parcels within the given weight limit and calculates a suitable delivery route starting and ending at the depot.

3. Project Objectives

1. Arrange parcels according to priority and deadline.
2. Select parcels without exceeding vehicle capacity.
3. Maximize the total declared value of selected parcels.
4. Represent delivery locations using a weighted graph.
5. Calculate shortest paths between delivery locations.
6. Generate an approximate delivery route.
7. Test correctness and measure algorithm performance.

4. System Design and Workflow

The project follows these steps:

1. Load parcel and route information from CSV datasets.
2. Sort parcels using the defined priority ordering.
3. Apply the 0/1 Knapsack Dynamic Programming algorithm to select parcels.
4. Build a weighted graph using road connections.
5. Apply Dijkstra’s algorithm to calculate shortest paths.
6. Use the nearest-neighbor approach to generate a delivery tour.
7. Return to the Depot and verify the final route.

5. Algorithms Used

5.1 Merge Sort

Merge Sort is used to arrange parcel records according to the defined priority, deadline, and parcel ID ordering.

Time Complexity: O(n log n)

5.2 0/1 Knapsack Dynamic Programming

The Knapsack algorithm selects the best combination of parcels while ensuring that the total packed weight does not exceed the vehicle capacity of 18 kg.

It maximizes the total declared value of the selected parcels.

Time Complexity: O(nW)

5.3 Dijkstra’s Algorithm

Dijkstra’s algorithm calculates the shortest path between delivery locations using positive weighted edges in the road graph.

A binary heap is used to efficiently select the next vertex with the minimum distance.

Time Complexity: O((V + E) log V)

5.4 Nearest-Neighbor TSP Approximation

The nearest-neighbor approach repeatedly selects the closest unvisited delivery location using shortest-path distances and finally returns to the Depot.

It is a fast heuristic but does not guarantee the optimal delivery tour.

6. Correctness Results

The executed notebook successfully passed all seven correctness checks:

1. Priority ordering matches the defined ordering.
2. Packed weight stays within 18.0 kg.
3. Selected declared value matches the exhaustive subset optimum.
4. Dijkstra returns the expected distance (7) on an independent three-node graph.
5. Every selected destination appears once in the tour.
6. The tour starts and ends at Depot.
7. Recomputed route length equals the reported total.

Final Execution Results

For the supplied dataset, the selected parcel IDs were:

P001, P003, P006, P009, P010, P011 and P012.

* Combined weight: 17.8 kg
* Declared value: 2,610
* Total shortest-path travel distance: 30.00 km

Delivery Tour:

Depot → Clinic → Hospital → University → Museum → Theatre → Harbor → Stadium → Depot

All seven correctness checks passed successfully.

7. Runtime Measurements

Runtime measurements were collected from the completed notebook execution. The values represent median elapsed time in seconds and may vary depending on the system and hardware.

Algorithm	Small Input	Small Time (s)	Large Input	Large Time (s)
Merge Sort	250 parcels	0.0013753	2,000 parcels	0.0162637
0/1 Knapsack DP	20 parcels, W=300	0.0012800	80 parcels, W=300	0.0107617
Dijkstra	30 vertices	0.0001526	120 vertices	0.0029651
Nearest-Neighbor TSP	10 stops	0.0000195	40 stops	0.0002039

The runtime measurements demonstrate how execution time changes as the input size increases.

8. Limitations

1. The project uses a supplied dataset rather than live courier information.
2. The Knapsack algorithm maximizes declared parcel value within the weight limit.
3. The nearest-neighbor TSP approach provides an approximate route and may not produce the globally optimal solution.
4. Live traffic, delivery time windows, and multiple vehicles are not included.

9. Future Enhancements

The project can be improved by adding live traffic information, Google Maps integration, multiple vehicle support, delivery time windows, and a graphical user interface.

Larger real-world datasets can also be used to evaluate the performance of the algorithms.

10. Conclusion

The Mini-Courier Planner successfully demonstrates the practical application of Data Structures and Algorithms in courier management.

It combines Merge Sort, 0/1 Knapsack Dynamic Programming, Dijkstra’s shortest-path algorithm, and the nearest-neighbor TSP approximation.

The system selected seven parcels with a combined weight of 17.8 kg and a declared value of 2,610. It generated a delivery tour with a total shortest-path travel distance of 30.00 km.

All seven correctness checks passed successfully. The project demonstrates how algorithmic techniques can improve parcel selection, vehicle loading, and delivery route planning.