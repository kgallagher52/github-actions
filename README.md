# github-actions

  This Repo is for learning and mastering Github Actions/Workflows

# Resources 
[Udemy Course](https://www.electronjs.org/docs/latest/api/web-frame)

# What Is CI / CD
1. CI - Continuous Integration
    - Code changes are automatically built, tested & merged with existing code
2. CD - Continuous Delivery
    - After integration, new app or package versions are published automatically

# GitHub Actions - Basic Building Blocks & Components

## Key Elements

- Hierarchy: workflows > jobs > steps

1. Workflows
  - Attached to a repository 
  - Has one or more **jobs**
  - Triggered upon **Events**
2. Jobs
  - Define a **Runner** (execution environment)
  - Contain one or more **Steps** 
  - Run in parallel (default) or sequential
  - Can be conditional
3. Steps
  - Execute a **shell script** or an **Action**
  - Can use custom or third-party actions
  - Steps are executed in order
  - Can be conditional 

- Private repositories have monthly usage is available for free. Public repositories are free

