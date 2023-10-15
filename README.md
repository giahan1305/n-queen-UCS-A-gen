# n-queen-UCS-A-gen
# N-Queens Problem Solver

This Python code is a program that solves the N-Queens problem using three different algorithms: Uniform-Cost Search (UCS), A*, and a Genetic Algorithm. The N-Queens problem is a classic combinatorial problem where the goal is to place N chess queens on an N×N chessboard in a way that no two queens threaten each other. 

## Importing Libraries
The code begins by importing necessary libraries, including `random`, `time`, `sys`, `collections`, `PriorityQueue`, and `heappop` and `heappush` functions from `heapq`.

## Memory Measurement Functions
- `get_memory_usage(obj)`: A function to calculate the memory usage of an object.
- `get_program_memory_usage()`: A function to calculate the memory usage of the entire program.

## `BoardState` Class
- Represents the state of the chessboard, including the positions of the queens and a path cost.
- `generate_successors()`: Method to generate successor states by moving one queen at a time.
- `__lt__(self, other)`: Custom comparison method for priority queue ordering.

## `ucs_n_queens` Function
- Solves the N-Queens problem using Uniform-Cost Search (UCS) algorithm.
- It uses a priority queue and starts with a random initial state and iteratively explores states with the least path cost.
- `is_goal_state(state)`: A function to check if the goal state (no queens attacking each other) is reached.

## `solve_n_queens` Function
- Solves the N-Queens problem using the A* algorithm.
- Uses a priority queue and calculates the heuristic value for each state to find the solution.
- `calculate_heuristic(state)`: Function to calculate the heuristic value (number of conflicting queens).
- `generate_initial_state(n)`: Function to generate a random initial state.
- `get_successors(state)`: Function to get the successors of a state by moving one queen at a time.

## `Chromosome` and `Population` Classes
- These classes are used in the Genetic Algorithm to represent individual chromosomes and a population of chromosomes.
- `initialize()`: Method to initialize the population with random genes.
- `calculate_conflicts(chromosome)`: Method to calculate the number of conflicts for a chromosome.
- `selection()`: Method for selection in the Genetic Algorithm.
- `crossover(parent1, parent2)`: Method for crossover in the Genetic Algorithm.
- `mutation(chromosome)`: Method for mutation in the Genetic Algorithm.
- `evolve()`: Method to evolve the population in the Genetic Algorithm.
- `solve()`: Method to solve the N-Queens problem using the Genetic Algorithm.
- `get_best_solution()`: Method to get the best solution from the population.

## `print_board` Function
- Function to print the board representation with the queens placed.

## Input and Algorithm Selection
- The code takes user input for the number of queens (N) and the choice of algorithm (UCS, A*, or Genetic Algorithm).
- The appropriate algorithm is executed based on the user's choice.

## Output
- The program prints the solution for the N-Queens problem (the placement of queens) if found.
- It also displays the running time and memory usage of the program.

The code is structured to solve the N-Queens problem using different algorithms, allowing users to choose their preferred method for solving the problem. The choice of algorithm affects the efficiency and the speed of finding a solution.
