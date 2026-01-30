---
description: Perform an evolutionary algorithm
---

You are the orchestrator in an evolutionary algorithm that maintains a population, evaluates fitness, selects elites, applies mutation/crossover, and iterates. Optimize toward stated objectives, prevent premature convergence, log progress, stop on convergence or budget.


# Tasks

- [ ] If the file `meta-guidance.md` does not exist under `/evolution`, create a new file `meta-guidance.md` under `/evolution`, with exactly the following contents:

```
# Objectives

# Fitness Evaluation Criteria

# Mutation Rules

# Crossover Rules
```

- [ ] Prompt the user to provide information within the `meta-guidance.md` file. Await their confirmation before you proceed.

- [ ] Create a new file `process.json` under `/evolution/process` (folder already exists; do not create a new folder). If the file already exists, overwrite it. Initialize the file with the following contents:

```
{
	"iteration": 0,
	"population_fitness": {},
	"elite": [],
	"mutation_rate": 0.1,
	"crossover_rate": 0.1,
	"selection_pressure": 0.5,
	"termination_criteria": {
		"max_iterations": 100,
		"max_fitness": 100
	}
}
```

- [ ] Check if the file `genesis.md` exists under `/evolution`. If it does not exist, create an empty `genesis.md` file under `/evolution` and prompt the user to fill in the `genesis.md` file. Await their confirmation before proceeding.

- [ ] Make 50 copies of the `genesis.md` file under `/evolution`, and place these copies under `/evolution/process` with the following naming pattern: `v_{index}.md`, counting from 1 to 50. Use an efficient command for this.

- [ ] Execute the `/evolve-concept-cycle` workflow.

- [ ] Once the recursive `/evolve-concept-cycle` workflow terminates, identify the best elite concept from the `process.json` file under the `elite` key, then copy the file as `result.md` placed under `/evolution`.
