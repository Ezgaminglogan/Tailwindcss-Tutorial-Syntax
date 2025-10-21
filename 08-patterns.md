# 08 - Common Patterns & Tips

## 🎨 Hover Effects

```html
<!-- Button Hover -->
<button class="bg-blue-600 hover:bg-blue-700 hover:shadow-lg transition-all">
  Hover Me
</button>

<!-- Card Hover -->
<div class="bg-white rounded-lg shadow hover:shadow-2xl hover:scale-105 transition-all">
  Card content
</div>

<!-- Text Hover -->
<a href="#" class="text-blue-600 hover:underline hover:text-blue-800">
  Link
</a>
```

## 🌈 Gradients

```html
<!-- Background Gradients -->
<div class="bg-gradient-to-r from-blue-500 to-purple-600">
  Gradient background
</div>

<div class="bg-gradient-to-br from-pink-400 via-purple-500 to-indigo-600">
  Multi-color gradient
</div>
```

## 💫 Transitions

```html
<button class="bg-blue-600 transition-colors duration-300 hover:bg-blue-700">
  Smooth Color Change
</button>

<div class="transition-all duration-500 hover:scale-110">
  Smooth Scale
</div>
```

## 🎯 Centering Techniques

```html
<!-- Center with Flexbox -->
<div class="flex items-center justify-center h-screen">
  <div>Centered Content</div>
</div>

<!-- Center Block Element -->
<div class="max-w-md mx-auto">
  Horizontally centered
</div>
```

## 📐 Common Spacing Scale

- `p-1` = 4px
- `p-2` = 8px
- `p-4` = 16px
- `p-6` = 24px
- `p-8` = 32px
- `p-10` = 40px
- `p-12` = 48px

---

## 🔄 Transforms

Transform elements with scale, rotate, translate, and skew:

```html
<!-- Scale -->
<div class="scale-50">50% size</div>
<div class="scale-75">75% size</div>
<div class="scale-100">Normal size</div>
<div class="scale-125">125% size</div>
<div class="scale-150">150% size</div>

<!-- Scale on Hover -->
<button class="hover:scale-110 transition-transform">
  Grows on hover
</button>

<!-- Rotate -->
<div class="rotate-0">No rotation</div>
<div class="rotate-45">45 degrees</div>
<div class="rotate-90">90 degrees</div>
<div class="rotate-180">180 degrees</div>
<div class="-rotate-45">-45 degrees</div>

<!-- Rotate on Hover -->
<img src="icon.svg" class="hover:rotate-180 transition-transform duration-500">

<!-- Translate (Move) -->
<div class="translate-x-4">Move right 16px</div>
<div class="translate-y-4">Move down 16px</div>
<div class="-translate-x-4">Move left 16px</div>
<div class="-translate-y-1/2">Move up 50%</div>

<!-- Combined Transforms -->
<div class="hover:scale-110 hover:rotate-3 transition-all">
  Scale and rotate on hover
</div>

<!-- Transform Origin -->
<div class="origin-center rotate-45">Rotate from center (default)</div>
<div class="origin-top-left rotate-45">Rotate from top-left</div>
<div class="origin-bottom-right rotate-45">Rotate from bottom-right</div>

<!-- Skew -->
<div class="skew-x-12">Skew horizontal</div>
<div class="skew-y-6">Skew vertical</div>
<div class="-skew-x-12">Skew left</div>
```

---

## 🎬 Animations

Built-in animations for common use cases:

```html
<!-- Spin Animation -->
<div class="animate-spin rounded-full h-12 w-12 border-4 border-gray-200 border-t-blue-600"></div>

<!-- Ping Animation (Pulsing Dot) -->
<div class="relative">
  <div class="animate-ping absolute h-12 w-12 rounded-full bg-blue-400 opacity-75"></div>
  <div class="relative h-12 w-12 rounded-full bg-blue-500"></div>
</div>

<!-- Pulse Animation (Fade in/out) -->
<div class="animate-pulse bg-gray-300 h-32 w-32 rounded"></div>

<!-- Bounce Animation -->
<div class="animate-bounce bg-blue-600 p-4 rounded">
  ↓ Bouncing
</div>

<!-- Skeleton Loader with Pulse -->
<div class="animate-pulse space-y-4">
  <div class="h-4 bg-gray-300 rounded w-3/4"></div>
  <div class="h-4 bg-gray-300 rounded"></div>
  <div class="h-4 bg-gray-300 rounded w-5/6"></div>
</div>

<!-- Custom Animation Duration -->
<div class="animate-spin animate-duration-[3s]">Slow spin (requires custom config)</div>
```

---

## ⏱️ Transition Properties & Duration

Fine-tune transition behavior:

```html
<!-- Transition Properties -->
<div class="transition-none">No transition</div>
<div class="transition-all">Transition all properties</div>
<div class="transition-colors">Only colors</div>
<div class="transition-opacity">Only opacity</div>
<div class="transition-shadow">Only shadow</div>
<div class="transition-transform">Only transform</div>

<!-- Duration -->
<button class="bg-blue-600 hover:bg-blue-700 transition duration-75">Fast (75ms)</button>
<button class="bg-blue-600 hover:bg-blue-700 transition duration-150">Default (150ms)</button>
<button class="bg-blue-600 hover:bg-blue-700 transition duration-300">Medium (300ms)</button>
<button class="bg-blue-600 hover:bg-blue-700 transition duration-500">Slow (500ms)</button>
<button class="bg-blue-600 hover:bg-blue-700 transition duration-1000">Very slow (1s)</button>

<!-- Easing (Timing Functions) -->
<div class="transition ease-linear">Linear</div>
<div class="transition ease-in">Ease in</div>
<div class="transition ease-out">Ease out</div>
<div class="transition ease-in-out">Ease in-out</div>

<!-- Delay -->
<div class="transition delay-75">75ms delay</div>
<div class="transition delay-150">150ms delay</div>
<div class="transition delay-300">300ms delay</div>

<!-- Combined Example -->
<button class="bg-blue-600 hover:bg-blue-700 hover:scale-110 transition-all duration-300 ease-in-out">
  Smooth hover effect
</button>
```

---

## 👥 Group Hover

Apply styles to children when hovering parent:

```html
<!-- Basic Group Hover -->
<div class="group">
  <img src="photo.jpg" class="group-hover:scale-110 transition-transform">
  <h3 class="group-hover:text-blue-600 transition-colors">Hover the card</h3>
</div>

<!-- Card with Group Hover -->
<div class="group bg-white rounded-lg shadow hover:shadow-2xl transition-all p-6">
  <img src="product.jpg" class="group-hover:scale-105 transition-transform">
  <h3 class="text-xl font-bold group-hover:text-blue-600">Product Name</h3>
  <p class="text-gray-600 group-hover:text-gray-900">Description</p>
  <button class="opacity-0 group-hover:opacity-100 transition-opacity bg-blue-600 text-white px-4 py-2 rounded">
    Add to Cart
  </button>
</div>

<!-- Multiple Elements -->
<a href="#" class="group block">
  <div class="flex items-center gap-4">
    <img src="avatar.jpg" class="w-12 h-12 rounded-full group-hover:ring-4 ring-blue-500 transition">
    <div>
      <h4 class="font-bold group-hover:text-blue-600">John Doe</h4>
      <p class="text-sm text-gray-600 group-hover:text-gray-900">View Profile</p>
    </div>
    <svg class="ml-auto w-5 h-5 opacity-0 group-hover:opacity-100 transition-opacity" fill="none" stroke="currentColor" viewBox="0 0 24 24">
      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"></path>
    </svg>
  </div>
</a>

<!-- Nested Groups -->
<div class="group/card">
  <div class="group/button">
    <button class="group-hover/button:bg-blue-700">Button in Card</button>
  </div>
</div>
```

---

## 🔗 Peer State

Style elements based on sibling state:

```html
<!-- Peer with Checkbox -->
<div class="flex items-center gap-2">
  <input type="checkbox" id="terms" class="peer">
  <label for="terms" class="peer-checked:text-blue-600 peer-checked:font-bold">
    I agree to terms
  </label>
</div>

<!-- Show/Hide based on Checkbox -->
<div>
  <input type="checkbox" id="show" class="peer">
  <label for="show">Show details</label>
  <div class="hidden peer-checked:block mt-4 p-4 bg-gray-100 rounded">
    Hidden content that appears when checked
  </div>
</div>

<!-- Radio Button Tabs -->
<div>
  <input type="radio" name="tab" id="tab1" class="peer/tab1 hidden" checked>
  <input type="radio" name="tab" id="tab2" class="peer/tab2 hidden">
  
  <div class="flex gap-2 mb-4">
    <label for="tab1" class="peer-checked/tab1:bg-blue-600 peer-checked/tab1:text-white px-4 py-2 rounded cursor-pointer">
      Tab 1
    </label>
    <label for="tab2" class="peer-checked/tab2:bg-blue-600 peer-checked/tab2:text-white px-4 py-2 rounded cursor-pointer">
      Tab 2
    </label>
  </div>
  
  <div class="hidden peer-checked/tab1:block">Content for Tab 1</div>
  <div class="hidden peer-checked/tab2:block">Content for Tab 2</div>
</div>

<!-- Input Focus Peer -->
<div class="relative">
  <input type="text" class="peer border-2 rounded px-4 py-2 w-full focus:outline-none focus:border-blue-600">
  <label class="absolute left-4 top-2 text-gray-500 peer-focus:text-blue-600 peer-focus:-top-6 peer-focus:text-sm transition-all">
    Email
  </label>
</div>
```

---

## 🌙 Dark Mode

Adapt styles for dark mode:

```html
<!-- Basic Dark Mode -->
<div class="bg-white dark:bg-gray-900 text-black dark:text-white">
  Adapts to dark mode
</div>

<!-- Dark Mode Card -->
<div class="bg-white dark:bg-gray-800 rounded-lg shadow-lg p-6">
  <h2 class="text-gray-900 dark:text-white text-2xl font-bold">Title</h2>
  <p class="text-gray-600 dark:text-gray-300">Description text</p>
  <button class="bg-blue-600 dark:bg-blue-500 text-white px-4 py-2 rounded hover:bg-blue-700 dark:hover:bg-blue-600">
    Button
  </button>
</div>

<!-- Dark Mode Borders -->
<div class="border border-gray-200 dark:border-gray-700 rounded p-4">
  Content with adaptive border
</div>

<!-- Dark Mode Images -->
<img src="logo-light.svg" class="dark:hidden">
<img src="logo-dark.svg" class="hidden dark:block">

<!-- Full Dark Mode Layout -->
<body class="bg-gray-50 dark:bg-gray-900">
  <nav class="bg-white dark:bg-gray-800 border-b border-gray-200 dark:border-gray-700 px-6 py-4">
    <div class="flex items-center justify-between">
      <h1 class="text-xl font-bold text-gray-900 dark:text-white">My App</h1>
      <button class="text-gray-600 dark:text-gray-300 hover:text-gray-900 dark:hover:text-white">
        Menu
      </button>
    </div>
  </nav>
</body>
```

---

## 🎭 Filters & Effects

Apply visual filters to elements:

```html
<!-- Blur -->
<img src="photo.jpg" class="blur-none">
<img src="photo.jpg" class="blur-sm">
<img src="photo.jpg" class="blur-md">
<img src="photo.jpg" class="blur-lg">
<img src="photo.jpg" class="blur-xl">
<img src="photo.jpg" class="blur-2xl">

<!-- Blur on Hover (Remove blur) -->
<img src="photo.jpg" class="blur-sm hover:blur-none transition-all">

<!-- Brightness -->
<img src="photo.jpg" class="brightness-50">  <!-- Darker -->
<img src="photo.jpg" class="brightness-100"> <!-- Normal -->
<img src="photo.jpg" class="brightness-150"> <!-- Brighter -->

<!-- Contrast -->
<img src="photo.jpg" class="contrast-50">   <!-- Low contrast -->
<img src="photo.jpg" class="contrast-100">  <!-- Normal -->
<img src="photo.jpg" class="contrast-150">  <!-- High contrast -->

<!-- Grayscale -->
<img src="photo.jpg" class="grayscale-0">    <!-- Full color -->
<img src="photo.jpg" class="grayscale">      <!-- Black and white -->

<!-- Grayscale on Hover -->
<img src="photo.jpg" class="grayscale hover:grayscale-0 transition-all">

<!-- Saturate -->
<img src="photo.jpg" class="saturate-0">     <!-- Desaturated -->
<img src="photo.jpg" class="saturate-50">    <!-- Less saturated -->
<img src="photo.jpg" class="saturate-100">   <!-- Normal -->
<img src="photo.jpg" class="saturate-150">   <!-- More saturated -->

<!-- Sepia -->
<img src="photo.jpg" class="sepia">          <!-- Sepia tone -->

<!-- Hue Rotate -->
<img src="photo.jpg" class="hue-rotate-0">
<img src="photo.jpg" class="hue-rotate-90">
<img src="photo.jpg" class="hue-rotate-180">

<!-- Invert -->
<img src="photo.jpg" class="invert">         <!-- Inverted colors -->

<!-- Combined Filters -->
<img src="photo.jpg" class="contrast-125 brightness-110 saturate-150">

<!-- Drop Shadow -->
<img src="icon.svg" class="drop-shadow-sm">
<img src="icon.svg" class="drop-shadow">
<img src="icon.svg" class="drop-shadow-lg">
<img src="icon.svg" class="drop-shadow-xl">
<img src="icon.svg" class="drop-shadow-2xl">
```

---

## 🪟 Backdrop Filters

Apply filters to background behind element:

```html
<!-- Backdrop Blur (Glass Effect) -->
<div class="relative">
  <img src="background.jpg" class="w-full h-64 object-cover">
  <div class="absolute inset-0 flex items-center justify-center">
    <div class="backdrop-blur-sm bg-white/30 p-8 rounded-lg">
      <h2 class="text-2xl font-bold">Frosted Glass Effect</h2>
    </div>
  </div>
</div>

<!-- Different Blur Intensities -->
<div class="backdrop-blur-none">No blur</div>
<div class="backdrop-blur-sm">Small blur</div>
<div class="backdrop-blur">Medium blur</div>
<div class="backdrop-blur-lg">Large blur</div>
<div class="backdrop-blur-xl">XL blur</div>

<!-- Modal with Backdrop Blur -->
<div class="fixed inset-0 backdrop-blur-sm bg-black/50 flex items-center justify-center">
  <div class="bg-white rounded-lg shadow-2xl p-8 max-w-md">
    <h2 class="text-2xl font-bold mb-4">Modal Title</h2>
    <p>Modal content with blurred background</p>
  </div>
</div>

<!-- Card with Glass Effect -->
<div class="relative bg-gradient-to-br from-purple-500 to-pink-500 p-8">
  <div class="backdrop-blur-md bg-white/20 rounded-lg p-6 border border-white/20">
    <h3 class="text-white text-xl font-bold mb-2">Glass Card</h3>
    <p class="text-white/90">Beautiful frosted glass effect</p>
  </div>
</div>

<!-- Backdrop Brightness -->
<div class="backdrop-brightness-50">Darken background</div>
<div class="backdrop-brightness-150">Brighten background</div>

<!-- Combined Backdrop Effects -->
<div class="backdrop-blur-lg backdrop-brightness-75 backdrop-saturate-150">
  Multiple backdrop effects
</div>
```

---

## 🎯 Interactive State Modifiers

Style elements based on various states:

```html
<!-- Active State (When clicking) -->
<button class="bg-blue-600 active:bg-blue-800 active:scale-95">
  Click me
</button>

<!-- Disabled State -->
<button class="bg-blue-600 disabled:bg-gray-400 disabled:cursor-not-allowed" disabled>
  Disabled button
</button>

<!-- Focus States -->
<input class="border-2 focus:border-blue-600 focus:ring-4 focus:ring-blue-200 focus:outline-none">

<!-- Focus Visible (Only keyboard focus) -->
<button class="focus:ring-2 focus-visible:ring-blue-600">
  Focus visible
</button>

<!-- Focus Within (When child is focused) -->
<form class="border-2 focus-within:border-blue-600 p-4">
  <input class="border rounded px-4 py-2">
</form>

<!-- Visited Links -->
<a href="#" class="text-blue-600 visited:text-purple-600">
  Link (changes when visited)
</a>

<!-- First, Last, Odd, Even -->
<ul>
  <li class="first:font-bold">First item (bold)</li>
  <li class="odd:bg-gray-100">Item 2</li>
  <li class="odd:bg-gray-100">Item 3</li>
  <li class="last:text-red-600">Last item (red)</li>
</ul>

<!-- Empty State -->
<div class="empty:hidden">
  <!-- Hidden when empty -->
</div>

<!-- Required/Invalid (Form validation) -->
<input required class="border-2 invalid:border-red-500 valid:border-green-500">

<!-- Placeholder Shown -->
<input placeholder="Email" class="placeholder-shown:border-gray-300">
```

---

## 📏 Responsive Variants

Combine with breakpoints:

```html
<!-- Responsive Hover (Only on large screens) -->
<button class="lg:hover:scale-110">
  Hover effect only on desktop
</button>

<!-- Dark Mode + Responsive -->
<div class="bg-white dark:bg-gray-900 md:bg-gray-100 md:dark:bg-gray-800">
  Complex responsive + dark mode
</div>

<!-- Group Hover + Responsive -->
<div class="group md:hover:shadow-lg">
  <h3 class="md:group-hover:text-blue-600">Title</h3>
</div>
```

---

## ✨ Pro Tips

1. Use `max-w-` classes to control content width
2. Use `mx-auto` to center containers
3. Use `gap-` instead of margins for spacing in flex/grid
4. Use `focus:` and `focus-visible:` states for accessibility
5. Combine hover with `transition-` for smooth effects
6. Use `group` for coordinated hover effects
7. Use `peer` for reactive sibling states
8. Add `dark:` variants for dark mode support
9. Combine transforms for creative effects
10. Use backdrop filters for glassmorphism designs

---

## 🎨 Advanced Pattern Examples

### Animated Button

```html
<button class="relative overflow-hidden bg-blue-600 text-white px-8 py-3 rounded-lg font-semibold transition-all hover:scale-105 active:scale-95 hover:shadow-lg group">
  <span class="relative z-10">Hover Me</span>
  <div class="absolute inset-0 bg-gradient-to-r from-blue-600 to-purple-600 opacity-0 group-hover:opacity-100 transition-opacity"></div>
</button>
```

### Floating Action Button

```html
<button class="fixed bottom-8 right-8 bg-blue-600 text-white w-14 h-14 rounded-full shadow-lg hover:shadow-2xl hover:scale-110 transition-all animate-bounce z-50">
  <svg class="w-6 h-6 mx-auto" fill="none" stroke="currentColor" viewBox="0 0 24 24">
    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4v16m8-8H4"></path>
  </svg>
</button>
```

### Image Overlay Card

```html
<div class="group relative overflow-hidden rounded-lg">
  <img src="photo.jpg" class="w-full h-64 object-cover group-hover:scale-110 transition-transform duration-500">
  <div class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent opacity-0 group-hover:opacity-100 transition-opacity flex items-end">
    <div class="p-6 text-white">
      <h3 class="text-xl font-bold">Title</h3>
      <p class="text-sm">Description appears on hover</p>
    </div>
  </div>
</div>
```

---

## 🎉 You're Done!

Congratulations! You now have comprehensive knowledge of Tailwind CSS, including:
- ✅ Core utilities (colors, spacing, typography)
- ✅ Layout systems (Flexbox & Grid)
- ✅ Components (buttons, cards, forms)
- ✅ Animations & Transforms
- ✅ Interactive States
- ✅ Filters & Effects
- ✅ Dark Mode
- ✅ Responsive Design

Keep practicing and building amazing projects! 🚀

