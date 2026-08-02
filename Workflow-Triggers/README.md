# Workflow Triggers

## Workflow Dispatch

Manually execute a workflow.

```yml
on:
  workflow_dispatch:
    inputs:
      environment:
        description: Environment
        required: true
        default: DEV
```


## Scheduled Workflow

Run workflows on a defined schedule.

``cron: 0 8 * * 1``
- **`0`:** Minute 0 (the top of the hour)
- **`8`:** Hour 8 (8:00 AM in 24-hour time)
- **`*`:** Every day of the month
- **`*`:** Every month1: Monday (where 1 represents Monday and 0 or 7 represents Sunday)


```yml
on:
  schedule:
    - cron: '0 8 * * 1'
```

## Workflow Inputs

Execute a workflow with user-defined parameters.

```yaml
on:
  workflow_dispatch:
    inputs:
      environment:
        description: Environment
        required: true
        default: DEV
```


## Push Trigger

Execute automatically when there is a push to a specific branch.

```yml
on:
  push:
    branches:
      - main
```

## PullRequest Trigger

Trigger workflows during pull request validation.

```yaml
on:
  pull_request:
    branches:
      - main
```


## Manual Approval
To stop a workflow and require approval to continue.

Here, the workflow may have been triggered by:
- push
- pull request
- workflow_dispatch
- schedule

The important thing is that an **Environmental Protection Rule** exists.


1. Workflow starts
2. Job build executes
3. Job deploy is pending **Waiting for approval**
4. Approve in Environment
5. Deployment continues
