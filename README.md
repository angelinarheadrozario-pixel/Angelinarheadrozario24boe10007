# Angelinarheadrozario24boe10007
Vityarthi Ai Ml project 

\<br\>
\<br\>

# Pathfinding Project: A Multi-Algorithm Python Toolkit

A Python toolkit for simulating smart GPS navigation on grid-based maps. This project provides a robust framework for exploring and comparing different pathfinding algorithms, supporting both static and dynamic environments.

-----

## 🌟 Features

  - Search Algorithms: Includes implementations of classic graph search algorithms:

      - Breadth-First Search (BFS): Optimal for unweighted graphs.
      - Uniform Cost Search (UCS): Finds the lowest-cost path.
      - A\ Search:* A powerful algorithm that finds the most efficient path by using a heuristic function.

  - Heuristics: Utilizes *admissible heuristics, such as **Manhattan distance, for the A\ algorithm to efficiently guide the search.

  - Map Support: Easily switch between various grid-based map sizes: small, **medium, and **large.

  - Dynamic Obstacles: Simulate real-world scenarios with moving obstacles and vehicles.

  - Extensible: The modular design allows for easy integration of new search strategies, heuristics, and map files.

  - Logging: Automatically saves detailed run results for later analysis and performance comparison.

  - Unit Tests: Comprehensive test suite ensures the correctness of grid loading and search algorithm implementations.

-----

## 📁 Project Structure


├── run.py                # Main entry point for the application
├── requirements.txt      # Project dependencies
├── src/
│   ├── grid.py           # Core grid and map handling logic
│   ├── heuristics.py     # Heuristic functions for A* search
│   ├── localsearch.py    # Local search (placeholder for future implementation)
│   ├── obstacles.py      # Logic for handling dynamic obstacles
│   ├── search.py         # Implementations of BFS, UCS, and A*
│   └── utils.py          # Utility functions for logging and file handling
├── maps/                 # Directory for static and dynamic map files
├── tests/                # Unit tests for the project
└── report/               # Directory for reports and analysis of results


-----

## 🚀 Quick Start

### 1. Installation

First, clone the repository and install the required dependencies:

bash
git clone https://github.com/your-username/pathfinding-project.git
cd pathfinding-project
pip install -r requirements.txt


### 2. Running a Search

Execute the run.py script from your terminal with the desired arguments:

bash
python run.py --algo astar --map maps/small.txt --start 0,0 --goal 4,4


### Command-Line Arguments

  - --algo: Specifies the search algorithm. Options: bfs, ucs, or astar.
  - --map: Path to the map file. Example: maps/medium.txt.
  - --start: Start coordinates, formatted as x,y. Example: 0,0.
  - --goal: Goal coordinates, formatted as x,y. Example: 4,4.
  - --diagonals: Allow diagonal movement. Use 1 for True and 0 for False.
  - --log: Path for the output log file. Defaults to out/run.log.

### Example Output

Upon successful execution, the script will output the found path and performance statistics:


Path: [(0, 0), (1, 0), (1, 1), (2, 1), (3, 1), (4, 1), (4, 2), (4, 3), (4, 4)]
Stats: {'nodes_expanded': 13, 'path_cost': 8}


-----

## 🗺 Maps

  - Static Maps: The format for static maps is simple. The first line contains the map's width and height. Subsequent lines represent the grid, where each number is the cost of moving through that cell. A value of -1 denotes an obstacle.
  - Dynamic Maps: For dynamic obstacles, refer to the example in maps/dynamic.json. This format allows for specifying scheduled movements for objects within the grid.

-----

## ✅ Testing

To run the full suite of unit tests for grid loading and search algorithms, use pytest:

bash
pytest


-----

## 🛠 Extending the Project

This toolkit is designed to be easily extensible:

  - Add New Heuristics: Implement new heuristic functions in src/heuristics.py.
  - Implement New Algorithms: Create new search strategies by adding a class or function to src/search.py.
  - Create New Maps: Add new static map files to the maps/ directory or create a new JSON file for a dynamic scenario.

-----

## 📄 License

This project is released under the MIT License.
