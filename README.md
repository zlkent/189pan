# 🌟 天翼云盘自动签到工具

<div align="center">

[![云盘签到](https://github.com/dext7r/189pan/actions/workflows/main.yml/badge.svg)](https://github.com/dext7r/189pan/actions/workflows/main.yml) 
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/python-3.8+-green.svg)](https://python.org)

**🚀 自动化天翼云盘签到，每日获取免费存储空间**

[📖 使用指南](#-使用指南) • [⚡ 快速开始](#-快速开始) • [🔧 配置说明](#-配置说明) • [📊 功能特性](#-功能特性)

</div>

---

## 📊 功能特性

### ✨ 核心功能
- 🎯 **自动签到** - 每日定时自动签到，无需手动操作
- 🎲 **智能抽奖** - 签到后自动参与抽奖活动
- 📈 **容量统计** - 实时显示获得的存储容量
- 🌐 **在线展示** - 通过GitHub Pages展示签到记录
- 🔄 **多账户支持** - 支持配置多个天翼云盘账户

### 🛠️ 技术特性
- ⚡ **现代化CI/CD** - 使用最新GitHub Actions v4/v5
- 🔒 **安全可靠** - 密码加密存储，安全登录验证
- 📱 **响应式设计** - 签到页面支持移动端访问
- 🚨 **智能监控** - 自动错误检测和通知
- 📝 **详细日志** - 完整的签到和抽奖记录

---

## 🎉 项目改进

> 本项目基于 [Cloud189_Action](https://github.com/qsf728999746/Cloud189_Action) 进行了全面优化和改进

### 🔧 修复内容

| 问题 | 状态 | 说明 |
|------|------|------|
| 🎲 抽奖容量显示异常 | ✅ **已修复** | 正确显示获得的容量数值 |
| 🔐 敏感信息泄露 | ✅ **已修复** | 隐藏sessionKey等敏感信息 |
| 📊 数据展示优化 | ✅ **已完成** | 通过GitHub Pages美化展示 |

### 🚀 新增功能

- 🎨 **美化界面** - 现代化的签到记录展示页面
- 📈 **数据统计** - 签到成功率和容量获取统计
- 🔔 **状态通知** - 实时的执行状态和结果反馈
- ⚙️ **配置优化** - 简化的部署和配置流程

---

## ⚡ 快速开始

### 1️⃣ Fork 仓库
点击右上角 **Fork** 按钮，将项目复制到您的GitHub账户

### 2️⃣ 配置密钥
在您的仓库中设置以下Secrets：

```
Settings → Secrets and variables → Actions → New repository secret
```

| 密钥名称 | 说明 | 示例 |
|----------|------|------|
| `TYYP_USERNAME` | 天翼云盘手机号 | `13800138000` |
| `TYYP_PSW` | 天翼云盘密码 | `your_password` |

### 3️⃣ 启用GitHub Pages
```
Settings → Pages → Source → GitHub Actions
```

### 4️⃣ 手动测试
```
Actions → 选择工作流 → Run workflow
```

---

## 🔧 配置说明

### 📅 执行时间
默认执行时间（北京时间）：
- 🌅 **上午 09:30** - 第一次签到
- 🌙 **晚上 21:30** - 第二次签到
- 📄 **上午 13:35 & 下午 01:35** - GitHub Pages更新

### ⚙️ 自定义时间
修改 `.github/workflows/main.yml` 中的 cron 表达式：
```yaml
schedule:
  - cron: '30 1,13 * * *'  # 签到时间：UTC时间，对应北京时间 09:30 和 21:30
  - cron: '35 5,17 * * *'  # 页面更新时间
```

### 🎯 手动执行
支持手动选择执行任务：
1. 进入 Actions 页面
2. 选择 "天翼云盘签到" 工作流
3. 点击 "Run workflow"
4. 选择任务类型：
   - `checkin` - 仅执行签到
   - `pages` - 仅更新页面
   - `both` - 执行签到并更新页面

### 🔗 多账户配置
支持配置多个账户，在Secrets中添加：
```
TYYP_USERNAME_2, TYYP_PSW_2
TYYP_USERNAME_3, TYYP_PSW_3
...
```

---

## 📖 使用指南

### 📚 详细文档
- 📋 [GitHub Actions升级指南](ACTIONS_UPGRADE_GUIDE.md)
- 🔧 [详细配置教程](action.md)
- 🌐 [项目Wiki](https://github.com/y377/189pan/wiki)

### 🆘 故障排除
遇到问题？查看我们的故障排除指南：

| 问题类型 | 解决方案 |
|----------|----------|
| 🚫 签到失败 | 检查用户名密码是否正确 |
| 📄 页面无法访问 | 确认GitHub Pages已启用 |
| ⏰ 执行时间异常 | 检查cron表达式配置 |
| 🔐 权限错误 | 确认Secrets配置正确 |

---

## 🤝 贡献

欢迎提交Issue和Pull Request来改进项目！

### 🎯 贡献指南
1. Fork 项目
2. 创建功能分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启Pull Request

---

## 📄 许可证

本项目采用 MIT 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情

---

## 🙏 致谢

- 感谢 [qsf728999746](https://github.com/qsf728999746) 提供的原始项目
- 感谢所有贡献者的支持和改进建议

---

<div align="center">

**⭐ 如果这个项目对您有帮助，请给个Star支持一下！**

Made with ❤️ by [Your Name](https://github.com/yourusername)

</div>
