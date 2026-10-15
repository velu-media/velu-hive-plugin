### Workplans and lanes (Hive)

- Hive's <hive> line names this session's autonomy, set by Velu's owners: auto, suggest or off. In
  auto, this topic and the topic `rulings` replace the "ask me" lines of CLAUDE.local.md before "What always holds" for work inside a workplan and for
  files Hive rules on. In suggest, tell me what Hive decided and ask me before acting on it. In off,
  only tell me.
- When you save a plan (a superpowers plan, a `## T-n [repo]` plan, a PROGRESS.md), Hive turns it into
  a workplan by itself: one task per task and repository, keyed like RSL-T3, grouped into lanes. Keep
  `### Task N:` headings, and give every task a `**Files:**` list and, where they apply, `**Repo:**`
  and `**Depends:** Task N` lines. Never write Hive's keys, lanes or statuses into a file by hand, and
  never put credentials, customer data or file contents in a plan.
- `{{hive}} progress workplans` lists your workplans and the team's (titles only), with each one's
  <KEY>; `{{hive}} progress lanes <KEY>` shows its lanes: tasks in one lane run one after another on
  one branch; different lanes can run at the same time.
- Take a task only when I pick it, or when I asked you to work through its workplan: then run
  `{{hive}} progress autopilot <KEY> on` once, and take what `{{hive}} progress next <KEY>` offers with
  `{{hive}} progress take <repository> <key>`. Work each lane in the worktree and on the branch its HIVE
  NEXT names, created with the commands it prints and the repository's own rules: where the repository
  keeps commits, pushes and merges for its committer agent, hand those commands to it exactly as
  printed. Put the task key in every commit subject (`RSL-T3: …`, or `feat(RSL-T3): …` where the
  repository wants a type).
- Before each task's first edit, run `{{hive}} progress move <repository> <task-id> in-progress` and
  `{{hive}} check <repository> <files>`. If Hive does not confirm the lane is still yours, do not start
  the task.
- When a task is done, commit it and push the lane branch. When Hive says the lane is ready for the
  mother branch, open or update its pull request into the mother branch, never into develop or main;
  merge it yourself only where HIVE NEXT says agents may. Merging into develop, main or any
  integration branch is always a person's step.
- When Hive says a dependency is in the mother branch, merge the mother branch into your lane before
  your next task. Never merge, rebase or push a teammate's branch.
- To hand a task you hold to another of my sessions, only when I ask: commit and push its lane branch, then
  run `{{hive}} progress handover <repository> <KEY> <session>` (`{{hive}} progress sessions` lists my live
  sessions and their labels; `{{hive}} progress session <label>` names this one). Uncommitted work and this
  conversation never move: the other session starts from the task's plan, its progress and the pushed
  branch. When Hive says another of my sessions handed you a task, take it with the command its HIVE NEXT
  names (in auto, in a headless run too) or ask me first (with no one to ask, name it in your final answer); if this session cannot take it, run `{{hive}} progress handover
  <repository> <KEY> --refuse`.
