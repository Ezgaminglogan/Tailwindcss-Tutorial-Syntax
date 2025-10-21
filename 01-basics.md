# 01 - Tailwind CSS Basics

## What is Tailwind CSS?

Tailwind CSS is a utility-first CSS framework. Instead of writing custom CSS, you apply pre-built classes directly to HTML elements.

## Core Concept: Utility Classes

Traditional CSS:
```css
.button {
  background-color: blue;
  padding: 1rem 2rem;
  border-radius: 0.5rem;
}
```

Tailwind Way:
```html
<button class="bg-blue-500 px-8 py-4 rounded-lg">Click Me</button>
```

---

## 🎨 Colors

### Syntax: `{property}-{color}-{shade}`

```html
<!-- Text Colors -->
<p class="text-red-500">Red text</p>
<p class="text-blue-700">Blue text</p>
<p class="text-green-400">Green text</p>

<!-- Background Colors -->
<div class="bg-purple-500">Purple background</div>
<div class="bg-gray-200">Gray background</div>
<div class="bg-yellow-300">Yellow background</div>

<!-- Border Colors -->
<div class="border border-red-500">Red border</div>
```

**Color Shades:** 50, 100, 200, 300, 400, 500, 600, 700, 800, 900
- Lower numbers = lighter
- Higher numbers = darker

---

## 📏 Spacing (Padding & Margin)

### Syntax: `{property}{direction}-{size}`

**Properties:**
- `p` = padding
- `m` = margin

**Directions:**
- `t` = top
- `r` = right
- `b` = bottom
- `l` = left
- `x` = horizontal (left + right)
- `y` = vertical (top + bottom)
- (none) = all sides

**Sizes:** 0, 1, 2, 3, 4, 5, 6, 8, 10, 12, 16, 20, 24, 32...

```html
<!-- Padding Examples -->
<div class="p-4">Padding all sides</div>
<div class="px-6 py-3">Padding x=6, y=3</div>
<div class="pt-8">Padding top only</div>

<!-- Margin Examples -->
<div class="m-4">Margin all sides</div>
<div class="mx-auto">Center horizontally</div>
<div class="mt-10 mb-5">Margin top & bottom</div>
```

---

## 📝 Typography

```html
<!-- Font Size -->
<p class="text-xs">Extra small</p>
<p class="text-sm">Small</p>
<p class="text-base">Base (16px)</p>
<p class="text-lg">Large</p>
<p class="text-xl">Extra large</p>
<p class="text-2xl">2XL</p>
<p class="text-3xl">3XL</p>
<p class="text-4xl">4XL</p>

<!-- Font Weight -->
<p class="font-thin">Thin</p>
<p class="font-normal">Normal</p>
<p class="font-medium">Medium</p>
<p class="font-semibold">Semibold</p>
<p class="font-bold">Bold</p>
<p class="font-extrabold">Extra bold</p>

<!-- Text Alignment -->
<p class="text-left">Left aligned</p>
<p class="text-center">Center aligned</p>
<p class="text-right">Right aligned</p>

<!-- Text Color -->
<p class="text-gray-900">Dark gray text</p>
<p class="text-blue-600">Blue text</p>
```

---

## 🔲 Width & Height

```html
<!-- Fixed Width -->
<div class="w-32">Width 128px</div>
<div class="w-64">Width 256px</div>
<div class="w-96">Width 384px</div>

<!-- Percentage Width -->
<div class="w-1/2">50% width</div>
<div class="w-1/3">33.333% width</div>
<div class="w-1/4">25% width</div>
<div class="w-full">100% width</div>

<!-- Height -->
<div class="h-32">Height 128px</div>
<div class="h-screen">100vh height</div>
<div class="h-full">100% height</div>

<!-- Min/Max Width -->
<div class="max-w-sm">Max width small</div>
<div class="max-w-md">Max width medium</div>
<div class="max-w-lg">Max width large</div>
<div class="max-w-xl">Max width XL</div>
<div class="max-w-full">Max width 100%</div>
```

---

## 🎯 Borders & Rounded Corners

```html
<!-- Border Width -->
<div class="border">1px border</div>
<div class="border-2">2px border</div>
<div class="border-4">4px border</div>

<!-- Border Sides -->
<div class="border-t">Top border</div>
<div class="border-r">Right border</div>
<div class="border-b">Bottom border</div>
<div class="border-l">Left border</div>

<!-- Border Colors -->
<div class="border border-red-500">Red border</div>
<div class="border-2 border-blue-700">Blue border</div>

<!-- Rounded Corners -->
<div class="rounded">Small rounded (4px)</div>
<div class="rounded-md">Medium rounded</div>
<div class="rounded-lg">Large rounded</div>
<div class="rounded-xl">XL rounded</div>
<div class="rounded-full">Fully rounded (circle/pill)</div>

<!-- Round Specific Corners -->
<div class="rounded-t-lg">Top corners</div>
<div class="rounded-r-lg">Right corners</div>
```

---

## 🌟 Shadows

```html
<div class="shadow-sm">Small shadow</div>
<div class="shadow">Default shadow</div>
<div class="shadow-md">Medium shadow</div>
<div class="shadow-lg">Large shadow</div>
<div class="shadow-xl">XL shadow</div>
<div class="shadow-2xl">2XL shadow</div>
<div class="shadow-none">No shadow</div>
```

---

## 🎪 Display & Visibility

```html
<!-- Display Types -->
<div class="block">Block element</div>
<div class="inline-block">Inline-block</div>
<div class="inline">Inline element</div>
<div class="flex">Flex container</div>
<div class="grid">Grid container</div>
<div class="hidden">Hidden (display: none)</div>

<!-- Visibility -->
<div class="visible">Visible</div>
<div class="invisible">Invisible (takes space)</div>
```

---

## 📦 Complete Example

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tailwind Basics</title>
    <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
</head>
<body class="bg-gray-100 p-8">
    
    <!-- Card Example -->
    <div class="max-w-md mx-auto bg-white rounded-lg shadow-lg p-6">
        <h1 class="text-3xl font-bold text-gray-900 mb-4">Hello Tailwind!</h1>
        <p class="text-gray-700 mb-6">
            This is a card component built with Tailwind CSS utility classes.
        </p>
        <button class="bg-blue-500 text-white px-6 py-3 rounded-lg hover:bg-blue-600">
            Click Me
        </button>
    </div>

</body>
</html>
```

---

## 📍 Position

Position utilities control how elements are positioned on the page.

```html
<!-- Static (default) -->
<div class="static">Normal document flow</div>

<!-- Relative - positioned relative to its normal position -->
<div class="relative">
  <div class="absolute top-0 right-0 bg-red-500 text-white px-2 py-1 rounded">
    Badge
  </div>
</div>

<!-- Absolute - positioned relative to nearest positioned ancestor -->
<div class="relative h-32 bg-gray-200">
  <div class="absolute top-4 right-4">Top Right</div>
  <div class="absolute bottom-4 left-4">Bottom Left</div>
  <div class="absolute inset-0 flex items-center justify-center">
    Centered
  </div>
</div>

<!-- Fixed - positioned relative to viewport -->
<button class="fixed bottom-4 right-4 bg-blue-600 text-white p-4 rounded-full shadow-lg">
  💬
</button>

<!-- Sticky - toggles between relative and fixed -->
<div class="sticky top-0 bg-white shadow-md p-4 z-10">
  Sticky Header
</div>
```

### Position Values

```html
<!-- Top/Right/Bottom/Left -->
<div class="absolute top-0">Top edge</div>
<div class="absolute right-0">Right edge</div>
<div class="absolute bottom-0">Bottom edge</div>
<div class="absolute left-0">Left edge</div>

<!-- Numeric Values -->
<div class="absolute top-4 right-8">Top 16px, Right 32px</div>

<!-- Inset (all sides) -->
<div class="absolute inset-0">All sides 0</div>
<div class="absolute inset-4">All sides 16px</div>
<div class="absolute inset-x-0">Left & Right 0</div>
<div class="absolute inset-y-0">Top & Bottom 0</div>
```

---

## 🎚️ Z-Index

Controls the stacking order of elements.

```html
<!-- Z-Index Values: 0, 10, 20, 30, 40, 50 -->
<div class="relative">
  <div class="absolute z-0 bg-blue-500">Behind (z-0)</div>
  <div class="absolute z-10 bg-red-500">Middle (z-10)</div>
  <div class="absolute z-20 bg-green-500">Front (z-20)</div>
  <div class="absolute z-50 bg-yellow-500">Top (z-50)</div>
</div>

<!-- Common Use Case: Modal Overlay -->
<div class="fixed inset-0 bg-black bg-opacity-50 z-40">
  <div class="relative z-50 bg-white p-6 rounded-lg">
    Modal Content
  </div>
</div>
```

---

## 📦 Overflow

Controls how content overflows its container.

```html
<!-- Overflow Auto - Add scrollbar when needed -->
<div class="h-32 overflow-auto">
  <p>Long content that will scroll...</p>
</div>

<!-- Overflow Hidden - Clip content -->
<div class="h-32 overflow-hidden">
  <p>Content is clipped</p>
</div>

<!-- Overflow Scroll - Always show scrollbar -->
<div class="h-32 overflow-scroll">
  <p>Content with scrollbar</p>
</div>

<!-- Overflow Visible - Content can overflow -->
<div class="h-32 overflow-visible">
  <p>Content can overflow container</p>
</div>

<!-- Directional Overflow -->
<div class="h-32 overflow-x-auto overflow-y-hidden">
  Horizontal scroll only
</div>
```

---

## 🔤 Advanced Typography

### Line Height

```html
<p class="leading-none">Tight line height</p>
<p class="leading-tight">Tight (1.25)</p>
<p class="leading-snug">Snug (1.375)</p>
<p class="leading-normal">Normal (1.5)</p>
<p class="leading-relaxed">Relaxed (1.625)</p>
<p class="leading-loose">Loose (2)</p>
```

### Letter Spacing

```html
<p class="tracking-tighter">Tighter spacing</p>
<p class="tracking-tight">Tight spacing</p>
<p class="tracking-normal">Normal spacing</p>
<p class="tracking-wide">Wide spacing</p>
<p class="tracking-wider">Wider spacing</p>
<p class="tracking-widest">Widest spacing</p>
```

### Text Decoration

```html
<p class="underline">Underlined text</p>
<p class="line-through">Strikethrough text</p>
<p class="no-underline">No underline</p>

<!-- Decoration Style -->
<p class="underline decoration-solid">Solid underline</p>
<p class="underline decoration-double">Double underline</p>
<p class="underline decoration-dotted">Dotted underline</p>
<p class="underline decoration-dashed">Dashed underline</p>
<p class="underline decoration-wavy">Wavy underline</p>

<!-- Decoration Color -->
<p class="underline decoration-blue-500">Blue underline</p>
<p class="underline decoration-2">Thick underline</p>
```

### Text Transform

```html
<p class="uppercase">uppercase text</p>
<p class="lowercase">LOWERCASE TEXT</p>
<p class="capitalize">capitalize each word</p>
<p class="normal-case">Normal Case</p>
```

### Text Overflow

```html
<!-- Truncate - Single line with ellipsis -->
<p class="truncate w-48">
  This is a very long text that will be truncated with ellipsis
</p>

<!-- Text Ellipsis -->
<p class="overflow-hidden text-ellipsis whitespace-nowrap w-48">
  Long text with ellipsis
</p>

<!-- Line Clamp (multiple lines) -->
<p class="line-clamp-2">
  This text will be clamped to 2 lines and show ellipsis after that...
</p>
```

### Whitespace

```html
<p class="whitespace-normal">Normal whitespace handling</p>
<p class="whitespace-nowrap">Text will not wrap to new line</p>
<p class="whitespace-pre">Preserves    spaces   and
line breaks</p>
<p class="whitespace-pre-line">Preserves line breaks but collapses spaces</p>
```

---

## 🎨 Opacity

Controls the transparency of elements.

```html
<!-- Opacity values: 0, 5, 10, 20, 25, 30, 40, 50, 60, 70, 75, 80, 90, 95, 100 -->
<div class="opacity-0">Invisible (0%)</div>
<div class="opacity-25">25% opacity</div>
<div class="opacity-50">50% opacity</div>
<div class="opacity-75">75% opacity</div>
<div class="opacity-100">Fully visible (100%)</div>

<!-- Hover Opacity -->
<button class="bg-blue-600 text-white px-4 py-2 hover:opacity-80">
  Hover Me
</button>

<!-- Image Overlay -->
<div class="relative">
  <img src="image.jpg" alt="Photo">
  <div class="absolute inset-0 bg-black opacity-50"></div>
</div>
```

---

## 🖱️ Cursor

Controls the cursor appearance on hover.

```html
<button class="cursor-pointer">Pointer cursor</button>
<button class="cursor-not-allowed" disabled>Not allowed</button>
<div class="cursor-wait">Wait cursor</div>
<div class="cursor-help">Help cursor</div>
<div class="cursor-move">Move cursor</div>
<div class="cursor-text">Text cursor</div>
<div class="cursor-default">Default cursor</div>
<div class="cursor-none">No cursor</div>
```

---

## 👆 User Select

Controls whether users can select text.

```html
<p class="select-none">Cannot select this text</p>
<p class="select-text">Can select this text</p>
<p class="select-all">Click to select all</p>
<p class="select-auto">Auto (default behavior)</p>
```

---

## ✅ Practice Exercise

Create a profile card with:
- White background with shadow
- Profile image placeholder (gray background, rounded)
- Name (large, bold)
- Bio text (gray color)
- "Follow" button (blue background)
- Add a "New" badge positioned at the top-right corner using `absolute`

Try building it yourself before checking the solution!

---

## 🔗 Next Steps

Continue to [02 - Layouts & Flexbox](02-layouts.md) to learn how to build complex layouts!

