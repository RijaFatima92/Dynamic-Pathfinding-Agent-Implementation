# Dynamic Pathfinding Agent

A real-time, grid-based pathfinding visualizer built with Python and Pygame. This project implements Informed Search Algorithms (A* and Greedy Best-First Search) capable of navigating dynamic environments where obstacles appear while the agent is in motion.

## 🚀 Features
* **Search Algorithms:** Toggle between **A* Search** ($f(n) = g(n) + h(n)$) and **Greedy Best-First Search** ($f(n) = h(n)$).
* **Heuristics:** Supports **Manhattan** and **Euclidean** distance calculations.
* **Dynamic Re-planning:** Real-time obstacle spawning and automated path recalculation if the current route is obstructed.
* **Interactive Editor:** Manually place/remove walls or generate a random maze with 30% obstacle density.
* **Real-Time Metrics:** Dashboard tracking Nodes Visited, Path Cost, and Execution Time (ms).

## 🛠️ Installation & Setup

### Prerequisites
* Python 3.8 or higher
* Anaconda (Optional, but recommended)

### Dependencies
Install the required library using pip:
```bash
pip install pygame
