Metro Network Simulation :metro:
1. Project Title & Short Description
This project is a Metro Network Simulator developed using Python. It aims to find the least transfer route and the fastest route within a given metro system.

📍 We use BFS & A* to calculate the best route!
⚡ Optimized algorithms for fast transportation!
⏳ Real-time duration estimations and station connections!

Project Goals:
🚇 Find the least transfer route between the selected start and destination stations.

🚄 Determine the fastest route between the selected stations based on travel time.

🌍 Provide a metro system structure that resembles real-world networks for analysis.

2. Technologies & Libraries Used
Python Libraries:
collections: Used for deque to optimize the BFS (Breadth-First Search) algorithm.

heapq: Used for managing the priority queue in the A algorithm*.

typing: Used to improve code readability with types like Dict, List, and Tuple.

3. Algorithmic Approach
BFS Algorithm (Least Transfer Route)
BFS (Breadth-First Search) finds the shortest path in terms of steps.

In this project, it is used to determine the least transfer route.

How BFS Works:
🚉 Add the starting station to the queue.

🌀 Check the current station at each iteration.

🎯 If the destination is found, return the result.

🔄 Add neighboring stations to the queue and mark them as visited

BFS Flowchart:

flowchart TD
    A[Start Station] -->|Visit Neighbors| B[First Neighbor]
    A --> C[Second Neighbor]
    B --> D[Is it the Destination?]
    C --> E[Is it the Destination?]
    D -->|Yes| F[Return Result]
    E -->|No| G[Add Neighbors to Queue]
    G --> A

A Algorithm (Fastest Route)*
🚀 The A algorithm* is used to calculate the shortest time route.
It uses a priority queue to always expand the most time-efficient path first.

How A Works:*
🚉 Add the starting station to the priority queue.

⏱️ Process the station with the lowest estimated travel time.

🎯 If the destination is found, return the result.

🔄 Add neighboring stations to the queue and update their travel times.

A*  Flowchart:
flowchart TD
    A[Start Station] -->|Add to Priority Queue| B[Get Lowest Time Node]
    B --> C[Check Neighbors]
    C --> D[Is it the Destination?]
    D -->|Yes| E[Return Result]
    D -->|No| F[Update Priority Queue with New Times]
    F --> B
4. Example Usage & Test Results

# Defining a Metro Network
metro = MetroNetwork()
metro.add_station("M1", "AŞTİ", "Blue Line")  # 🚉
metro.add_station("M2", "Kızılay", "Blue Line")  
metro.add_connection("M1", "M2", 5)

# Finding the Least Transfer Route
route = metro.find_least_transfer_route("M1", "M2")
print("Least transfer route:", " -> ".join(i.name for i in route))

# Finding the Fastest Route
route, time = metro.find_fastest_route("M1", "M2")
print(f"Fastest route ({time} minutes):", " -> ".join(i.name for i in route))

Example Test Cases
Start	Destination	Least Transfer Route	Fastest Route & Time
AŞTİ	OSB	AŞTİ → Kızılay → OSB	AŞTİ → Kızılay → OSB (25 min)
Batıkent	Keçiören	Batıkent → Demetevler → Gar → Keçiören	Batıkent → Demetevler → Gar → Keçiören (21 min)
Keçiören	AŞTİ	Keçiören → Gar → Kızılay → AŞTİ	Keçiören → Gar → Kızılay → AŞTİ (19 min)

5. Future Development Ideas
🌍 Integration with Real Metro Data: Enhance the project by using real metro data.

💻 Graphical User Interface (GUI): Develop an interactive interface for users to select stations on a map.

📊 Real-Time Traffic & Delays: Incorporate real-time train congestion and delays for a dynamic system.

🚋 Multi-Modal Transportation: Expand the simulation to include buses, trams, and other public transport for city-wide transit optimization.

