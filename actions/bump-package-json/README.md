# bump-package-json

更新 `package.json` 中的 `version`、`repository` 和 `homepage`。

## Inputs

| Name | Required | Description |
|---|---|---|
| `version` | ✓ | 要写入的版本号（semver） |

## Usage

```yaml
- uses: wxyy-org/.github/actions/bump-package-json@main
  with:
    version: "2026.6.4-0"
```
