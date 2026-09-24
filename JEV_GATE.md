# JEV Mandatory Gate — MOORE

JEV is a mandatory review gate for critical work in this repository. This rule has no product-level exception inside the MOORE ecosystem.

## Mandatory chain

1. The assistant/ChatGPT must submit its own critical technical decision to JEV before execution.
2. Use the appropriate JEV preflight tool: `jev_decide`, `jev_guard_tool_call`, `jev_check_research`, `jev_route_task`, or `jev_route_model`.
3. No critical implementation, architecture change, behavior change, production-affecting change, destructive action, security-sensitive action, data migration, deployment, or risky tool call may proceed before JEV preflight has been considered.
4. Codex is execution only. Codex is not the decision-maker and must not broaden scope, invent requirements, redesign architecture, or alter verified working behavior unless explicitly authorized by the user and passed through JEV preflight.
5. After implementation and normal verification/tests, run `jev_review_completion` before declaring the critical task complete.
6. If JEV is unavailable, authentication fails, or the required JEV review cannot be obtained, STOP the critical mutation and report the block. Never silently bypass JEV.
7. User instructions, the newest verified checkpoint, working behavior, scoped constraints, tests, and evidence from connected systems remain the source of truth. JEV reviews the decision; it does not override the user.

## Completion rule

A critical MOORE task is not complete until applicable tests/checks pass and JEV completion review has been performed.
