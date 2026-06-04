# calver-tag

生成 CalVer 标签（`YYYY.MM.DD.N`）及对应 semver（`YYYY.M.D-N`）。

## Inputs

| Name | Required | Description |
|---|---|---|
| `timezone` | ✓ | 时区，如 `Asia/Shanghai` |

## Outputs

| Name | Description | 示例 |
|---|---|---|
| `tag` | CalVer 标签 | `2026.06.04.0` |
| `semver` | 对应 semver | `2026.6.4-0` |

## Usage

```yaml
- uses: wxyy-org/.github/actions/calver-tag@main
  id: calver
  with:
    timezone: Asia/Shanghai

- run: echo "${{ steps.calver.outputs.tag }}"
```
