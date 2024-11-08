# Cloudflare R2 到 GitHub 文件迁移工具

这个 GitHub Action 用于将 Cloudflare R2 存储中的文件迁移到 GitHub 仓库，支持根据策略选择文件的迁移目标仓库。支持按照文件大小或文件数量的策略进行选择，支持迁移后删除 R2 中的文件。

## 功能

- 从 Cloudflare R2 存储中获取文件列表。
- 根据配置文件中的策略将文件迁移到指定的 GitHub 仓库。
- 支持两种策略：根据仓库文件数量或仓库大小选择目标仓库。
- 支持迁移后删除 R2 中的文件。

## 使用说明
```
    - name: Sync files to GitHub
      continue-on-error: true
      uses: fscarmen2/r2_to_github@v1.0.0
      with:
        config_path: < 用户配置文件存放路径，不填则默认: ./config.yml >
```