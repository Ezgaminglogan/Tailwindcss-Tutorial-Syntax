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

## ✅ Practice Exercise

Create a profile card with:
- White background with shadow
- Profile image placeholder (gray background, rounded)
- Name (large, bold)
- Bio text (gray color)
- "Follow" button (blue background)

Try building it yourself before checking the solution!

---

## 🔗 Next Steps

Continue to [02 - Layouts & Flexbox](02-layouts.md) to learn how to build complex layouts!

