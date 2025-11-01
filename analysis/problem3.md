# 🚑 Problem 3 – Emergency Response System Using Dijkstra’s Algorithm

## 1️⃣ Real-World Context
In **disaster management** or **emergency response**, finding the **fastest route** for ambulances, fire trucks, or rescue teams is critical.  
All road travel times (weights) are **non-negative**, making **Dijkstra’s Algorithm** ideal for this scenario.

---

## 2️⃣ Graph Modeling
| Entity | Representation |
|:--------|:----------------|
| Intersection / Checkpoint | Node |
| Road between intersections | Weighted Edge |
| Travel Time | Weight (always positive) |
| Data Structure | Adjacency List with min-heap priority queue |

Example:
S–A(2), S–B(5), A–B(1), A–C(3), B–C(1), C–D(2)

---

## 3️⃣ Algorithm – Dijkstra
### Steps:
1. Initialize all distances to infinity, source = 0.  
2. Use a **min-heap (priority queue)** to pick the next nearest node.  
3. Update distances to its neighbors if shorter paths are found.  
4. Continue until all reachable nodes are processed.

---

## 4️⃣ Output Example
Shortest distances from S->
S: 0,
A: 2,
B: 3,
C: 4,
D: 6

Shortest path from S → D: **S → A → C → D**

---

## 5️⃣ Visualization
Graph edges are labeled with weights (travel times).  
The **shortest path** is highlighted in red in the plot, showing the route selected by Dijkstra’s algorithm.

---

## 6️⃣ Complexity Analysis
| Operation | Complexity | Explanation |
|:-----------|:-----------:|:------------|
| Using Min-Heap | **O(E log V)** | Each edge relaxation involves heap operations |
| Space | **O(V + E)** | To store adjacency and distance map |

---

## 7️⃣ Advantages & Limitations
**✅ Advantages**
- Efficient for **large positive-weight graphs**.
- Guarantees optimal paths.
- Widely used in **GPS**, **network routing**, and **game AI pathfinding**.

**⚠️ Limitations**
- Cannot handle **negative edge weights**.
- Slower than A* in heuristic-based search scenarios.

---

## 8️⃣ Conclusion
Dijkstra’s algorithm efficiently finds the **fastest route** in real-time navigation systems where edge weights represent travel time or distance.  
It’s the cornerstone for path planning in emergency and logistics networks.

---

**Time Complexity:** O(E log V)  
**Space Complexity:** O(V + E)  
**Algorithm Used:** Dijkstra’s Algorithm  
**Application Domain:** Disaster Management / GPS Routing
