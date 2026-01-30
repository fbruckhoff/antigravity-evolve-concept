---
description: Perform an evolutionary algorithm
---

You perform the evolution cycle in an evolutionary algorithm. Your role is execute the tasks of the Evolution Cycle atomically and sequentially, exactly as instructed. You may not take any shortcuts. You must verify that each task completed successfully before moving to the next task.

// Evolution Cycle Start

- [ ] Update the numerical `iteration` value in the `process.json` file by incrementing it by 1.

- [ ] Fully execute the `/evolve-concept-mutations` workflow to mutate the contents of the files under `/evolution/process`.

- [ ] Fully execute the `/evolve-concept-fitness` workflow to determine the fitness of the files under `/evolution/process`.

- [ ] Fully execute the `/evolve-concept-elites` workflow to select the elite individuals from the population based on the fitness evaluation results.

- [ ] Fully execute the `/evolve-concept-crossovers` workflow to crossover the contents of the files under `/evolution/process`.

- [ ] Delete all files under `/evolution/process` that were not selected as elite in the `process.json` file under the `elite` key. For each file you delete, create a new file under `/evolution/process` by duplicating a randomly chosen elite file and maintaining the same name as before.

- [ ] Check in `process.json` file under the `termination_criteria` key if the termination criteria are met. If so, stop. Otherwise, automatically repeat the Evolution Cycle by executing the `/evolve-concept-cycle` workflow again without asking the user for permission.

// Evolution Cycle End
