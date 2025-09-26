# SportScore Zen Style Guide

## Colors
### Primary Colors
- **primary-base**: `bg-[#1E3A5F]` or `text-[#1E3A5F]` - Deep navy blue for headers, key data
- **primary-lighter**: `bg-[#2C4A6B]` - Subtle variation for interactive states
- **primary-darker**: `bg-[#16304C]` or `text-[#16304C]` - Enhanced emphasis areas

### Background Colors
- **bg-page**: `bg-[#F8FAFB]` - Pure light page background
- **bg-container-primary**: `bg-white` - Main cards, content containers
- **bg-container-secondary**: `bg-[#FAFBFC]` - Secondary content areas
- **bg-container-tertiary**: `bg-[#F3F5F7]` - Subtle differentiation areas
- **bg-active**: `bg-[#F0F2F4]` - Active/selected card states

### Text Colors
- **color-text-primary**: `text-[#1E3A5F]` - Primary content, headlines
- **color-text-secondary**: `text-[#4A5568]` - Secondary information
- **color-text-tertiary**: `text-[#718096]` - Supporting text, metadata
- **color-text-quaternary**: `text-[#A0AEC0]` - Subtle labels, placeholders
- **color-text-on-dark**: `text-white` - Text on primary color backgrounds
- **color-text-score**: `text-[#1E3A5F]` - Score numbers emphasis

### Functional Colors
Use minimally to maintain pure aesthetic focus
- **color-success-default**: `#34D399` - Win indicators
- **color-success-light**: `bg-[#ECFDF5]` - Win background areas
- **color-neutral-default**: `#6B7280` - Draw/neutral states
- **color-neutral-light**: `bg-[#F9FAFB]` - Neutral background areas

## Typography
- **Font Stack**:
  - **font-family-base**: `-apple-system, BlinkMacSystemFont, "Segoe UI", "Roboto", "Helvetica Neue", Arial, sans-serif` — Clean sans-serif for clarity

- **Font Size & Weight**:
  - **Caption**: 10px / 400 - Navigation labels, timestamps
  - **Body small**: 12px / 400 - Supporting information
  - **Body default**: 14px / 400 - Standard content
  - **Score Text**: 16px / 600 - Score numbers
  - **Card Title**: 14px / 600 - Team names, match titles
  - **Page Title**: 20px / 600 - Section headers
  - **Score Display**: 24px / 700 - Large score emphasis
  - **Hero Score**: 32px / 700 - Featured match scores

- **Line Height**: 1.4

## Border Radius
- **Minimal**: 4px — Small elements, tags
- **Small**: 6px — Buttons, inputs
- **Medium**: 8px — Cards, containers
- **Large**: 12px — Main content cards

## Layout & Spacing
- **Spacing Scale**:
  - **Base Unit**: 4px
  - **Tight**: 8px - Card internal spacing
  - **Compact**: 12px - List item gaps
  - **Standard**: 16px - Section spacing, card margins
  - **Generous**: 24px - Major section separation

## Create Boundaries (contrast of surface color, borders, shadows)
Pure surface color contrast creates all visual hierarchy and boundaries
### Borders
- **case 1**: No borders - Primary approach using only background color differentiation
- **case 2**: If absolutely needed for data clarity:
  - **Minimal**: 1px solid #F1F5F9 - Extremely subtle table divisions only

### Dividers
- **case 1**: No dividers - Use spacing and background color contrast
- **case 2**: If needed for complex data tables: `border-t border-[#F1F5F9]`

### Shadows & Effects
- **case 1**: No shadows - Maintain pure flat design aesthetic

## Assets
### Image
- For normal `<img>`: object-cover
- For team logos: object-contain to preserve aspect ratios
- For background images: object-cover brightness-95

### Logo
- To protect copyright, do **NOT** use real product logos as a logo for a new product, individual user, or other company products.
- **Icon-based**:
  - **Graphic**: Use a simple sports-related FontAwesome Solid icon (e.g., `fa-trophy` for victories, `fa-futbol` for sports focus).

### Icon
- Use Lucide icons from Iconify for consistent line weight and clarity.
- To ensure aesthetic layout, each icon should be centered in a square container matching the icon's size.
- Use Tailwind font size to control icon size
- Example:
  ```html
  <div class="flex items-center justify-center bg-transparent w-4 h-4">
    <iconify-icon icon="lucide:trophy" class="text-base"></iconify-icon>
  </div>
  ```

## Page Layout - Mobile
```html
<!-- Mobile Layout Template: SportScore optimized for sports content -->
<body class="w-[390px] min-h-[844px] bg-[#F8FAFB] font-['-apple-system','BlinkMacSystemFont','Segoe_UI','Roboto','Helvetica_Neue',Arial,sans-serif] leading-[1.4]">

  <!-- Top Fixed Header: Contains status bar safe area and navigation bar -->
  <div class="z-10 fixed top-0 w-full bg-[#F8FAFB]">
    <!-- Default Top Safe Area -->
    <div class="h-[env(safe-area-inset-top,0px)]"></div>
    <!-- Top Navigation Bar: Standard height of 56px (h-14) -->
    <header class="h-14 flex items-center justify-between px-4 bg-white">
      <!-- Navigation content goes here -->
    </header>
  </div>

  <!-- Top Spacer: Pushes content down to avoid overlapping with the fixed header -->
  <div>
    <!-- h should match the top safe area height -->
    <div class="h-[env(safe-area-inset-top,0px)]"></div>
    <!-- h should match the navigation bar height -->
    <div class="h-14"></div>
  </div>

  <!-- Main Scrollable Content Area -->
  <main class="pb-4 space-y-3">
    <!-- Main content goes here, use section with horizontal page padding(px-4) -->
    <section class="px-4 space-y-3">
    </section>
  </main>

  <!-- Bottom Spacer: Avoid overlapping with the fixed bottom bars -->
  <div>
    <!-- mt is an additional margin, h should match the Bottom Navigation height -->
    <div class="mt-4 h-[72px]"></div>
    <!-- h equals to Bottom Safe Area -->
    <div class="h-[env(safe-area-inset-bottom,0px)]"></div>
  </div>

  <!-- Bottom Fixed Area: Contains bottom navigation and bottom safe area -->
  <div class="z-10 fixed bottom-0 w-full flex flex-col">
    <!-- Bottom Navigation container -->
    <div class="bg-white border-t border-[#F1F5F9]">
      <!-- Bottom Navigation layout -->
      <nav class="flex justify-around py-3 px-1">
        <!-- Navigation Item: flex-1; text-[#A0AEC0](Default); text-[#1E3A5F](Active) -->
        <div class="flex flex-1 flex-col items-center gap-1">
          <div class="w-6 h-6 flex items-center justify-center">
            <iconify-icon icon="lucide:home" class="text-[#A0AEC0]"></iconify-icon>
          </div>
          <span class="text-[10px] font-normal text-[#A0AEC0]">Home</span>
        </div>
      </nav>
      <!-- Default Bottom Safe Area-->
      <div class="h-[env(safe-area-inset-bottom,0px)]"></div>
    </div>
  </div>
</body>
```

## Tailwind Component Examples
### Basic
- **Progress bars**: h-1
- **Button**:
  - Primary button:
    - button: flex items-center justify-center bg-[#1E3A5F] px-4 py-2 rounded-md
      - span: text-white text-sm font-medium
  - Secondary button:
    - button: flex items-center justify-center bg-[#F3F5F7] px-4 py-2 rounded-md
      - span: text-[#1E3A5F] text-sm font-medium
- **Label/Tag/Badge**:
  - Live indicator:
    - div: flex items-center bg-[#ECFDF5] px-2 py-1 rounded
      - span: text-[#059669] text-xs font-medium

### Data Entry
- **Input Field**:
  - div: relative
    - input: w-full bg-white border-0 px-3 py-2 rounded-md text-sm placeholder-[#A0AEC0]

### Container
- **Score Card**:
  - div: bg-white rounded-lg p-4 space-y-3
    - Match info and scores content
- **Match List Item**:
  - div: bg-white p-3 space-y-2 first:rounded-t-lg last:rounded-b-lg
    - Team and score information

## Additional Notes
This style guide emphasizes visual purity through surface color differentiation rather than borders or shadows. The deep navy blue (#1E3A5F) provides authoritative presence for sports data while maintaining readability. All visual hierarchy is achieved through careful spacing, typography weight, and subtle background color variations to create a focused, distraction-free sports viewing experience.

<colors_extraction>
#1E3A5F
#2C4A6B
#16304C
#F8FAFB
#FFFFFF
#FAFBFC
#F3F5F7
#F0F2F4
#4A5568
#718096
#A0AEC0
#34D399
#ECFDF5
#6B7280
#F9FAFB
#F1F5F9
#059669
</colors_extraction>