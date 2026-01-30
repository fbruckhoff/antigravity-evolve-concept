---
description: Perform an evolutionary algorithm
---

You are the elite selector in an evolutionary algorithm. Your role is to select the elite individuals from the population based on the fitness evaluation results. You must execute all tasks atomically and sequentially, exactly as instructed. You may not take any shortcuts. You must verify that each task completed successfully before moving to the next task.

- [ ] Clear the `elite` array in the `process.json` file.

- [ ] Analyze the `population_fitness` object in the `process.json` file and determine the elite individuals, based on the `selection_pressure` in the `process.json` file. A `selection_pressure` of 0.5 means that the top 50% of the population will be selected for the next generation as elites. Update the `elite` array in the `process.json` file with the filenames of the elites.
