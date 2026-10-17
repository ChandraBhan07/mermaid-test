# Job Manager Workflow

This diagram describes how the job manager processes incoming jobs,
handles failures and retries, records job history, and schedules jobs
for the outgoing queue.

## Workflow diagram

[View Mermaid source](./diagrams/job-manager.mmd)

## Processing logic

1. Wait for an incoming job.
2. Remove a job from the incoming queue.
3. Check its state and retry attempts.
4. Record successful jobs and exhausted failures in job history.
5. Schedule eligible jobs and send them to the outgoing queue.
