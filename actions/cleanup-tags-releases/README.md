# cleanup-tags-releases

清理旧 tag / release，保留最近 N 个。

- 私有仓库：仅清理 tag
- 公开仓库：清理 release + tag

## Inputs

| Name | Required | Description |
|---|---|---|
| `keep` | ✓ | 保留最近的数量 |
| `public_repo` | - | 公开仓库（owner/repo），留空则跳过 |
| `token` | ✓ | GitHub token（需公开仓库 delete 权限） |

## Usage

```yaml
- uses: wxyy-org/.github/actions/cleanup-tags-releases@main
  with:
    keep: 5
    public_repo: owner/release-repo
    token: ${{ secrets.RELEASES_TOKEN }}
```
