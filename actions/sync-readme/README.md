# sync-readme

将 README 源文件同步到发布仓库（git 操作）。

## Inputs

| Name | Required | Description |
|---|---|---|
| `readme_source` | ✓ | README 源文件路径（相对于 workspace） |
| `release_repo_url` | ✓ | 发布仓库的 clone URL（不含 token） |
| `tag` | ✓ | 当前 tag，用于 commit message |
| `token` | ✓ | 发布用的 token |

## Usage

```yaml
- uses: wxyy-org/.github/actions/sync-readme@main
  with:
    readme_source: docs/README.md
    release_repo_url: https://github.com/owner/release-repo.git
    tag: "2026.06.04.0"
    token: ${{ secrets.RELEASES_TOKEN }}
```
