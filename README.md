# Google AI Studio Helper

一个功能强大的油猴脚本，为 Google AI Studio 提供三大核心功能，全面提升使用体验。

## 🚀 功能特性

### 1. 从此处删除 (Delete From Here)
- **一键批量删除**：在任意对话回合添加"❌"按钮，点击即可删除该回合及之后的所有对话
- **智能删除机制**：支持快速删除和备用删除方法，确保删除操作的可靠性
- **安全确认**：删除前会弹出确认对话框，防止误操作
- **视觉反馈**：删除过程中会高亮显示即将删除的回合

### 2. 自动中文输出
- **智能检测**：自动检测系统指令区域，如果未包含中文输出指令则自动添加
- **无缝集成**：自动在系统指令中添加"你始终用中文输出"
- **防重复添加**：智能检测已有指令，避免重复添加
- **实时监控**：持续监控页面变化，确保新会话也能自动应用中文输出

### 3. HTML 预览功能
- **一键预览**：为 HTML 代码块添加预览按钮（👁️图标）
- **模态窗口**：在弹出窗口中实时预览 HTML 效果
- **安全渲染**：使用 Trusted Types 策略确保安全的 HTML 渲染
- **响应式设计**：预览窗口支持响应式布局，适配不同屏幕尺寸

## 📦 安装方法

### 前置要求
- 浏览器需要安装 [Tampermonkey](https://www.tampermonkey.net/) 或其他用户脚本管理器

### 安装步骤
1. 点击 [安装链接](https://update.greasyfork.org/scripts/549116/Google%20AI%20Studio%20Helper.user.js)
2. 在弹出的 Tampermonkey 安装页面点击"安装"
3. 访问 [Google AI Studio](https://aistudio.google.com/) 即可使用

## 🎯 使用指南

### 从此处删除功能
1. 在任意对话回合右上角找到"❌"按钮
2. 点击按钮，确认删除操作
3. 脚本会自动删除该回合及之后的所有对话

### 自动中文输出功能
- **自动运行**：无需手动操作，脚本会自动检测并添加中文输出指令
- **手动检查**：可以点击"System instructions"查看是否已添加指令

### HTML 预览功能
1. 找到包含 HTML 代码的代码块
2. 点击代码块右上角的预览按钮（👁️图标）
3. 在弹出的模态窗口中查看 HTML 效果
4. 按 ESC 键或点击关闭按钮退出预览

## ⚙️ 技术特性

- **模块化设计**：三个功能模块独立运行，互不干扰
- **智能观察器**：使用 MutationObserver 实时监控页面变化
- **错误处理**：完善的错误处理机制，确保脚本稳定运行
- **性能优化**：防抖机制和智能缓存，减少不必要的操作
- **兼容性强**：支持中英文界面，适配不同语言环境

## 🔧 配置选项

脚本内置了以下可配置常量：

```javascript
// 聊天回合元素选择器
const CHAT_TURN_SELECTOR = 'ms-chat-turn';

// 选项按钮选择器（支持中英文）
const OPTIONS_BUTTON_SELECTOR = 'button[aria-label="Open options"], button[aria-label="打开选项"]';

// 聊天会话容器选择器
const CHAT_SESSION_SELECTOR = 'ms-chat-session';
```

## 🐛 故障排除

### 删除功能不工作
- 确保页面完全加载后再使用
- 检查是否为最后一个对话回合（Google AI Studio 限制不能删除最后一个回合）
- 刷新页面重试

### 中文输出功能无效
- 检查系统指令区域是否可编辑
- 手动点击"System instructions"查看指令内容
- 清除浏览器缓存后重试

### HTML 预览无法显示
- 确保代码块被正确识别为 HTML 类型
- 检查 HTML 代码语法是否正确
- 尝试刷新页面

## 📝 更新日志

### v2.1
- 整合三大功能模块
- 优化删除机制，提高成功率
- 修复 HTML 预览的安全性问题
- 改进自动中文输出的稳定性

## 📄 许可证

MIT License - 详见 [LICENSE](LICENSE) 文件

## 👨‍💻 作者

**Chris_C**

## 🔗 相关链接

- [Greasyfork 页面](https://greasyfork.org/scripts/549116)
- [更新地址](https://update.greasyfork.org/scripts/549116/Google%20AI%20Studio%20Helper.user.js)
- [Google AI Studio](https://aistudio.google.com/)

## 🤝 贡献

欢迎提交 Issue 和 Pull Request 来改进这个脚本！

---

**注意**：本脚本仅在 Google AI Studio 官方网站上运行，请确保从可信来源安装。