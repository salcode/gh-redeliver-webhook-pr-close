# gh-redeliver-webhook-pr-close

[GitHub CLI extension](https://docs.github.com/en/github-cli/github-cli/using-github-cli-extensions) to redeliver the most recent GitHub close PR webhook delivery for the current branch.

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

### Installation

After installing the [GitHub CLI](https://cli.github.com/), you can install this extension using the following command:

```bash
gh extension install salcode/gh-redeliver-webhook-pr-close
```
