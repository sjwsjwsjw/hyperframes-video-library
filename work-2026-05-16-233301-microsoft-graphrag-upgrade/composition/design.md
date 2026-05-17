# Design

## Mood
科技感、紧迫感、颠覆认知。暗色调为主，局部霓虹高亮制造视觉冲击。整体氛围：深夜程序员看到了改变认知的内容。

## Palette
- Background Primary: `#0a0e1a`（深蓝黑，主背景）
- Background Secondary: `#0d1b2a`（稍浅深蓝，卡片/区块背景）
- Accent Blue: `#00d4ff`（霓虹蓝，关键词高亮、图谱连线）
- Accent Red: `#ff3b5c`（警告红，错误状态、冲突强调）
- Text Primary: `#ffffff`（主文字）
- Text Secondary: `#8899aa`（辅助文字、说明文字）
- Graph Node: `#1e90ff`（知识图谱节点色）
- Success Green: `#00ff88`（正确方案标注）

## Typography
- 标题：系统无衬线粗体，font-weight: 900，letter-spacing: -0.02em
- 正文：font-weight: 400-500，line-height: 1.6
- 强调词：font-weight: 700，color: accent-blue 或 accent-red
- 数字/数据：font-variant-numeric: tabular-nums，font-weight: 800，font-size 放大1.5-2x

## Motion
- 入场：元素从下方 translateY(20px) + opacity 0→1，duration 0.4-0.6s，ease-out
- 强调：关键词 scale(1.05) pulse，duration 0.3s
- 图谱节点：连线从中心向外扩散，stagger 0.1s per node
- 数字：counter animation，从0增长到目标值
- 转场：crossfade 0.3s，保持背景色连续

## Density
中高密度。每个 scene 有明确的主信息区（占60%画面）+ 辅助装饰区（占40%）。
禁止大面积空白。使用卡片、标签、图示、数据块填充空间。
布局优先 display: grid，将画面切分为明确的内容区域。

## Layout Grid（竖屏 9:16）
- 安全区：上下各10%，左右各10%
- 主内容区：中间80%宽 × 80%高
- 顶部装饰带：10%高（品牌标识、进度指示）
- 底部装饰带：10%高（标签、来源标注）
