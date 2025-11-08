# SADP 智能教育系统

一个集成了多种AI智能体的教育辅助系统，提供学习伴侣、编程教练和教学助手三大核心功能，帮助提升学习和教学体验。该系统基于现代Web技术开发，可通过任何静态网站托管服务进行部署，方便用户免费使用。

## 系统功能

### 1. SADP智能伴学（Learning Companion）
- 提供学习资料解析与问答
- 支持文档、图片内容理解
- 智能问题生成与解答
- **支持全屏聊天模式**，提供沉浸式学习体验

### 2. SADP智能代码编程教练（Coding Coach）
- 代码分析与优化建议
- 设计模式识别与应用
- 编程问题诊断与解决方案
- **支持全屏聊天模式**，方便展示代码和详细解释

### 3. SADP教学伴侣（Teaching Assistant）
- 教学计划生成
- 学习目标与策略制定
- 教学内容与评估方法推荐
- **支持全屏聊天模式**，便于详细讨论教学方案

## 快速开始

### 本地运行

1. 确保您的电脑已安装以下软件：
   - 现代浏览器（Chrome、Firefox、Edge等）
   - Python 3.x（可选，用于启动本地服务器）
   - Node.js（可选，另一种启动服务器的方式）

2. 克隆或下载本项目到本地

3. 启动本地服务器（三选一）：

   **使用Python（推荐）**：
   ```bash
   # 在项目根目录运行
   python -m http.server 8080
   ```

   **使用Node.js**：
   ```bash
   # 首先安装http-server
   npm install -g http-server
   # 在项目根目录运行
   http-server -p 8080
   ```
   
   **使用Windows批处理脚本（可选）**：
   ```bash
   # 双击运行项目根目录下的deploy.bat文件
   ```

4. 打开浏览器，访问：`http://localhost:8080`（Python和Node.js方式）或`http://localhost:8000`（Windows批处理脚本方式）

5. 根据您的角色选择进入：
   - 学生端：`http://localhost:8080/student.html`
   - 教师端：`http://localhost:8080/teacher.html`

## 系统架构

- **前端技术**：HTML5, CSS3, JavaScript
- **智能体集成**：Coze Web SDK (嵌入式模式)
- **可视化**：Mermaid.js 流程图
- **响应式设计**：适配不同屏幕尺寸
- **布局特点**：智能体嵌入右侧面板，支持600px宽度自适应

## 部署说明

### 1. 静态网站托管
该系统是一个纯静态网站，可以部署到任何静态网站托管服务，例如：
- GitHub Pages (免费)
- Netlify (免费)
- Vercel (免费)
- Cloudflare Pages (免费)
- 阿里云OSS
- 腾讯云COS

#### GitHub Pages部署详细步骤

1. 创建一个新的GitHub仓库
2. 将项目文件上传到仓库
3. 进入仓库的"Settings"页面
4. 向下滚动到"GitHub Pages"部分
5. 在"Source"下拉菜单中选择"main"或"master"分支
6. 点击"Save"按钮
7. GitHub将自动构建和部署你的网站
8. 部署完成后，你将看到一个URL，可以通过该URL访问你的网站

#### Netlify部署详细步骤

1. 访问Netlify官网(https://www.netlify.com/)并注册账号
2. 点击"New site from Git"
3. 选择GitHub并授权
4. 选择你的项目仓库
5. 点击"Deploy site"
6. Netlify将自动部署你的网站并提供一个URL

#### Vercel部署详细步骤

1. 访问Vercel官网(https://vercel.com/)并注册账号
2. 点击"Import Project"
3. 选择"Import Git Repository"
4. 连接GitHub账号并选择你的项目仓库
5. 点击"Deploy"
6. Vercel将自动部署你的网站并提供一个URL

### 2. 发布到Coze平台

SADP智能教育系统使用了Coze SDK集成智能体，您可以将单个智能体发布到Coze平台供更广泛的用户使用：

#### 步骤：
1. 登录Coze官网(https://www.coze.cn/)
2. 进入Coze Studio创建或导入您的智能体
3. 配置智能体的功能和知识库
4. 在发布设置中选择发布方式：
   - **发布到Coze商城**：供其他用户发现和使用
   - **发布为API服务**：通过API密钥调用
   - **发布为Web SDK**：目前系统已使用此方式集成
   - **发布到社交平台**：如微信公众号、抖音等

#### 注意事项：
- 发布到Coze平台需要单独创建每个智能体
- 您需要更新系统中的bot_id以匹配在Coze平台上发布的智能体ID
- Coze平台提供免费和付费版本，根据使用量可能产生费用

### 3. 发布到通义千问(Qwen)平台

您也可以将系统发布到阿里云的通义千问平台：

#### 步骤：
1. 访问通义千问官网(https://tongyi.aliyun.com/)
2. 注册并登录开发者账号
3. 在控制台创建智能体应用
4. 配置应用参数，包括接入您的知识库和功能
5. 获取API密钥和接入点信息
6. 修改系统中的SDK配置，替换为通义千问的API

#### 技术调整：
需要修改三个智能体页面中的SDK配置：
1. 将Coze SDK替换为通义千问SDK
2. 更新认证信息和API调用方式
3. 调整UI组件以适配新的SDK

### 4. Coze Studio本地部署

您还可以使用开源的Coze Studio进行本地部署：

#### 步骤：
1. 克隆Coze Studio仓库：`git clone https://github.com/coze-dev/coze-studio.git`
2. 按照项目README进行本地环境配置
3. 启动本地服务
4. 在Coze Studio中导入和管理您的智能体
5. 通过本地部署的Studio发布和测试您的智能体

## 系统文件结构

```
├── agent-coach.html      # 编程教练智能体页面
├── agent-companion.html  # 学习伴侣智能体页面
├── agent-teacher.html    # 教学助手智能体页面
├── index.html           # 系统首页
├── student.html         # 学生端入口
├── teacher.html         # 教师端入口
├── README.md            # 项目说明文档
├── LICENSE              # MIT开源许可证
└── deploy.bat           # Windows部署脚本
```

## 技术说明

- 系统使用嵌入式模式集成Coze智能体SDK
- 所有智能体均支持全屏聊天功能
- 采用响应式设计，适配不同设备
- 无需后端服务，可完全静态部署

## 开源协议

本项目采用 MIT 许可证开源，您可以自由使用、修改和分享。

```
MIT License

Copyright (c) 2023 SADP智能教育系统

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## 注意事项

- 系统中使用的Coze智能体需要有效的token才能正常工作
- 确保在公网部署时保护好API密钥信息
- 所有智能体已配置为嵌入模式，并支持全屏聊天功能
- 确保浏览器支持JavaScript
- 部分功能可能需要网络连接以访问Coze API
- 建议使用现代浏览器以获得最佳体验

## 贡献指南

欢迎提交Issue和Pull Request来改进本系统！

### 贡献步骤
1. Fork本仓库
2. 创建你的特性分支 (`git checkout -b feature/amazing-feature`)
3. 提交你的更改 (`git commit -m 'Add some amazing feature'`)
4. 推送到分支 (`git push origin feature/amazing-feature`)
5. 开启一个Pull Request

## 联系我们

如有任何问题或建议，请通过以下方式联系我们：
- 项目仓库：[项目链接]
- 电子邮件：[联系邮箱]