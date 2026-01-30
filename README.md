# 🧬 Evolutionary Algorithm Workflow for Google Antigravity

This workflow implements an evolutionary algorithm designed to evolve and refine unstructured text concepts, drafts, and ideas. Unlike code evolution tools, this workflow is intended for improving concepts and unstructured text through recursive mutation, crossover, and selection of the fittest.

## High-Level Overview

The workflow acts as an orchestrator that manages a population of variations. In each cycle, it:
1.  **Evaluates Fitness**: Assesses how well each variation meets the defined objectives.
2.  **Selects Elites**: Identifies the strongest versions to preserve.
3.  **Applies Mutations & Crossovers**: Generates new variations by modifying or combining existing ones.
4.  **Iterates**: Repeats the process to progressively enhance the population.

This process allows you to explore a wide search space of ideas and converge on high-quality candidates that align with your specific goals. I've found it particularly useful for refining creative concepts, structuring content, and generating diverse but high-quality variations.

## Usage with Google Antigravity

This workflow is composed of a main entry point and several sub-workflows that handle specific parts of the evolutionary cycle.

### Installation

1.  Copy the workflow files into your project's `.agent/workflows/` directory.
    *   `evolve-concept.md` (Main Workflow)
    *   `evolve-concept-cycle.md` (Evolutionary Cycle)
    *   `evolve-concept-fitness.md` (Fitness Evaluation)
    *   `evolve-concept-elites.md` (Elite Selection)
    *   `evolve-concept-mutations.md` (Mutation Application)
    *   `evolve-concept-crossovers.md` (Crossover Application)

### Setup

Before running the workflow, you must set up the required folder structure in your project root:

1.  Create a folder named `evolution`.
2.  Inside `evolution`, create a subfolder named `process`.

Your structure should look like this:

```
/
├── .agent/
│   └── workflows/
│       ├── evolve-concept.md
│       ├── evolve-concept-cycle.md
│       ├── evolve-concept-fitness.md
│       ├── evolve-concept-elites.md
│       ├── evolve-concept-mutations.md
│       └── evolve-concept-crossovers.md
└── evolution/
    └── process/
```

### Running the Workflow

1.  Trigger the **`evolve-concept`** workflow.
2.  **First Run Configuration**:
    *   The workflow will ask you to populate `meta-guidance.md` in the `/evolution` folder. This file defines your objectives, fitness criteria, and mutation/crossover rules.
    *   It will also ask you to populate `genesis.md` in the `/evolution` folder. This is your starting concept or draft.
3.  **Evolution**:
    *   Once configured, the workflow will generate an initial population (e.g., 50 variations) in `/evolution/process`.
    *   It will recursively execute the evolutionary cycle (`evolve-concept-cycle`) to refine the population.
4.  **Result**:
    *   Upon completion, the best evolved concept will be saved as `result.md` in the `/evolution` folder.
