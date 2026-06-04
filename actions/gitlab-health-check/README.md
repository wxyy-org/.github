# gitlab-health-check

检测 GitLab 实例是否可达。

## Inputs

| Name | Required | Description |
|---|---|---|
| `gitlab_host` | ✓ | GitLab 实例地址，如 `https://gitlab.example.com` |

## Outputs

| Name | Description |
|---|---|
| `reachable` | `true` 或 `false` |

## Usage

```yaml
- uses: wxyy-org/.github/actions/gitlab-health-check@main
  id: check
  with:
    gitlab_host: https://gitlab.example.com

- run: echo "${{ steps.check.outputs.reachable }}"
```
