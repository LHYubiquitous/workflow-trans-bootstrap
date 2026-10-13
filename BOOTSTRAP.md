# Workflow Bootstrap

Use this entry to prepare a portable task bundle without assuming access to a
particular account, machine, vault, or paid provider.

1. Describe the current task and the target client.
2. Supply an environment descriptor based on `environment.example.json`.
3. Run bounded probes and generate a reviewable plan.
4. Apply only an explicitly approved plan. Keep unknown or shared machines
   session-only unless the owner authorizes broader persistence.
5. Verify behavior in a fresh session and keep unsupported combinations marked
   `NOT_RUN`.

This package contains no personal profile, credential, private repository URL,
or machine-specific absolute path. If automation is unavailable, use the
generated offline packet and follow its manual instructions.
