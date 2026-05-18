# 🐌 蜗牛主页

一个温柔实用的个人起始页 · 单 HTML · 可装为 App

🌐 在线访问：**[woniu.bee.al](https://woniu.bee.al)**

## ✨ 功能

| 模块 | 说明 |
|------|------|
| ⏰ **时钟** | 实时时间 · 农历 · 干支 · 生肖 · 节日提醒 |
| 🌤 **天气** | 自动定位 · 可手动改城市 · 温度/湿度/风速/体感 |
| 💬 **一言** | 古诗词随机一句 · 点击换一条 |
| 📅 **日历** | 农历 · 节日红点 · 翻月浏览 |
| ⏳ **倒计时** | 支持多个事件 · 本地保存 |
| 📝 **待办** | 简易 todo · 本地保存 · 回车快速添加 |
| 🍅 **番茄钟** | 25/5/15 三种模式 · 桌面通知 · 当日累计 |
| 🌙 **暗色模式** | 跟随系统 / 手动切换（右上角按钮） |
| 📱 **PWA** | 可"添加到主屏幕"当 App 用 · 离线可访问 |

## 🛠️ 技术

- 纯 HTML/CSS/JS，**单文件部署**，无依赖、无构建
- 字体走 [font.im](https://font.im) 国内镜像（替代 Google Fonts）
- 天气：[Open-Meteo](https://open-meteo.com)（免 key）
- 定位：ipapi.co + ipwho.is + ip.sb 三源冗余
- 农历算法：内嵌 1900–2050 数据表（无外部库）
- 一言：[hitokoto.cn](https://hitokoto.cn)
- 全部数据**本地存储**，不上传任何服务器

## 🚀 部署

仓库内容直接放到任何静态托管即可：

- **GitHub Pages**（当前使用）：push 到 `main` 自动部署
- **Cloudflare Pages / Vercel / Netlify**：导入仓库一键发布
- **自己的服务器**：把 4 个文件丢到 web 根目录就行

### 4 个核心文件

```
index.html      # 主页面（含所有逻辑）
manifest.json   # PWA 配置
sw.js           # Service Worker（离线缓存）
icon.svg        # 图标
```

`CNAME` 文件用于 GitHub Pages 绑定自定义域名 `woniu.bee.al`。

## 🎨 自定义

打开 `index.html`，在 `:root` 里改色：

```css
:root{
  --accent: #9b84e0;   /* 紫 - 倒计时按钮 */
  --accent2: #4a90c4;  /* 蓝 - 今天高亮 */
  --danger: #e07070;   /* 红 - 节日 */
  --bg-grad: linear-gradient(135deg, #e8f4fd 0%, #d4f5ee 40%, #fde8f5 100%);
}
```

## 📜 License

MIT
