# SADP 智能教育系统

一个集成了多种AI智能体的教育辅助系统，提供学习伴侣、编程教练和教学助手三大核心功能，帮助提升学习和教学体验。

## 系统功能

### 1. SADP智能伴学（Learning Companion）
- 提供学习资料解析与问答
- 支持文档、图片内容理解
- 智能问题生成与解答

### 2. SADP智能代码编程教练（Coding Coach）
- 代码分析与优化建议
- 设计模式识别与应用
- 编程问题诊断与解决方案

### 3. SADP教学伴侣（Teaching Assistant）
- 教学计划生成
- 学习目标与策略制定
- 教学内容与评估方法推荐

## 快速开始

### 本地运行

1. 确保您的电脑已安装以下软件：
   - 现代浏览器（Chrome、Firefox、Edge等）
   - Python 3.x（可选，用于启动本地服务器）

2. 克隆或下载本项目到本地

3. 启动本地服务器（二选一）：

   **使用Python（推荐）**：
   ```bash
   # 在项目根目录运行
   python -m http.server 8000
   ```

   **使用Node.js**：
   ```bash
   # 首先安装http-server
   npm install -g http-server
   # 在项目根目录运行
   http-server -p 8000
   ```

4. 打开浏览器，访问：`http://localhost:8000`

5. 根据您的角色选择进入：
   - 学生端：`http://localhost:8000/student.html`
   - 教师端：`http://localhost:8000/teacher.html`

## 系统架构

- **前端技术**：HTML5, CSS3, JavaScript
- **智能体集成**：Coze Web SDK
- **可视化**：Mermaid.js 流程图
- **响应式设计**：适配不同屏幕尺寸

## 部署说明

### 部署到静态网站托管服务

您可以将本项目部署到任何支持静态网站的托管服务，如：

- GitHub Pages
- Netlify
- Vercel
- Cloudflare Pages

部署步骤（以GitHub Pages为例）：

1. 创建GitHub仓库并上传代码
2. 在仓库设置中启用GitHub Pages
3. 选择主分支作为源
4. 等待部署完成

## 开源协议

本项目采用 MIT 许可证开源，您可以自由使用、修改和分享。

## 注意事项

- 系统中使用的Coze智能体需要有效的token才能正常工作
- 确保在公网部署时保护好API密钥信息
- 所有智能体已配置为嵌入模式，并支持全屏聊天功能

## 贡献指南

欢迎提交Issue和Pull Request来改进本系统！

## 联系我们

如有任何问题或建议，请通过以下方式联系我们：
- 项目仓库：[项目链接]
- 电子邮件：[联系邮箱]