# 🌟 天翼云盘自动签到工具

<div align="center">

[![云盘签到](https://github.com/dext7r/189pan/actions/workflows/main.yml/badge.svg)](https://github.com/dext7r/189pan/actions/workflows/main.yml) 
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/python-3.8+-green.svg)](https://python.org)

**🚀 自动化天翼云盘签到，每日获取免费存储空间**

</div>

---

## 📊 功能特性

- 🎯 **自动签到** - 每日定时自动签到，无需手动操作
- 🎲 **智能抽奖** - 签到后自动参与抽奖活动
- 📈 **容量统计** - 实时显示获得的存储容量
- 🌐 **在线展示** - 通过GitHub Pages展示签到记录
- 🔄 **多账户支持** - 支持配置多个天翼云盘账户

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

### ⚙️ 自定义时间
修改 `.github/workflows/main.yml` 中的 cron 表达式：
```yaml
schedule:
  - cron: '30 1,13 * * *'  # UTC时间，对应北京时间 09:30 和 21:30
```

### 🔗 多账户配置
支持配置多个账户，在Secrets中添加：
```
TYYP_USERNAME: 账户1手机号&账户2手机号
TYYP_PSW: 账户1密码&账户2密码
```

---

## 🆘 故障排除

| 问题类型 | 解决方案 |
|----------|----------|
| 🚫 签到失败 | 检查用户名密码是否正确 |
| 📄 页面无法访问 | 确认GitHub Pages已启用 |
| ⏰ 执行时间异常 | 检查cron表达式配置 |
| 🔐 权限错误 | 确认Secrets配置正确 |

---

## 📁 项目结构

```
189pan/
├── main.py              # 核心签到脚本
├── requirements.txt     # Python依赖
├── _config.yml         # Jekyll配置
├── README.md           # 项目说明
└── .github/
    └── workflows/
        └── main.yml    # GitHub Actions工作流
```

---

## 🤝 贡献

欢迎提交Issue和Pull Request来改进项目！

---

## 🙏 致谢

- 感谢 [qsf728999746](https://github.com/qsf728999746) 提供的原始项目
- 感谢所有贡献者的支持和改进建议

---

<div align="center">

**⭐ 如果这个项目对您有帮助，请给个Star支持一下！**

</div>
