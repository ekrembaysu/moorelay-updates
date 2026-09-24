# MOORE Agent Rules

Read `JEV_GATE.md` before any critical work.

Mandatory rule: the assistant's own critical technical decisions must pass JEV preflight before execution. Codex is execution-only. No critical mutation, deployment, destructive action, behavior change, architecture change, security-sensitive action, or risky tool call may proceed without the applicable JEV review.

If JEV is unavailable or authentication/review fails, STOP and report the block. Do not bypass JEV.

After implementation and normal verification/tests, run `jev_review_completion` before declaring a critical task complete.

User instructions, the newest verified checkpoint, existing working behavior, scoped constraints, tests, and connected-system evidence remain the source of truth.
