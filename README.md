# gh-redeliver-webhook-pr-close

Redeliver Most Recent GitHub Close PR Webhook Delivery for the current branch.

## Usage

```bash
gh redeliver-webhook-pr-close <webhook-url> [flags]

FLAGS
  --dry-run   Do not actually redeliver, just print what would be done.

EXAMPLES
  $ gh redeliver-webhook-pr-close https://example.com/webhook
  $ gh redeliver-webhook-pr-close https://example.com/webhook --dry-run
```

### Find your `webhook-url`

You can get a list of the webhook URLs for your repository by running:

```bash
gh api "/repos/{owner}/{repo}/hooks" --jq '.[].config.url'
```

