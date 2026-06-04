# sync-readme-gh

使用 gh CLI 将 README 源文件同步到目标仓库。

## Inputs

| Name | Required | Description |
|---|---|---|
| `readme_source` | ✓ | README 源文件路径（相对于 workspace） |
| `target_repo` | ✓ | 目标仓库（owner/repo） |
| `tag` | ✓ | 当前 tag，用于 commit message |
| `token` | ✓ | GitHub token |

## Usage

```yaml
- uses: wxyy-org/.github/actions/sync-readme-gh@main
  with:
    readme_source: docs/README.md
    target_repo: owner/release-repo
    tag: "2026.06.04.0"
    token: ${{ secrets.GITHUB_TOKEN }}
```
