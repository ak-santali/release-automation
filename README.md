# release-automation

Release automation using release-it

```bash
npm init -y
```

### Steps

#### 1. Install release it

```bash
npm i -D release-it
```

#### 2. Create `.release-it.json` configuration file.

```json
{
  "git": {
    "commitMessage": "chore: release v${version}",
    "tagName": "v${version}"
  },
  "github": {
    "release": true
  },
  "npm": {
    "publish": false
  }
}
```

#### 3. Generate and export github token

```bash
export GITHUB_TOKEN="ghp_fMOBxoFjphqx5pv9Qq5BN1KymnpgYK1AgW3"
```
