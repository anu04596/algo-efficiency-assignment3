# 🗺️ Problem 2 – Route Finding Using Bellman-Ford Algorithm

## 1️⃣ Real-World Context
Navigation and routing systems like **Google Maps** or **Waze** rely on shortest path algorithms to calculate optimal travel routes.  
Sometimes, road segments may have **negative weights** (e.g., toll rebates, discounts, or negative cost factors).  
Bellman-Ford is preferred for such cases because it handles **negative edge weights** safely.

---

## 2️⃣ Graph Modeling
| Entity | Representation |
|:--------|:----------------|
| City / Location | Node |
| Road / Path | Directed Edge |
| Distance / Cost | Weight (positive or negative) |
| Data Structure | List of edges (u, v, w) |

Example input edges:
A → B (4), A → C (5), B → C (-6), C → D (2), D → E (1), B → E (10)


---

## 3️⃣ Algorithm – Bellman-Ford
### Steps:
1. Initialize distance from source to all vertices as infinity, except source = 0.  
2. Relax all edges **V−1 times**, where V is number of vertices.  
3. Check once more for changes to detect **negative weight cycles**.  
4. If a cycle is detected, mark affected nodes appropriately.

---

## 4️⃣ Output Example
For source **A**, the shortest distances might be:
A: 0
B: 4
C: -2
D: 0
E: 1


Negative-cycle-affected nodes (if any) are also reported.

---

## 5️⃣ Visualization
Each edge is **directed** with an arrow, and weights are labeled.
This helps visualize how distance updates propagate along paths and where negative edges exist.

---

## 6️⃣ Complexity Analysis
| Operation | Complexity | Explanation |
|:-----------|:------------:|:------------|
| Relax edges | **O(V * E)** | Each of (V−1) iterations scans all edges |
| Cycle detection | **O(E)** | Additional single pass |
| Space | **O(V)** | To store distances and parents |

---

## 7️⃣ Advantages & Limitations
**✅ Advantages**
- Works with **negative weights**.
- Detects **negative weight cycles**.
- Simpler to implement than Dijkstra’s for dense graphs.

**⚠️ Limitations**
- Slower (O(V·E)) than Dijkstra (O(E log V)).
- Inefficient for large-scale real-time routing (e.g., millions of roads).

---

## 8️⃣ Conclusion
Bellman-Ford is an essential algorithm for finding shortest paths in **weighted directed graphs**, especially when **negative edges** exist.  
It guarantees correctness where Dijkstra’s fails. In navigation systems, it provides robust fallback logic for complex cost scenarios.

---

**Time Complexity:** O(V * E)  
**Space Complexity:** O(V)  
**Algorithm Used:** Bellman-Ford  
**Application Domain:** Navigation / Routing Systems
