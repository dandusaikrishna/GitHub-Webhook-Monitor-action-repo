# GitHub Action Repo (action-repo)

This repository contains GitHub Actions workflows that send webhook events to the webhook-repo.

## Workflow

- Triggers on push and pull request events.
- Sends the event payload to the configured webhook endpoint.

## Setup

1. Create a repository secret named `WEBHOOK_URL` with the URL of your webhook-repo `/webhook` endpoint, e.g. `http://your-server:5000/webhook`.

2. Commit and push changes to trigger the workflow.

## Notes

- The workflow uses `curl` to POST the event payload with the `X-GitHub-Event` header.
- Supports push and pull request events.
- Merge events are handled as part of pull request events.

## License

MIT License
