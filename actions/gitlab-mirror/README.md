# gitlab-mirror

将当前仓库全量镜像推送到 GitLab（含裁剪过时分支）。

## Inputs

| Name | Required | Description |
|---|---|---|
| `gitlab_host` | ✓ | GitLab 实例地址，如 `https://gitlab.example.com` |
| `gitlab_repo` | ✓ | GitLab 上的 `group/repo`（不含 .git） |
| `gitlab_token` | ✓ | GitLab OAuth2 Token |

## Usage

```yaml
- uses: wxyy-org/.github/actions/gitlab-mirror@main
  with:
    gitlab_host: https://gitlab.example.com
    gitlab_repo: group/repo
    gitlab_token: ${{ secrets.GITLAB_TOKEN }}
```
