# renovate-config

Shared Renovate config for @enjoyjs projects

## Features

- Use Asia/Tokyo timezone by default
- Automerge patch and minor upgrades if they pass tests
- If automerging, push the new commit directly to base branch (no PR)
- Wait until branch tests have passed or failed before creating the PR
- If semantic commits detected, use semantic commit type `build` for all
- Apply label `dependencies` to PRs
- Set a status check pending for 3 days from release timestamp to guard against npm unpublishing
- Schedule for weekends

## Setup

`.github/renovate.json`

```json
{
  "extends": ["github>enjoyjs/renovate-config"]
}
```
