---
name: workflow-bootstrap
description: Build a privacy-scoped workflow bundle, stage client files, require explicit approval, and verify the result in a fresh session.
---

# Workflow Bootstrap

Use the checked-in `workflow-trans` controller. Do not infer access, identity,
ownership, or persistence from the current machine.

1. Validate the supplied environment and canonical records.
2. Run only bounded, read-only probes within user-approved roots.
3. Resolve rules and build a budget-aware bundle. If mandatory content exceeds
   the budget, pause instead of silently truncating it.
4. Stage output for the selected client and show the exact import plan.
5. Apply only after the plan hash and scoped authorization reference are
   present. Preserve existing unmanaged content and create a rollback journal.
6. Verify from a fresh session. Report untested clients, operating systems, and
   accounts as `NOT_RUN`.

For browser or mobile use, generate an offline packet. Never place private
profile data, credentials, account identifiers, or machine-specific absolute
paths in the public bootstrap export.
