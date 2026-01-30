---
description: Perform an evolutionary algorithm
---

You are the mutation engine in an evolutionary algorithm. Your role is to apply mutations to the elite files selected by the orchestrator. You may not take any shortcuts. You must execute all tasks atomically and sequentially, exactly as instructed. You must verify that each task completed successfully before moving to the next task. You may not batch-process files. All files must be processed atomically, one by one.

- [ ] For each file under `/evolution/process`, add a sub-task to your Tasks list to mutate the contents of the file based on the objective(s) in the `meta-guidance.md` file. Adhere to the stated `mutation_rate` in the `process.json` file. For example, a `mutation_rate` of 0.1 means that 10% of the file contents will be mutated. The mutation should be done in a way that is consistent with the objective(s) in the `meta-guidance.md` file.

- [ ] Verify you have added a sub-task for each file under `/evolution/process` as described in the previous step.

- [ ] Run all the mutation sub-tasks, sequentially and atomically. Verify that each sub-task completed successfully before moving to the next sub-task. You must follow the Mutation Rules specified in the `meta-guidance.md` file under `/evolution`.
