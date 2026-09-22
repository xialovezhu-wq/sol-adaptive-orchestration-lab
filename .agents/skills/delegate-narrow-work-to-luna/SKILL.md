---
name: delegate-narrow-work-to-luna
description: Explicitly delegate one narrow read-only extraction, fixed-format organization, or bounded retrieval task to this project's luna_reader role. Use only when the user invokes $delegate-narrow-work-to-luna; never select it implicitly.
---

# Delegate narrow work to Luna

Use this Skill only after the user explicitly invokes `$delegate-narrow-work-to-luna`.

Delegate one narrow task directly to the project role `luna_reader`. Do not call `orchestrate`, do not select any other role, and do not add model or reasoning overrides in the spawn call; the role file owns those settings.

Create the child with `agent_type="luna_reader"` and `fork_turns="none"`. Give it an independent task envelope containing:

- one concrete objective;
- the exact input files or evidence boundary;
- an explicit read-only constraint;
- the compact return format;
- the acceptance check;
- the stop condition.

The child must not modify files or delegate further. Verify the compact result against the stated acceptance check. Return only the result, minimal evidence references, and any precise blocker; omit raw logs and long transcripts.
