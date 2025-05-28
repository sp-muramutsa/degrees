# Degrees of Separation

## Project Overview

This project exemplifies foundational Artificial Intelligence methodologies by addressing the classic "degrees of separation" problem within a large-scale knowledge graph of actors and movies. It models the problem as a graph search task to find the shortest path connecting two individuals through shared film appearances.

## AI Concepts

* **Graph-Based Knowledge Representation:**
  Actors and movies are represented as nodes and edges, respectively, forming a complex relational network that serves as a knowledge base.

* **Search Algorithms in AI:**
  Implements Breadth-First Search (BFS) using a queue-based frontier to systematically explore possible connections. This approach guarantees finding the shortest path in an unweighted graph.

* **State Space and Transition Modeling:**
  Each actor represents a state, and transitions (actions) correspond to shared movie roles, illustrating how AI agents can navigate environments defined by states and actions.

* **Ambiguity Resolution & Human-in-the-Loop:**
  The system includes mechanisms to handle ambiguous queries by interacting with the user to disambiguate entities sharing identical names, reflecting practical AI strategies for managing uncertainty and incomplete information.

* **Knowledge-Based Agent Principles:**
  By relying on structured data and search heuristics, the program functions as a knowledge-based agent, making decisions based on stored facts and relationships.

## Implementation Details

* Uses Python for all logic and data processing.
* CSV files store extensive datasets describing people, movies, and their relationships.
* Data is preprocessed into memory-efficient dictionaries and sets for rapid lookup.
* Search logic uses custom data structures (`Node`, `StackFrontier`, `QueueFrontier`) for managing explored and frontier states.

## Usage

Execute the script via command line with an optional dataset directory parameter:

```bash
python degrees.py [directory]
```

If omitted, defaults to the `large` dataset directory. The user is prompted for two actor names, and the program returns the shortest chain of connections through movies linking them, or indicates if no connection exists.

## Project Structure

* `degrees.py`: Main executable containing data loading, search logic, and user interaction.
* `util.py`: Supporting classes for graph search management.
* `large/`, `small/`: Dataset folders with CSV files (`people.csv`, `movies.csv`, `stars.csv`) reflecting the knowledge graph in varying scales.

---
**Author:** CS50 & Sandrin Muramutsa

---
No license specified.
