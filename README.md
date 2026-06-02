# AI-Popout-Game

A Python implementation of the **PopOut** board game featuring multiple Artificial Intelligence approaches, including:

* **Monte Carlo Tree Search (MCTS)**
* **Heuristic-enhanced MCTS**
* **ID3 Decision Tree**
* **Random AI baseline**

This project was developed to explore and compare different AI techniques in adversarial games, combining search-based methods and machine learning approaches.

---

# Authors

* **Flávia Queiroz**
* **Telma Freitas**

---

# Project Overview

The project implements the game **PopOut**, a variation of Connect Four where players can:

* Drop pieces into columns
* Remove their own bottom pieces ("PopOut" move)
* Win by aligning four pieces horizontally, vertically, or diagonally

The repository includes:

* Complete game logic
* Terminal interface
* AI agents
* Dataset generation tools
* ID3 model training
* Performance comparison scripts

---

# AI Implementations

## Monte Carlo Tree Search (MCTS)

The project includes a full implementation of the **Monte Carlo Tree Search** algorithm using the classical phases:

1. Selection
2. Expansion
3. Simulation
4. Backpropagation

MCTS evaluates game states through repeated simulations and progressively builds a search tree to improve decision-making.

### Features

* UCT (Upper Confidence Bound applied to Trees)
* Adjustable number of iterations
* Deep-copy game state simulation
* Dynamic move exploration

---

## Heuristic MCTS

A heuristic-enhanced version of MCTS was implemented to improve early-game efficiency and reduce search complexity.

### Improvements

* Faster exploration in highly branching states
* Better move prioritization
* Reduced computational cost

---

## ID3 Decision Tree

The project also implements an **ID3-based AI model** trained on datasets generated from simulated games.

### Dataset Features

The dataset stores:

* Board state
* Current player
* Best move chosen by MCTS

The trained ID3 model predicts moves based on previously generated gameplay data.

### Concepts Used

* Entropy
* Information Gain
* Decision Trees
* Dynamic discretization

---

# Project Structure

```text
proj_popout_ai/
│
├── 1_data/
│   ├── dataset_winner_150.csv
│   └── iris.csv
│
├── 3_src/
│   ├── game.py
│   ├── interface.py
│   ├── mcts.py
│   ├── dataset_generator.py
│   ├── id3_popout_dataset.py
│   ├── test_game.py
│   ├── utils.py
│   └── id3_model.pkl
│
├── 4_reports/
│   ├── id3_vs_MCTS.txt
│   ├── id3_vs_MCTS_Heuristico.txt
│   └── id3_vs_Random.txt
│
└── README.md
```

---

# Main Files

## `game.py`

Implements:

* Game rules
* Move validation
* Win detection
* State management
* PopOut mechanics

---

## `mcts.py`

Contains:

* MCTS implementation
* Heuristic MCTS
* Tree node structure
* UCT calculations

---

## `interface.py`

Interactive terminal interface using the `rich` library.

Allows matches between:

* Human vs AI
* AI vs AI

---

## `dataset_generator.py`

Generates datasets through automated AI matches.

Used to train the ID3 model.

---

## `id3_popout_dataset.py`

Implements:

* Entropy calculation
* Information gain
* ID3 training
* Prediction logic
* Model serialization

---

## `test_game.py`

Runs automated matches between AI agents to evaluate performance.

---

# Requirements

Install dependencies with:

```bash
pip install numpy pandas rich
```

---

# How to Run

## Start the Game Interface

```bash
python interface.py
```

---

## Generate Dataset

```bash
python dataset_generator.py
```

---

## Run AI Tests

```bash
python test_game.py
```

---

# Technologies Used

* Python
* NumPy
* Pandas
* Rich
* Pickle

---

# AI Comparison Goals

The project compares:

* Search-based AI (MCTS)
* Heuristic search
* Machine learning (ID3)
* Random baseline

Main evaluation criteria:

* Win rate
* Decision quality
* Computational efficiency
* Execution time

---

# Academic Concepts

This project explores several Artificial Intelligence topics, including:

* Adversarial Search
* Monte Carlo Methods
* Decision Trees
* Supervised Learning
* Game State Evaluation
* Information Gain
* Entropy
* Heuristic Search

---

# License

This project was developed for academic and educational purposes.

