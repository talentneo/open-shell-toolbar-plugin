# 自动化发布说明

## GitHub Actions 自动发布流程

本项目已配置 GitHub Actions，当代码推送到 `main` 分支时会自动：

1. **自动递增版本号** - 补丁版本（第三位）自动 +1
   - 例如：`1.0.0` → `1.0.1`

2. **创建 Git 标签** - 自动生成并推送版本标签
   - 格式：`v{版本号}`，如 `v1.0.1`

3. **创建 GitHub Release** - 自动生成发布版本
   - 包含版本信息和变更说明

## 工作流程

```yaml
触发条件：push 到 main 分支
↓
检出代码
↓
设置 Node.js 环境
↓
读取当前版本号
↓
递增补丁版本 (1.0.0 → 1.0.1)
↓
更新 package.json
↓
提交并推送版本变更
↓
创建并推送 Git 标签
↓
创建 GitHub Release
```

## 使用方法

### 本地开发
```bash
# 开发测试
npm start

# 部署到 GitHub
npm run deploy
```

### 自动发布
只需将代码推送到 main 分支：
```bash
git add .
git commit -m "feat: your changes"
git push origin main
```

GitHub Actions 会自动处理版本发布！

## 配置文件

- `.github/workflows/auto-release.yml` - GitHub Actions 工作流配置
- `package.json` - 项目版本信息

## 注意事项

1. 确保有权限推送到 main 分支
2. GitHub Actions 会自动使用 `GITHUB_TOKEN` 创建 Release
3. 每次推送到 main 都会触发新版本发布
4. 版本号格式：`主版本。次版本。补丁版本` (MAJOR.MINOR.PATCH)
