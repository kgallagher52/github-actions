# GitHub Actions
  This Repo is for learning and mastering Github Actions

# Resources 
  [Udemy Course](https://getweave.udemy.com/course/github-actions-the-complete-guide/learn/lecture/34138488#overview)

  [GitHub Runners](https://docs.github.com/en/actions/using-github-hosted-runners/about-github-hosted-runners)
  - *** side note for runners you can check what comes pre installed with each runner like node js 

  [GitHub Action Triggers](https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows)

  [GitHub Marketplace for Actions](https://github.com/marketplace?type=)

  [GitHub action context](https://docs.github.com/en/actions/learn-github-actions/contexts)
# What Is CI / CD
  1. CI - Continuous Integration
        - Code changes are automatically built, tested & merged with existing code
  2. CD - Continuous Delivery
        - After integration, new app or package versions are published automatically

# GitHub Actions - Basic Building Blocks & Components

## Key Elements
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

## Events (Workflow Triggers)
### Repository-Main-Triggers
  1. push - pushing commit
  2. pull_request - pull request action
  3. create - a branch or tag was created
  4. fork - repository was forked
  5. issues - a issue was opened or deleted etc...
  6. issue_comment - issue or pull request comment action
  7. watch - repository was starred
  8. discussion - discussion action created, deleted etc...
  9. workflow_dispatch - manually trigger workflow
  10. repository_dispatch  - REST api request triggers workflow
  11. schedule - workflow is scheduled
  12. workflow_call - can be called by other workflows

## What Are Actions? 
  - A (custom) application that performs a (typically complex) frequently repeated task!
  - **uses:** is the key word for an action in the yaml
    - **with:** key word is how you define configurations (options) for an action
  - Alternatively there are **commands** such as "run" example:
      ```yaml
      run: echo "I am a command instead of a action :)"
      ```
## Adding Multiple Jobs 
  - *** Each Job has it's own VM & Runner

## Jobs in Parallel vs Sequential 
  - If you want a job to run after another job you can specify it with the needs key word
  ```yaml
      needs: test
  ```