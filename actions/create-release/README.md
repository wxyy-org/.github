# create-release

在指定仓库创建 GitHub Release。

## Inputs

| Name | Required | Description |
|---|---|---|
| `tag` | ✓ | tag 名称 |
| `name` | ✓ | Release 名称 |
| `body` | ✓ | Release body（Markdown） |
| `repository` | ✓ | 目标仓库（owner/repo） |
| `token` | ✓ | GitHub token |

## Usage

```yaml
- uses: wxyy-org/.github/actions/create-release@main
  with:
    tag: "2026.06.04.0"
    name: "Release 2026.06.04.0"
    body: "## Changes\n- ..."
    repository: "owner/repo"
    token: ${{ secrets.GITHUB_TOKEN }}
```
