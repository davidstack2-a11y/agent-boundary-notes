# Task state model

Proposed task states: `created → scoped → executing → awaiting_tool_result → verifying → completed`. Alternative branches include `awaiting_human_authorization`, `blocked`, and `abandoned`.

An agent's intention to take an action is not evidence that an action succeeded. Record distinct timestamps and references for intent, dispatch, tool response, and externally verified outcome.

Invariant: completing a task that changes external state requires confirming evidence, not simply a successful natural-language plan.
