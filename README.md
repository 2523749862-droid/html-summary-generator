# HTML 文档生成器 Skill
# HTML Document Generator Skill

一个功能强大的Agent   Skill，用于生成精美的 HTML 文档。支持 8 种文档类型、12 种主题、丰富的动效和自定义功能。
A powerful Agent Skill for generating beautiful HTML documents. Supports 8 document types, 12 themes, rich animations and custom features.

---

## ✨ 特性 | Features

### 📄 8 种文档类型 | 8 Document Types
- 📋 **项目总结 / Project Summary**
  项目背景、目标完成情况、关键成果、问题与复盘
  Project background, goal achievement, key results, issues & review

- 📘 **技术文档 / Technical Document**
  架构设计、技术选型、接口说明、部署流程
  Architecture design, tech stack, API specs, deployment process

- 📊 **汇报PPT / Presentation PPT**
  封面、目录、核心内容、数据图表、总结
  Cover, table of contents, core content, charts, summary

- 📖 **教程指南 / Tutorial Guide**
  前置条件、分步操作、注意事项、FAQ
  Prerequisites, step-by-step guide, notes, FAQ

- 📈 **数据报告 / Data Report**
  数据概览、趋势分析、对比分析、结论
  Data overview, trend analysis, comparison, conclusion

- ⚖️ **对比分析 / Comparison Analysis**
  对比维度、各方案详情、优劣评分、推荐
  Comparison dimensions, solution details, scoring, recommendation

- 🔄 **流程文档 / Process Document**
  流程概述、流程图、角色职责、操作规范
  Process overview, flowchart, roles & responsibilities, SOP

- 📝 **会议纪要 / Meeting Minutes**
  会议信息、参会人员、议题讨论、待办跟踪
  Meeting info, attendees, discussion, action items

---

### 🎨 12 种预设主题 | 12 Preset Themes

| 主题 Theme | 主色调 Main Color | 背景色 Background | 适用场景 Use Case |
|---|---|---|---|
| 银河 Galaxy | `#7c3aed` | `#0d1117` 深色 Dark | 科技、商务 Tech, Business |
| 深海 Deep Sea | `#00e5ff` | `#0a1929` 深色 Dark | 科技、金融 Tech, Finance |
| 薰衣草 Lavender | `#e040fb` | `#1a0e2e` 深色 Dark | 时尚、美妆 Fashion, Beauty |
| 玫瑰 Rose | `#ff1744` | `#2d0a1a` 深色 Dark | 健康、公益 Health, Charity |
| 黄金 Gold | `#f0c040` | `#1a1508` 深色 Dark | 奢华、高贵 Luxury, Premium |
| 莫兰迪 Morandi | `#8b6f5e` | `#e8e0d8` 浅色 Light | 高级、艺术 Premium, Art |
| 雪白 Snow White | `#2563eb` | `#f0f4f8` 浅色 Light | 正式、学术 Formal, Academic |
| 奶油 Cream | `#b45309` | `#fef7e7` 浅色 Light | 温馨、生活 Warm, Lifestyle |
| 薄荷 Mint | `#059669` | `#ecfdf5` 浅色 Light | 清新、自然 Fresh, Nature |
| 天空 Sky | `#0369a1` | `#eef6ff` 浅色 Light | 简洁、专业 Clean, Professional |
| 洛可可 Rococo | `#be185d` | `#fdf0f5` 浅色 Light | 浪漫、古典 Romantic, Classic |
| 敦煌 Dunhuang | `#c23b22` | `#faf5ef` 浅色 Light | 古朴、文化 Antique, Culture |

---

### ✨ 动效系统 | Animation System

- **11 种背景动效 / 11 Background Animations**
  粒子飘浮、星空闪烁、雪花飘落、泡泡上升、网格连线、波浪流动、萤火虫、矩阵雨、星云漩涡、彩纸飘落、无动效
  Particle float, starry flicker, snowfall, bubble rise, grid connect, wave flow, firefly, matrix rain, nebula vortex, confetti, none

- **9 种鼠标动效 / 9 Mouse Animations**
  泛光跟随、拖尾光轨、星河轨迹、星星闪烁、彩虹光环、波纹扩散、磁性吸引、烟花点击、无动效
  Glow follow, light trail, galaxy track, star blink, rainbow ring, ripple spread, magnetic attract, fireworks click, none

- **10 种边框样式 / 10 Border Styles**
  毛玻璃、霓虹发光、脉冲呼吸、渐变流动、闪烁微光、悬浮漂浮、霓虹闪烁、实线边框、虚线边框、双线边框
  Frosted glass, neon glow, pulse breathe, gradient flow, shimmer glow, hover float, neon flash, solid line, dashed line, double line

---

### 🛠️ 自定义功能 | Custom Features
- 色相轮调色器（360° Canvas 色相环）
  Hue wheel color picker (360° Canvas hue ring)
- 毛玻璃强度调节（0–40px）
  Frosted glass intensity (0–40px)
- 边框圆角调节（0–32px）
  Border radius adjustment (0–32px)
- 卡片透明度调节（20%–95%）
  Card opacity adjustment (20%–95%)
- 字体设置（9 种字体、字号、行高、标题字号）
  Font settings (9 fonts, size, line height, heading size)
- 添加段落功能（支持大段/小段、选择插入位置）
  Add paragraph (long/short, choose insertion position)
- 自动保存设置到 localStorage
  Auto-save settings to localStorage
- PDF 导出（A4 打印优化）
  PDF export (A4 print optimized)

---

## 📦 三种生成模式 | Three Generation Modes

| 模式 Mode | 功能 Features | 文件大小 Size | 生成速度 Speed | 适用场景 Use Case |
|---|---|---|---|---|
| **完整版 Full** | 调色器+动效+字体+边框样式+自动保存<br>Color picker + animation + font + border + auto-save | ~80KB | 较慢 Slow | 需要事后调整 Need later editing |
| **精简版 Lite** | 固定动效+固定样式+PDF导出<br>Fixed animation + fixed style + PDF export | ~30KB | 快速 Fast | 不需要调整 No further changes |
| **纯静态 Static** | 固定样式，无交互<br>Fixed style, no interaction | ~15KB | 最快 Fastest | 邮件发送、打印 Email, Print |

---

## 🚀 安装 | Installation

将 `html-summary-generator` 文件夹复制到你的 WorkBuddy skills 目录：
Copy the `html-summary-generator` folder to your WorkBuddy skills directory:

```bash
# 用户级安装（推荐）
cp -r html-summary-generator ~/.workbuddy/skills/

# 或项目级安装
cp -r html-summary-generator <project>/.workbuddy/skills/
