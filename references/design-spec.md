# HTML总结文档设计规范

## 一、整体风格

### 设计理念
- **银河/星河背景**：营造科技感和深度感
- **高对比度文字**：确保可读性
- **流畅动效**：提升视觉体验
- **响应式布局**：适配各种屏幕

### 色彩体系

| 颜色名称 | 色值 | 用途 |
|---------|------|------|
| 背景色 | `#0d1117` | 页面背景 |
| 主色调 | `#648cff` | 蓝紫色，用于标题、高亮 |
| 辅助色 | `#3cb478` | 绿色，用于成功状态 |
| 警告色 | `#e8a838` | 橙色，用于警告状态 |
| 危险色 | `#e85454` | 红色，用于错误状态 |
| 信息色 | `#5890ff` | 蓝色，用于信息提示 |
| 正文色 | `#f0f0f0` | 白色，用于正文 |
| 标题色 | `#ffffff` | 纯白，用于标题 |

## 二、组件样式

### 卡片组件
```css
.card {
  background: rgba(255,255,255,0.03);
  border-radius: 16px;
  padding: 28px;
  margin: 20px 0;
  border: 1px solid rgba(255,255,255,0.08);
  transition: all 0.4s ease;
  position: relative;
  overflow: hidden;
  backdrop-filter: blur(5px);
}
.card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 2px;
  background: linear-gradient(90deg, #648cff, #3cb478, #e8a838);
  transform: scaleX(0);
  transform-origin: left;
  transition: transform 0.4s ease;
}
.card:hover::before {
  transform: scaleX(1);
}
.card:hover {
  border-color: rgba(100,140,255,0.3);
  box-shadow: 0 10px 40px rgba(100,140,255,0.15);
  transform: translateY(-5px);
}
```

### 时间线组件
```css
.timeline {
  position: relative;
  padding-left: 40px;
  margin: 40px 0;
}
.timeline::before {
  content: '';
  position: absolute;
  left: 12px;
  top: 0;
  bottom: 0;
  width: 3px;
  background: linear-gradient(to bottom, #648cff, #3cb478, #e8a838, #e85454);
  border-radius: 2px;
}
.timeline-item {
  position: relative;
  margin-bottom: 35px;
  padding: 24px;
  background: rgba(255,255,255,0.03);
  border-radius: 16px;
  border: 1px solid rgba(255,255,255,0.08);
  transition: all 0.4s ease;
}
.timeline-item::before {
  content: '';
  position: absolute;
  left: -35px;
  top: 28px;
  width: 16px;
  height: 16px;
  border-radius: 50%;
  border: 3px solid rgba(13,17,23,0.8);
}
.timeline-item.success::before { background: #3cb478; box-shadow: 0 0 15px #3cb478; }
.timeline-item.error::before { background: #e85454; box-shadow: 0 0 15px #e85454; }
.timeline-item.warning::before { background: #e8a838; box-shadow: 0 0 15px #e8a838; }
```

### 步骤组件
```css
.steps { counter-reset: step-counter; margin: 40px 0; }
.step {
  position: relative;
  padding: 24px 24px 24px 90px;
  margin-bottom: 24px;
  background: rgba(255,255,255,0.03);
  border-radius: 16px;
  border: 1px solid rgba(255,255,255,0.08);
  transition: all 0.4s ease;
}
.step::before {
  counter-increment: step-counter;
  content: counter(step-counter);
  position: absolute;
  left: 24px;
  top: 24px;
  width: 48px;
  height: 48px;
  background: linear-gradient(135deg, #3cb478, #64ffaa);
  color: #0d1117;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 20px;
  font-weight: 600;
  animation: glow 2s infinite;
}
```

## 三、动效规范

### 鼠标光效
- 跟随鼠标移动
- 半透明渐变圆形
- 平滑过渡效果

### 粒子背景
- 随机分布的小圆点
- 缓慢浮动动画
- 半透明效果

### 悬停效果
- 卡片：上移 + 阴影
- 流程图节点：放大 + 发光
- 时间线项：右移 + 阴影

### 涟漪效果
- 点击产生波纹
- 从点击位置扩散
- 逐渐消失

## 四、响应式设计

### 断点设置
- **移动端**: `< 768px`
- **平板端**: `768px - 1024px`
- **桌面端**: `> 1024px`

### 适配规则
- 统计卡片：4列 → 2列（移动端）
- 平台图标：7列 → 4列（移动端）
- 对比卡片：2列 → 1列（移动端）
- 标题字号：42px → 28px（移动端）
