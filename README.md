# spacelift_tf_test


## Spacelift notes

- Spacelift is based on **stacks** (single tf state file)
- **Tracked runs** (deployments)
  - you can lock the stack for maintenance
- **Tasks** let you run arbitrary commands within your terraform state (destroy, import resources)
- **PRs** are natively supported + proposed runs are previewed (what would happen if you merged it)
  - can be visible within GitHub in the actual PR
- **Policies**
  - __login policies__ - who accessed spacelift
  - __access policy__ - who can get read access on the stack
  - __plan policy__ - check the plan for various rules and deny/continue run
    - No passwords 
  - __task policy__ - only execute whitelisted commands
  - __push policy__ - customize the git flow (be notified for all commits/PRs)
    - should you create a proposed/tracked run
  - __trigger policies__ - to build arbitrary workflows on top of spacelift