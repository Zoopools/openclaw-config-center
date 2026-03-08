# OpenClaw 集中配置管理系统

[![ClawHub](https://img.shields.io/badge/ClawHub-openclaw--config--center-blue)](https://clawhub.com/skill/k970v8njvvtgnqc43wn5g0387h82gh6c)
[![水产市场](https://img.shields.io/badge/水产市场-OpenClaw 集中配置管理系统-orange)](https://openclawmp.cc/asset/s-4ecdf53242b788bd)

为 OpenClaw 构建集中化配置管理系统，告别硬编码和配置分散，实现"改一处，生效全局"的现代化运维体验。

**贡献家 v2.0 评分**: 8.0/10 ⭐⭐⭐⭐⭐

## 🎯 核心功能

1. **配置集中管理** - 将所有配置统一存储在 `~/.openclaw/config/` 目录
2. **动态配置读取** - 提供 `config-loader.sh` 脚本，动态读取配置
3. **主配置自动融合** - 提供 `generate-main-config.sh` 脚本，自动合并到 `openclaw.json`
4. **记忆自动同步** - 提供 `update-soul.sh` 脚本，配置修改后自动同步到 SOUL.md
5. **完整运维文档** - 包含 ARCHIVE.md、SOUL.md、故障排查指南

## 📦 安装方式

### 方式 1: 通过水产市场安装（推荐）
```bash
openclawmp install skill/@u-9e6ebb2ab773477594f5/config-center
```

### 方式 2: 通过 ClawHub 安装
```bash
clawhub install openclaw-config-center
```

### 方式 3: 手动安装
```bash
git clone https://github.com/whiteareas/openclaw-config-center.git
cd openclaw-config-center
cp -r templates/* ~/.openclaw/
```

## 🚀 快速开始

### 1. 复制配置模板
```bash
mkdir -p ~/.openclaw/config/{agents,skills,channels}
cp templates/*.example ~/.openclaw/config/
```

### 2. 修改配置
```bash
vim ~/.openclaw/config/core.json
vim ~/.openclaw/config/agents/writer.json
vim ~/.openclaw/config/channels/feishu.json
```

### 3. 生效配置
```bash
~/.openclaw/scripts/generate-main-config.sh
~/.openclaw/scripts/update-soul.sh
openclaw gateway restart --force
```

## 📊 贡献家评分

| 资产 | 通用性 | 完整性 | 独特性 | 总分 |
|------|--------|--------|--------|------|
| ARCHIVE.md 运维归档 | 9/10 | 10/10 | 8/10 | **9.1** |
| 配置中心架构 | 9/10 | 8/10 | 9/10 | **8.7** |
| 记忆同步脚本 | 8/10 | 9/10 | 9/10 | **8.7** |
| 配置加载器 | 10/10 | 7/10 | 8/10 | **8.5** |
| **平均分** | | | | **8.0/10** |

## 🔒 安全说明

⚠️ **重要**: 以下文件包含敏感信息，请勿上传到公开仓库！

```bash
# .gitignore 配置
config/channels/feishu.json
config/core.json
```

## 📝 版本历史

### v1.0.0 (2026-03-08)
- ✅ 初始版本发布
- ✅ 包含完整配置中心功能
- ✅ 贡献家 v2.0 评分 8.0/10

## 🖤 作者

- **作者**: 墨墨 (Mò) / whiteareas
- **许可**: MIT
- **最后更新**: 2026-03-08

## 📚 相关文档

- [多 Agent 配置指南](https://tbbbk.com/openclaw-multi-agent-config-guide/)
- [进阶配置教程](https://tbbbk.com/openclaw-advanced-config-guide/)
- [CLI Commands 指南](https://tbbbk.com/openclaw-cli-commands-guide/)
