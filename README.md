# Catan - Board Game Simulator with AI Agent

[![SonarQube Cloud](https://sonarcloud.io/images/project_badges/sonarcloud-dark.svg)](https://sonarcloud.io/summary/new_code?id=MohitGedela_Team19-Catan-V3)

**Course:** SFWRENG 2AA4: Software Design I  
**Institution:** McMaster University, Winter 2026  
**Team:** Team 19

---

## Team Members
- Manasvi Bandi
- Nithya Majeti
- Mohit Gedela
- Lohitashwa Madhan 

---

## Overview
<p align="justify">
This project is a Java-based simulator for Settlers of Catan that models the core game elements, including the board, players, resources, roads, settlements, cities, dice rolls, turns, robber behavior, resource production, and victory point tracking. The simulator follows the rules specified in the course rulebook and uses object-oriented design principles such as abstraction, encapsulation, inheritance, polymorphism, clear class responsibilities, SOLID principles, and other OO mechanisms to organize the game logic.

The simulator was extended to include boundary and partition test cases, which were run using JUnit to validate core gameplay behavior such as board limits, dice roll ranges, resource handling, and building logic. It was also improved with several design-pattern features: the Command pattern for human-player commands and undo/redo, the Strategy pattern for a rule-based AI agent, an observer-style visualizer that exports board state to JSON, and a Chain of Responsibility flow for handling priority AI constraints before normal strategy selection. SonarQube was also used to support code quality analysis and identify maintainability issues.

</p>

---

## Requirements to Run
* Java 25 (OpenJDK 25.0.1) 
* Git
* Eclipse (JUnit 5)
* Python3

---

## How to Run

### Part 1: Visualizer Setup

#### 1. Clone the repository and navigate to the visualizer
```bash
git clone https://github.com/MohitGedela/Team19-Catan-V3.git
cd Task3
cd visualize
```

#### 2. Set up a Python virtual environment
```bash
python3.11 -m venv .venv
source .venv/bin/activate
```

#### 3. Install the required packages
```bash
pip install -r requirements.txt
```

#### 4. Clone the Catanatron rendering library
```bash
git clone -b gym-rendering https://github.com/bcollazo/catanatron.git
cd catanatron
```

#### 5. Install Catanatron's dependencies
```bash
pip install -e ".[web,gym,dev]"
```

#### 6. Go back to the visualizer directory
```bash
cd ..
```

#### 7. Run the visualizer

**Single render:**
```bash
python light_visualizer.py base_map.json state.json
```

**Watch mode:**
```bash
python light_visualizer.py base_map.json --watch
```

*Note: It is not aligned with the mappings in the repo provided, so to make it work, please use the outlined mappings:
## Tile-Node Mappings
```java
private int[][] tilesNodes = {
    // Row 1 (3 tiles)
    { 42, 40, 41, 16, 18, 38 },
    { 41, 43, 44, 19, 17, 16 },
    { 44, 45, 46, 47, 20, 19 },

    // Row 2 (4 tiles)
    { 39, 38, 18, 13, 15, 35 },
    { 18, 16, 17,  0,  5, 13 },
    { 17, 19, 20, 21,  1,  0 },
    { 20, 47, 48, 49, 22, 21 },

    // Row 3 (5 tiles)
    { 37, 35, 15, 14, 34, 36 },
    { 15, 13,  5,  4, 12, 14 },
    {  5,  0,  1,  2,  3,  4 },
    {  1, 21, 22, 23,  6,  2 },
    { 22, 49, 50, 51, 52, 23 },

    // Row 4 (4 tiles)
    { 34, 14, 12, 11, 32, 33 },
    { 12,  4,  3,  9, 10, 11 },
    {  3,  2,  6,  7,  8,  9 },
    {  6, 23, 52, 53, 24,  7 },

    // Row 5 (3 tiles)
    { 32, 11, 10, 29, 30, 31 },
    { 10,  9,  8, 27, 28, 29 },
    {  8,  7, 24, 25, 26, 27 },
};
```

---

### Part 2: Running the Java Game

#### Run manually (To see live render create another tab and run part 1. This will allow to see live snapshots of the boards that are generated in the scraped boards folder in Task3/visualize)
```bash
cd Task3
java Demonstrator.java
```

---

## File Structure
```
Team19-Catan-V3/
├── .github/
│   └── workflows/
├── UML/
│   └── UML Class Diagram.png
├── code/
│   ├── visualize/           # Python visualizer and state.json
│   └── *.java               # Source files
├── Team19_Assignment3_Report.pdf
├── sonar-project.properties
└── README.md
```
---

## Software & Tools Used
- **Java** – For compiling and running the simulator and demonstrator programs  
- **Eclipse Papyrus** – For UML modeling and code generation  
- **Visual Studio Code** – For editing and navigating Java code  
- **GitHub** – Repository hosting and version control  
- **Python** – For compiling and running the visualizer 

---

## Our Process
- **Project Board:** [View our Kanban Board](https://github.com/users/MohitGedela/projects/10)
- **Tasks:** Work items created and assigned as GitHub Issues throughout the project
- **Merging:** Features developed on separate branches and merged through pull requests

---

## Assignment checklist

### Technical Content
- [x] Task 1: Command pattern designed and implemented (undo/redo)
- [x] Task 2: Observer pattern designed and implemented (Visualizer decoupling)
- [x] Task 3: Strategy pattern designed (AI agent rule evaluation)
- [x] R3.1: Undo/redo functionality implemented
- [x] R3.2: Rule-based AI with value scoring implemented
- [x] R3.3: Constraint-based AI rules implemented
- [x] Reflection points written for all three tasks
 
### Delivery
 
#### Software
- [x] Requirements addressed
- [x] Demonstrator implemented and documented
 
#### Management
- [x] Kanban board maintained and publicly available
- [x] Commits linked to work items
- [x] Deliverable tagged
 
### Report
- [x] Reflection points elaborated
- [x] Report written
- [x] Report submitted
