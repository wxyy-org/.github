# .github

跨仓库共享的 GitHub Actions 组件。

## Workflows（可复用工作流）

| Workflow | 说明 |
|---|---|
| `sync-to-gitlab` | 将 GitHub 仓库全量镜像到 GitLab（先检测 GitLab 可达性，不可达时跳过） |

```yaml
# 在子仓库中调用
jobs:
  sync:
    uses: wxyy-org/.github/.github/workflows/sync-to-gitlab@main
    with:
      gitlab_repo: "group/repo"
    secrets:
      GITLAB_TOKEN: ${{ secrets.GITLAB_TOKEN }}
```

## Actions（复合动作）

| Action | 说明 |
|---|---|
| `calver-tag` | 生成 CalVer 标签（YYYY.MM.DD.N）及对应 semver，输出 `tag` 和 `semver` |
| `bump-package-json` | 更新 package.json 中的 version、repository 和 homepage |
| `git-commit-tag-push` | 提交 package.json 变更、打 tag 并推送 |
| `git-tag-push` | 仅创建 tag 并推送（不 commit） |
| `create-release` | 在指定仓库创建 GitHub Release |
| `cleanup-tags-releases` | 清理旧 tag / release，保留最近 N 个（公开仓库清理 release+tag，私有仓库仅清理 tag） |
| `sync-readme` | 将 README 源文件同步到发布仓库（git 操作） |
| `sync-readme-gh` | 使用 gh CLI 将 README 源文件同步到目标仓库 |
| `gitlab-mirror` | 全量镜像推送到 GitLab（含裁剪过时分支） |
| `gitlab-health-check` | 检测 GitLab 实例是否可达，输出 `reachable` |

### 典型组合方式

calver-tag → bump-package-json → git-commit-tag-push → create-release → cleanup-tags-releases

```
wxyy-org/.github/actions/calver-tag@main
wxyy-org/.github/actions/bump-package-json@main
wxyy-org/.github/actions/git-commit-tag-push@main
wxyy-org/.github/actions/create-release@main
wxyy-org/.github/actions/cleanup-tags-releases@main
```
