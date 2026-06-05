# SVG流程图模板

## 一、基础流程图

### 线性流程图
```svg
<svg viewBox="0 0 900 200" width="100%">
  <defs>
    <marker id="arrow" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="6" markerHeight="6" orient="auto-start-reverse">
      <path d="M2 1L8 5L2 9" fill="none" stroke="context-stroke" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
    </marker>
  </defs>
  
  <!-- 节点1 -->
  <rect x="50" y="70" width="150" height="60" rx="10" fill="rgba(100,140,255,0.1)" stroke="rgba(100,140,255,0.3)" stroke-width="1"/>
  <text x="125" y="105" text-anchor="middle" fill="#fff" font-size="14">开始</text>
  
  <!-- 箭头1 -->
  <line x1="200" y1="100" x2="280" y2="100" stroke="rgba(100,140,255,0.5)" stroke-width="1" marker-end="url(#arrow)"/>
  
  <!-- 节点2 -->
  <rect x="280" y="70" width="150" height="60" rx="10" fill="rgba(100,140,255,0.1)" stroke="rgba(100,140,255,0.3)" stroke-width="1"/>
  <text x="355" y="105" text-anchor="middle" fill="#fff" font-size="14">处理</text>
  
  <!-- 箭头2 -->
  <line x1="430" y1="100" x2="510" y2="100" stroke="rgba(100,140,255,0.5)" stroke-width="1" marker-end="url(#arrow)"/>
  
  <!-- 节点3 -->
  <rect x="510" y="70" width="150" height="60" rx="10" fill="rgba(100,140,255,0.1)" stroke="rgba(100,140,255,0.3)" stroke-width="1"/>
  <text x="585" y="105" text-anchor="middle" fill="#fff" font-size="14">完成</text>
</svg>
```

### 分支流程图
```svg
<svg viewBox="0 0 900 300" width="100%">
  <defs>
    <marker id="arrow" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="6" markerHeight="6" orient="auto-start-reverse">
      <path d="M2 1L8 5L2 9" fill="none" stroke="context-stroke" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
    </marker>
  </defs>
  
  <!-- 开始节点 -->
  <rect x="375" y="20" width="150" height="60" rx="10" fill="rgba(100,140,255,0.1)" stroke="rgba(100,140,255,0.3)" stroke-width="1"/>
  <text x="450" y="55" text-anchor="middle" fill="#fff" font-size="14">开始</text>
  
  <!-- 箭头到决策点 -->
  <line x1="450" y1="80" x2="450" y2="120" stroke="rgba(100,140,255,0.5)" stroke-width="1" marker-end="url(#arrow)"/>
  
  <!-- 菱形决策点 -->
  <polygon points="450,120 550,170 450,220 350,170" fill="rgba(232,168,56,0.1)" stroke="rgba(232,168,56,0.3)" stroke-width="1"/>
  <text x="450" y="175" text-anchor="middle" fill="#fff" font-size="12">条件判断</text>
  
  <!-- 分支1：是 -->
  <line x1="550" y1="170" x2="650" y2="120" stroke="rgba(60,180,120,0.5)" stroke-width="1" marker-end="url(#arrow)"/>
  <text x="600" y="140" text-anchor="middle" fill="rgba(255,255,255,0.7)" font-size="10">是</text>
  <rect x="650" y="90" width="150" height="60" rx="10" fill="rgba(60,180,120,0.1)" stroke="rgba(60,180,120,0.3)" stroke-width="1"/>
  <text x="725" y="125" text-anchor="middle" fill="#fff" font-size="14">处理A</text>
  
  <!-- 分支2：否 -->
  <line x1="350" y1="170" x2="250" y2="220" stroke="rgba(232,84,84,0.5)" stroke-width="1" marker-end="url(#arrow)"/>
  <text x="300" y="200" text-anchor="middle" fill="rgba(255,255,255,0.7)" font-size="10">否</text>
  <rect x="100" y="190" width="150" height="60" rx="10" fill="rgba(232,84,84,0.1)" stroke="rgba(232,84,84,0.3)" stroke-width="1"/>
  <text x="175" y="225" text-anchor="middle" fill="#fff" font-size="14">处理B</text>
  
  <!-- 汇合到结束 -->
  <line x1="725" y1="150" x2="725" y2="250" stroke="rgba(60,180,120,0.5)" stroke-width="1" marker-end="url(#arrow)"/>
  <line x1="175" y1="250" x2="175" y2="270" stroke="rgba(232,84,84,0.5)" stroke-width="1"/>
  <line x1="175" y1="270" x2="725" y2="270" stroke="rgba(100,140,255,0.5)" stroke-width="1"/>
  <line x1="725" y1="270" x2="725" y2="290" stroke="rgba(100,140,255,0.5)" stroke-width="1" marker-end="url(#arrow)"/>
  <rect x="650" y="280" width="150" height="40" rx="8" fill="rgba(100,140,255,0.1)" stroke="rgba(100,140,255,0.3)" stroke-width="1"/>
  <text x="725" y="305" text-anchor="middle" fill="#fff" font-size="12">结束</text>
</svg>
```

## 二、时间线流程图

### 纵向时间线
```svg
<svg viewBox="0 0 900 300" width="100%">
  <!-- 时间轴 -->
  <line x1="100" y1="50" x2="100" y2="280" stroke="rgba(100,140,255,0.3)" stroke-width="2"/>
  
  <!-- 节点1 -->
  <circle cx="100" cy="70" r="10" fill="rgba(100,140,255,0.3)" stroke="rgba(100,140,255,0.5)" stroke-width="2"/>
  <rect x="140" y="50" width="200" height="40" rx="8" fill="rgba(100,140,255,0.1)" stroke="rgba(100,140,255,0.3)" stroke-width="1"/>
  <text x="240" y="75" text-anchor="middle" fill="#fff" font-size="12">阶段1：开始</text>
  
  <!-- 节点2 -->
  <circle cx="100" cy="140" r="10" fill="rgba(60,180,120,0.3)" stroke="rgba(60,180,120,0.5)" stroke-width="2"/>
  <rect x="140" y="120" width="200" height="40" rx="8" fill="rgba(60,180,120,0.1)" stroke="rgba(60,180,120,0.3)" stroke-width="1"/>
  <text x="240" y="145" text-anchor="middle" fill="#fff" font-size="12">阶段2：进行中</text>
  
  <!-- 节点3 -->
  <circle cx="100" cy="210" r="10" fill="rgba(232,168,56,0.3)" stroke="rgba(232,168,56,0.5)" stroke-width="2"/>
  <rect x="140" y="190" width="200" height="40" rx="8" fill="rgba(232,168,56,0.1)" stroke="rgba(232,168,56,0.3)" stroke-width="1"/>
  <text x="240" y="215" text-anchor="middle" fill="#fff" font-size="12">阶段3：完成</text>
</svg>
```

### 横向时间线
```svg
<svg viewBox="0 0 900 200" width="100%">
  <!-- 时间轴 -->
  <line x1="50" y1="100" x2="850" y2="100" stroke="rgba(100,140,255,0.3)" stroke-width="2"/>
  
  <!-- 节点1 -->
  <circle cx="150" cy="100" r="12" fill="rgba(100,140,255,0.3)" stroke="rgba(100,140,255,0.5)" stroke-width="2"/>
  <text x="150" y="80" text-anchor="middle" fill="#fff" font-size="12">2024-01</text>
  <text x="150" y="130" text-anchor="middle" fill="rgba(255,255,255,0.7)" font-size="10">项目启动</text>
  
  <!-- 节点2 -->
  <circle cx="450" cy="100" r="12" fill="rgba(60,180,120,0.3)" stroke="rgba(60,180,120,0.5)" stroke-width="2"/>
  <text x="450" y="80" text-anchor="middle" fill="#fff" font-size="12">2024-06</text>
  <text x="450" y="130" text-anchor="middle" fill="rgba(255,255,255,0.7)" font-size="10">核心功能完成</text>
  
  <!-- 节点3 -->
  <circle cx="750" cy="100" r="12" fill="rgba(232,168,56,0.3)" stroke="rgba(232,168,56,0.5)" stroke-width="2"/>
  <text x="750" y="80" text-anchor="middle" fill="#fff" font-size="12">2024-12</text>
  <text x="750" y="130" text-anchor="middle" fill="rgba(255,255,255,0.7)" font-size="10">项目上线</text>
</svg>
```

## 三、架构图

### 层级架构图
```svg
<svg viewBox="0 0 900 400" width="100%">
  <!-- 顶层 -->
  <rect x="300" y="20" width="300" height="60" rx="10" fill="rgba(100,140,255,0.1)" stroke="rgba(100,140,255,0.3)" stroke-width="1"/>
  <text x="450" y="55" text-anchor="middle" fill="#fff" font-size="14">应用层</text>
  
  <!-- 箭头 -->
  <line x1="450" y1="80" x2="450" y2="120" stroke="rgba(100,140,255,0.5)" stroke-width="1" marker-end="url(#arrow)"/>
  
  <!-- 中间层 -->
  <rect x="100" y="120" width="200" height="60" rx="10" fill="rgba(60,180,120,0.1)" stroke="rgba(60,180,120,0.3)" stroke-width="1"/>
  <text x="200" y="155" text-anchor="middle" fill="#fff" font-size="14">模块A</text>
  
  <rect x="350" y="120" width="200" height="60" rx="10" fill="rgba(60,180,120,0.1)" stroke="rgba(60,180,120,0.3)" stroke-width="1"/>
  <text x="450" y="155" text-anchor="middle" fill="#fff" font-size="14">模块B</text>
  
  <rect x="600" y="120" width="200" height="60" rx="10" fill="rgba(60,180,120,0.1)" stroke="rgba(60,180,120,0.3)" stroke-width="1"/>
  <text x="700" y="155" text-anchor="middle" fill="#fff" font-size="14">模块C</text>
  
  <!-- 箭头 -->
  <line x1="200" y1="180" x2="200" y2="220" stroke="rgba(60,180,120,0.5)" stroke-width="1" marker-end="url(#arrow)"/>
  <line x1="450" y1="180" x2="450" y2="220" stroke="rgba(60,180,120,0.5)" stroke-width="1" marker-end="url(#arrow)"/>
  <line x1="700" y1="180" x2="700" y2="220" stroke="rgba(60,180,120,0.5)" stroke-width="1" marker-end="url(#arrow)"/>
  
  <!-- 底层 -->
  <rect x="300" y="220" width="300" height="60" rx="10" fill="rgba(232,168,56,0.1)" stroke="rgba(232,168,56,0.3)" stroke-width="1"/>
  <text x="450" y="255" text-anchor="middle" fill="#fff" font-size="14">数据层</text>
</svg>
```

## 四、对比图

### 双列对比图
```svg
<svg viewBox="0 0 900 300" width="100%">
  <!-- 左侧：旧方案 -->
  <rect x="30" y="20" width="400" height="260" rx="12" fill="rgba(232,84,84,0.05)" stroke="rgba(232,84,84,0.3)" stroke-width="1"/>
  <text x="230" y="50" text-anchor="middle" fill="#fff" font-size="16" font-weight="600">旧方案</text>
  
  <text x="60" y="90" fill="rgba(255,255,255,0.8)" font-size="13">• 问题1</text>
  <text x="60" y="120" fill="rgba(255,255,255,0.8)" font-size="13">• 问题2</text>
  <text x="60" y="150" fill="rgba(255,255,255,0.8)" font-size="13">• 问题3</text>
  
  <!-- 右侧：新方案 -->
  <rect x="470" y="20" width="400" height="260" rx="12" fill="rgba(60,180,120,0.05)" stroke="rgba(60,180,120,0.3)" stroke-width="1"/>
  <text x="670" y="50" text-anchor="middle" fill="#fff" font-size="16" font-weight="600">新方案</text>
  
  <text x="500" y="90" fill="rgba(255,255,255,0.8)" font-size="13">• 优势1</text>
  <text x="500" y="120" fill="rgba(255,255,255,0.8)" font-size="13">• 优势2</text>
  <text x="500" y="150" fill="rgba(255,255,255,0.8)" font-size="13">• 优势3</text>
  
  <!-- 中间箭头 -->
  <text x="450" y="150" text-anchor="middle" fill="rgba(100,140,255,0.8)" font-size="24">→</text>
</svg>
```

## 五、统计图表

### 柱状图
```svg
<svg viewBox="0 0 900 300" width="100%">
  <!-- 坐标轴 -->
  <line x1="100" y1="250" x2="800" y2="250" stroke="rgba(255,255,255,0.3)" stroke-width="1"/>
  <line x1="100" y1="50" x2="100" y2="250" stroke="rgba(255,255,255,0.3)" stroke-width="1"/>
  
  <!-- 柱子 -->
  <rect x="150" y="100" width="80" height="150" rx="4" fill="rgba(100,140,255,0.6)"/>
  <text x="190" y="270" text-anchor="middle" fill="rgba(255,255,255,0.7)" font-size="12">项目A</text>
  
  <rect x="300" y="80" width="80" height="170" rx="4" fill="rgba(60,180,120,0.6)"/>
  <text x="340" y="270" text-anchor="middle" fill="rgba(255,255,255,0.7)" font-size="12">项目B</text>
  
  <rect x="450" y="120" width="80" height="130" rx="4" fill="rgba(232,168,56,0.6)"/>
  <text x="490" y="270" text-anchor="middle" fill="rgba(255,255,255,0.7)" font-size="12">项目C</text>
  
  <rect x="600" y="60" width="80" height="190" rx="4" fill="rgba(232,84,84,0.6)"/>
  <text x="640" y="270" text-anchor="middle" fill="rgba(255,255,255,0.7)" font-size="12">项目D</text>
</svg>
```
