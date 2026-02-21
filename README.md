# Misskey Theme Editor

🎨 一个可视化的 Misskey 主题编辑器，支持实时调整颜色、深浅模式切换，并导出符合 Misskey 格式的主题配置。

## ✨ 功能特性

- **实时颜色编辑**：左侧面板列出所有主题变量（含中文注释），可自由调整基础颜色，所有派生变量（如 `lighten`, `alpha`, `hue`）自动重新计算。
- **深浅模式一键切换**：内置深色/浅色两套预设，切换后所有颜色重新生成，方便对比。
- **流畅调色体验**：颜色选择器支持拖拽实时预览，面板不会消失，焦点不丢失。
- **导出配置**：点击按钮即可生成符合 Misskey 原生格式的主题配置文件（键值对形式），可直接复制使用。
- **复制颜色值**：点击色块可快速复制当前颜色值。
- **完全客户端运行**：纯 HTML/JavaScript，无需后端，可直接在浏览器中运行。

## 📦 使用方法

### 1. 本地运行
**Linux系统** 克隆本仓库：
```bash
git clone https://github.com/your-username/misskey-theme-editor.git
```
**Windows系统** 浏览器下载misskey-theme-editor.html

然后用浏览器打开 `misskey-theme-editor.html` 即可。

### 2. 在线DEMO
**本站DEMO：** https://mktheme-editor.captraw.com

**若页面显示异常请换用更新的浏览器**

## 🔧 主要功能
- 左侧面板列出了所有 Misskey 主题变量，带有中文注释。
- **基础颜色**（如 `accent`, `bg`, `fg`）右侧带有颜色选择器，可随意调整。
- **派生颜色**（如 `panel`, `buttonBg`）会自动跟随基础色变化，不可直接编辑。
- 点击上方“深色/浅色”按钮可切换整体风格。
- 调整完成后，点击底部“📤 导出当前配置”即可复制生成的配置代码。

## 🧠 主题配置说明

编辑器完全兼容 Misskey 的主题格式，支持以下函数：
- `:lighten<amount<@color` — 提高亮度
- `:alpha<amount<@color` — 调整透明度
- `:hue<degrees<@color` — 色相偏移

所有变量间相互引用，最终会计算出具体的颜色值（HEX 或 RGBA）。

## 🛠️ 技术栈

- 原生 HTML / CSS / JavaScript（无任何依赖）
- CSS 变量实现主题动态更新
- 颜色转换与解析逻辑纯手工实现

## 🤝 贡献指南

欢迎提交 Issue 或 Pull Request！如果你有好的想法或发现了 Bug，请随时提出。

1. Fork 本仓库
2. 创建你的特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交修改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 打开一个 Pull Request

## 📄 许可证

本项目基于 Apache 2.0 许可证开源。
