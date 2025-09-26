# SportScore Professional Dark Style Guide

## Colors
### Primary Colors
- **primary-base**: `text-[#FF6B35]` or `bg-[#FF6B35]` - 体育橙色主色，用于关键操作按钮和重要数据高亮
- **primary-lighter**: `bg-[#FF8555]` - 悬停和激活状态
- **primary-darker**: `text-[#E55A2B]` or `bg-[#E55A2B]` - 按压状态和深色变体

### Background Colors
- **bg-page**: `bg-[#1A1D23]` - 深炭灰主背景
- **bg-container-primary**: `bg-[#242832]` - 主要卡片和内容容器
- **bg-container-secondary**: `bg-[#2A2F3A]` - 次级容器和悬浮面板
- **bg-container-inset**: `bg-[#1E2128]` - 输入框和表单背景
- **bg-container-inset-strong**: `bg-[#161920]` - 深嵌入背景，用于数据表格交替行
- **bg-bottom-navigation**: `bg-[#1F2229]` - 底部导航栏背景

### Text Colors
- **color-text-primary**: `text-white/95` - 主要文本，比分数字
- **color-text-secondary**: `text-white/75` - 次级文本，队伍名称
- **color-text-tertiary**: `text-white/55` - 三级文本，时间戳和标签
- **color-text-quaternary**: `text-white/35` - 占位符和辅助信息
- **color-text-on-primary**: `text-white` - 橙色背景上的文本
- **color-text-link**: `text-[#FF6B35]` - 链接文本和可点击元素

### Functional Colors
- **color-success-default**: `#22C55E` - 胜利、上涨数据指示
- **color-success-light**: `#22C55E/20` - 成功状态背景
- **color-error-default**: `#EF4444` - 失败、下跌数据指示
- **color-error-light**: `#EF4444/20` - 错误状态背景
- **color-warning-default**: `#F59E0B` - 警告和中性数据状态
- **color-warning-light**: `#F59E0B/20` - 警告状态背景
- **color-function-default**: `#3B82F6` - 功能性元素和信息提示
- **color-function-light**: `#3B82F6/20` - 功能状态背景

### Data Visualization Charts
- **Primary Chart Colors**: #FF6B35, #22C55E, #EF4444, #F59E0B, #3B82F6, #8B5CF6
- **Neutral Data Colors**: #71717A, #52525B, #3F3F46, #27272A, #18181B
- **Grid and Axis**: #374151, #4B5563

## Typography
- **Font Stack**:
  - **font-family-base**: `-apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif` - 无衬线字体确保数据清晰度

- **Font Size & Weight**:
  - **Caption**: 10px / 500 - 底部导航标签和数据单位
  - **Body small**: 12px / 400 - 辅助信息和时间戳
  - **Body default**: 14px / 400 - 常规界面文本
  - **Data Emphasis**: 14px / 600 - 重要数据和队伍名称
  - **Score Display**: 24px / 700 - 比分显示
  - **Page Title**: 20px / 600 - 页面标题
  - **Headline**: 28px / 700 - 重要赛事标题

- **Line Height**: 1.3 - 紧凑的行高确保数据密度

## Border Radius
- **Minimal**: 2px - 输入框和小按钮，保持几何精确性
- **Small**: 4px - 数据卡片内部元素
- **Medium**: 6px - 主要卡片和按钮
- **Large**: 8px - 大型容器和模态框

## Layout & Spacing
- **Spacing Scale**:
- **Base Unit**: 4px
- **Tight**: 6px - 数据表格内部间距
- **Compact**: 8px - 列表项和数据行间距
- **Standard**: 12px - 卡片内边距和模块间距
- **Loose**: 16px - 页面级分段间距

## Create Boundaries (contrast of surface color, borders, shadows)
主要依靠表面色彩差异和细线边框创建数据分割，突出专业数据界面的清晰层次

### Borders
- **Data Divider**: 1px solid #374151 - 数据表格分割线和卡片边框 `border border-gray-600`
- **Subtle**: 1px solid #4B5563 - 激活状态边框 `border border-gray-500`
- **Accent**: 1px solid #FF6B35 - 选中状态和重要边框 `border border-[#FF6B35]`

### Dividers
- **Horizontal**: `border-t border-gray-600` - 数据行分割
- **Vertical**: `border-l border-gray-600` - 数据列分割
- **Section**: `border-t-2 border-gray-500` - 主要分段分割

### Shadows & Effects
- **Data Card**: `shadow-[0_2px_8px_rgba(0,0,0,0.3)]` - 数据卡片轻微阴影
- **Floating Panel**: `shadow-[0_4px_12px_rgba(0,0,0,0.4)]` - 悬浮面板和模态框
- **Active Element**: `shadow-[0_0_0_2px_rgba(255,107,53,0.3)]` - 橙色焦点环效果

## Assets
### Image
- For normal `<img>`: `object-cover brightness-90 contrast-90` - 深色模式图片优化
- For `<img>` with:
  - Slight overlay: `object-cover brightness-75 contrast-90`
  - Heavy overlay: `object-cover brightness-60 contrast-90`

### Logo
- **Icon-based**:
  - **Graphic**: Use FontAwesome Solid sports-related icons (`fa-futbol` for soccer, `fa-basketball-ball` for basketball)

### Icon
- Use Material Symbols - rounded from Iconify for 友好的运动感
- Icons should maintain visual weight consistency with bold data presentation
- Example:
  ```html
  <div class="flex items-center justify-center bg-transparent w-5 h-5">
  <iconify-icon icon="material-symbols:sports-soccer-rounded" class="text-lg"></iconify-icon>
  </div>
  ```

## Page Layout - Mobile
```html
<body class="w-[390px] min-h-[844px] bg-[#1A1D23] font-['-apple-system','BlinkMacSystemFont','Segoe_UI','Roboto',sans-serif] leading-[1.3]">

  <!-- Top Fixed Header -->
  <div class="z-10 fixed top-0 w-full bg-[#1A1D23]">
    <div class="h-[env(safe-area-inset-top,0px)]"></div>
    <header class="h-14 flex items-center justify-between px-4 border-b border-gray-600">
      <!-- Navigation content -->
    </header>
  </div>

  <!-- Top Spacer -->
  <div>
    <div class="h-[env(safe-area-inset-top,0px)]"></div>
    <div class="h-14"></div>
  </div>

  <!-- Main Scrollable Content Area -->
  <main class="py-3 space-y-3">
    <section class="px-4">
      <!-- Content sections -->
    </section>
  </main>

  <!-- Bottom Spacer -->
  <div>
    <div class="mt-[12px] h-[72px]"></div>
    <div class="h-[env(safe-area-inset-bottom,0px)]"></div>
  </div>

  <!-- Bottom Fixed Area -->
  <div class="z-10 fixed bottom-0 w-full flex flex-col">
    <!-- Bottom Navigation -->
    <div class="bg-[#1F2229] border-t border-gray-600">
      <nav class="flex justify-around py-3 px-1">
        <div class="flex flex-1 flex-col items-center gap-1">
            <div class="w-6 h-6 flex items-center justify-center">
                <iconify-icon icon="material-symbols:sports-soccer-rounded" class="text-white/55"></iconify-icon>
            </div>
            <span class="text-[10px] font-medium text-white/55">比分</span>
        </div>
      </nav>
      <div class="h-[env(safe-area-inset-bottom,0px)]"></div>
    </div>
  </div>
</body>
```

## Tailwind Component Examples
### Basic
- **Progress bars**: `h-1 bg-gray-700` with `bg-[#FF6B35]` progress fill
- **Button**:
  - Primary: `bg-[#FF6B35] text-white px-4 py-2 rounded border-0 font-medium`
  - Secondary: `bg-[#242832] text-white/90 px-4 py-2 rounded border border-gray-600 font-medium`
- **Score Display**: `text-2xl font-bold text-white/95 tabular-nums`
- **Data Badge**: `bg-[#22C55E]/20 text-[#22C55E] px-2 py-1 rounded text-xs font-medium`

### Data Entry
- **Input Field**: `bg-[#1E2128] border border-gray-600 text-white/90 px-3 py-2 rounded focus:border-[#FF6B35] focus:ring-1 focus:ring-[#FF6B35]/30`

### Container
- **Data Card**: `bg-[#242832] border border-gray-600 rounded-md p-4`
- **Live Score Panel**: `bg-[#2A2F3A] border-l-2 border-[#FF6B35] p-3 rounded`

## Additional Notes
该风格指南专为体育数据应用设计，强调数据的清晰呈现和实时更新的视觉反馈。深色背景减少长时间使用的眼部疲劳，而鲜明的橙色主色确保关键操作和数据的突出显示。所有颜色选择都考虑了在不同光线条件下的可读性，特别适合体育赛事的观看环境。

<colors_extraction>
#FF6B35
#FF8555
#E55A2B
#1A1D23
#242832
#2A2F3A
#1E2128
#161920
#1F2229
#FFFFFF
#22C55E
#22C55E33
#EF4444
#EF444433
#F59E0B
#F59E0B33
#3B82F6
#3B82F633
#8B5CF6
#71717A
#52525B
#3F3F46
#27272A
#18181B
#374151
#4B5563
</colors_extraction>