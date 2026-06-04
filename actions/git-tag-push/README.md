# git-tag-push

创建 tag 并推送到 origin（不 commit）。

## Inputs

| Name | Required | Description |
|---|---|---|
| `tag` | ✓ | 要创建的 tag |

## Usage

```yaml
- uses: wxyy-org/.github/actions/git-tag-push@main
  with:
    tag: "2026.06.04.0"
```
