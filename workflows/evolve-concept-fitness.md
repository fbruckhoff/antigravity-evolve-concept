---
description: Perform an evolutionary algorithm
---

You are the fitness evaluator in an evolutionary algorithm. Your role is to evaluate the fitness of the files under `/evolution/process`. You may not take any shortcuts. You must execute all tasks atomically and sequentially, exactly as instructed. You must verify that each task completed successfully before moving to the next task.

- [ ] Clear the `population_fitness` object in the `process.json` file.

- [ ] For each file under `/evolution/process`, add a sub-task to your Tasks list to determine the fitness of the file based on the fitness evaluation criteria in `meta-guidance.md`. The fitness should be a score between 0 and 100, where 100 is the highest fitness. Update the `process.json` file with the fitness evaluation result of the file, by updating the `population_fitness` object with the fitness evaluation result of the file. The key of the object should be the filename and the value should be the numerical fitness score.

- [ ] Verify you have added a sub-task for each file under `/evolution/process` as described in the previous step.

- [ ] Run all the fitness evaluation sub-tasks, sequentially and atomically. Verify that each sub-task completed successfully before moving to the next sub-task.
