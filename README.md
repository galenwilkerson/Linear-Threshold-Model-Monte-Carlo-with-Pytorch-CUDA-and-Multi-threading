# Linear Threshold Model - Monte Carlo Simulation with PyTorch, CUDA, and Multi-Threading

This repository contains a Jupyter notebook that simulates the Linear Threshold Model (LTM) using PyTorch, CUDA, and multi-threading. The LTM is a framework used to study social computing, decision-making, and information diffusion in networks.

## Table of Contents

- [Introduction](#introduction)
- [Historical Background](#historical-background)
- [Model Description](#model-description)
- [Simulation Process](#simulation-process)
- [Applications](#applications)
- [Installation](#installation)
- [Usage](#usage)
- [Example](#example)
- [Contributing](#contributing)
- [License](#license)

## Introduction

The Linear Threshold Model (LTM) helps researchers understand how behaviors, ideas, innovations, or information spread through a network of individuals. Each node represents an individual, and edges signify social connections or interactions. This model is widely used in social computing, decision-making, and information diffusion studies.

## Historical Background

### Mark Granovetter

In 1978, sociologist Mark Granovetter introduced the concept of "threshold models of collective behavior." He emphasized the importance of weak ties in social networks and how they play a crucial role in spreading information and innovations.

### Duncan Watts

In the early 2000s, sociologist Duncan Watts extended Granovetter's ideas by applying them to network theory and complex systems. He explored how network structure affects social influence dynamics and demonstrated that small-world networks facilitate rapid and widespread diffusion.

### Percolation Theory

Percolation theory, adapted from studying fluids through porous materials, helps explain how a critical mass of initial adopters leads to a cascade of activation in networks. The LTM, viewed through this lens, identifies conditions for effective information spread.

## Model Description

### Nodes and Edges

- **Nodes**: Represent individuals or entities in the network.
- **Edges**: Represent connections or interactions between nodes.

### Initial State

Each node starts in either an active (influenced) or inactive (uninfluenced) state, determined by initial conditions or randomly assigned.

### Thresholds

Each node has a threshold value representing the fraction of its neighbors that need to be active for the node to become active. This threshold reflects the node's susceptibility to influence.

### Activation Rule

A node becomes active if the fraction of its active neighbors meets or exceeds its threshold value.

### Propagation and Iteration

The model iteratively updates each node's state based on the activation rule until the network reaches a stable state or a maximum number of steps is reached.

## Simulation Process

1. **Initialization**: Initialize the network with nodes and edges, and assign initial states and thresholds.
2. **Fraction of Activated Neighbors**: Calculate the fraction of active neighbors for each node.
3. **Threshold Comparison and Activation**: Compare the fraction of active neighbors to the threshold for each node.
4. **Iteration and Convergence**: Iteratively update the states of the nodes until convergence or a maximum number of iterations.
5. **Outcome and Analysis**: Analyze the final state of the network to understand the spread of influence.

## Applications

- **Social Computing**: Understanding the spread of social behaviors and trends.
- **Decision Making**: Studying collective decision-making processes.
- **Information Diffusion**: Analyzing the spread of information in networks.

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/your-username/Linear-Threshold-Model-Pytorch.git
    cd ltm-simulation
    ```

2. Create a virtual environment:
    ```sh
    python -m venv env
    source env/bin/activate  # On Windows, use `env\Scripts\activate`
    ```

3. Install the required packages:
    ```sh
    pip install -r requirements.txt
    ```

## Usage

Open the Jupyter notebook:
```sh
jupyter notebook "Linear_Threshold_Model_Monte_Carlo_Pytorch.ipynb"
