# AI 聊天助手

打开链接就能用的在线 AI 对话页面。纯静态单文件，不依赖后端服务器，无需安装、无需注册。

## 在线地址

**https://97ea2cc954c24078b2f0be7e45e6d48d.app.workbuddy.host**

## 文件说明

| 文件 | 说明 |
| --- | --- |
| `index.html` | 完整页面，样式与逻辑都在里面，可直接用浏览器打开 |

## 功能

- **流式输出**：逐字返回，边生成边显示，带闪烁光标
- **多轮记忆**：自动携带最近 5 轮对话作为上下文
- **可中断**：生成过程中再次点击发送按钮即可停止

## 技术说明

页面不依赖任何后端服务，直接在前端调用文本生成接口，因此可以部署在任意静态托管平台上（GitHub Pages、EdgeOne Pages、Vercel 等），把 `index.html` 放上去即可。

配置项集中在 `index.html` 的脚本开头：

```js
const API = 'https://text.pollinations.ai/openai';   // 接口地址
const MODEL = 'openai';                              // 模型标识
const MEMORY = 5;                                    // 携带的历史轮数
```
