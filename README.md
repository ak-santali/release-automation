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

#### 4. Release it

```bash
npm run release
```

#### 5. Interactive mode

```
🚀 Let's release release-automation (currently at 1.0.0)

Changelog:
* Add release-it configuration (36d9004)
* Initial commit (6a9ecba)

✔ Select increment (next version): major (2.0.0)

Changeset:
 M package-lock.json
 M package.json

✔ Commit (chore: release v2.0.0)? Yes
✔ Tag (v2.0.0)? Yes
✔ Push? Yes
✔ Create a release on GitHub (Release 2.0.0)? Yes
🔗 https://github.com/ak-santali/release-automation/releases/tag/v2.0.0
🏁 Done (in 107s.)
```

#### 6. Dry run

```bash
npm run release -- --dry-run
```

OR

```bash
npm run release:dry
```
