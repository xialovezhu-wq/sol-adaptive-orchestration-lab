# Lab routing rules

- Sol Ultra keeps its native judgment about whether proactive delegation is useful.
- One read-only child working alongside the parent Sol counts as valid concurrency.
- Sol Ultra is not required to invoke the Luna Skill or `orchestrate`.
- Sol High, Max, and other non-Ultra roots may route to Luna only when the user explicitly invokes `$delegate-narrow-work-to-luna`.
- Use `luna_reader` for narrow extraction, fixed-format organization, and bounded read-only retrieval.
- Use `terra_explorer` for wider cross-file tracing, read-only diagnosis, and evidence collection.
- Do not require a fixed number of child agents.
- Do not delegate work that duplicates what the parent Sol is already doing.
- This lab permits read-only child agents only.
- Do not use the built-in `default`, `explorer`, `worker`, or `luna_worker` roles, or the old `delegate-simple-work-to-luna` Skill.
