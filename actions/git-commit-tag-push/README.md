# git-commit-tag-push

提交 `package.json` 变更、打 tag 并推送。

## Inputs

| Name | Required | Description |
|---|---|---|
| `tag` | ✓ | 要创建的 tag |
| `commit_message` | ✓ | 提交信息 |

## Usage

```yaml
- uses: wxyy-org/.github/actions/git-commit-tag-push@main
  with:
    tag: "2026.06.04.0"
    commit_message: "release: 2026.06.04.0"
```
