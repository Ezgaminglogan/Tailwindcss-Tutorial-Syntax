# 10 - Advanced Utilities & Special Features

## 📦 Container

Center and constrain content width responsively:

```html
<!-- Basic Container -->
<div class="container">
  Content constrained to max-width with automatic margins
</div>

<!-- Container with Padding -->
<div class="container mx-auto px-4">
  Centered container with horizontal padding
</div>

<!-- Container Behavior:
sm (640px):   max-width: 640px
md (768px):   max-width: 768px
lg (1024px):  max-width: 1024px
xl (1280px):  max-width: 1280px
2xl (1536px): max-width: 1536px
-->

<!-- Common Usage -->
<div class="container mx-auto px-4 py-8">
  <h1 class="text-4xl font-bold mb-6">Page Title</h1>
  <p class="text-gray-700">
    Content automatically adjusts width based on screen size
  </p>
</div>
```

---

## 🎨 Mix Blend Mode

Control how element colors blend with background:

```html
<!-- Blend Modes -->
<div class="mix-blend-normal">Normal</div>
<div class="mix-blend-multiply">Multiply</div>
<div class="mix-blend-screen">Screen</div>
<div class="mix-blend-overlay">Overlay</div>
<div class="mix-blend-darken">Darken</div>
<div class="mix-blend-lighten">Lighten</div>
<div class="mix-blend-color-dodge">Color dodge</div>
<div class="mix-blend-color-burn">Color burn</div>
<div class="mix-blend-hard-light">Hard light</div>
<div class="mix-blend-soft-light">Soft light</div>
<div class="mix-blend-difference">Difference</div>
<div class="mix-blend-exclusion">Exclusion</div>
<div class="mix-blend-hue">Hue</div>
<div class="mix-blend-saturation">Saturation</div>
<div class="mix-blend-color">Color</div>
<div class="mix-blend-luminosity">Luminosity</div>

<!-- Practical Example: Text Over Image -->
<div class="relative">
  <img src="background.jpg" class="w-full h-64 object-cover">
  <h2 class="absolute inset-0 flex items-center justify-center text-6xl font-bold text-white mix-blend-difference">
    Blend Text
  </h2>
</div>

<!-- Overlay with Blend -->
<div class="relative">
  <img src="photo.jpg">
  <div class="absolute inset-0 bg-blue-500 mix-blend-multiply opacity-50"></div>
</div>
```

---

## 🎭 Background Blend Mode

Blend background images with background colors:

```html
<!-- Background Blend -->
<div class="bg-blue-500 bg-cover bg-blend-multiply" style="background-image: url('image.jpg')">
  Background image blended with blue
</div>

<!-- Blend Modes -->
<div class="bg-blend-normal">Normal</div>
<div class="bg-blend-multiply">Multiply</div>
<div class="bg-blend-screen">Screen</div>
<div class="bg-blend-overlay">Overlay</div>
<div class="bg-blend-darken">Darken</div>
<div class="bg-blend-lighten">Lighten</div>
<div class="bg-blend-color-dodge">Color dodge</div>
<div class="bg-blend-color-burn">Color burn</div>
<div class="bg-blend-hard-light">Hard light</div>
<div class="bg-blend-soft-light">Soft light</div>
<div class="bg-blend-difference">Difference</div>
<div class="bg-blend-exclusion">Exclusion</div>
<div class="bg-blend-hue">Hue</div>
<div class="bg-blend-saturation">Saturation</div>
<div class="bg-blend-color">Color</div>
<div class="bg-blend-luminosity">Luminosity</div>

<!-- Duotone Effect -->
<div class="h-64 bg-purple-600 bg-cover bg-center bg-blend-multiply" style="background-image: url('photo.jpg')">
  Purple tinted photo
</div>
```

---

## 🔒 Isolation

Create new stacking context:

```html
<!-- Isolate element from parent stacking context -->
<div class="isolate">
  Creates new stacking context
</div>

<div class="isolation-auto">
  Auto isolation (default)
</div>

<!-- Use Case: Prevent blend mode from affecting siblings -->
<div>
  <div class="isolate">
    <div class="mix-blend-multiply">
      Blend mode isolated to this container
    </div>
  </div>
  <div>This won't be affected by the blend mode above</div>
</div>
```

---

## ⚡ Will Change

Optimize animations by hinting to browser:

```html
<!-- Optimize specific properties -->
<div class="will-change-transform hover:scale-110 transition">
  Optimized scale animation
</div>

<div class="will-change-scroll">
  Optimized for scrolling
</div>

<div class="will-change-contents">
  Optimized for content changes
</div>

<div class="will-change-auto">
  Auto (default)
</div>

<!-- Use Case: Smooth Animations -->
<button class="will-change-transform hover:translate-y-1 transition-transform">
  Optimized button
</button>
```

---

## 📜 Scroll Behavior

Control scrolling smoothness:

```html
<!-- Smooth Scrolling -->
<html class="scroll-smooth">
  <!-- All anchor links will smooth scroll -->
</html>

<div class="scroll-auto">Auto scroll (default)</div>

<!-- Smooth Scroll Example -->
<nav class="scroll-smooth">
  <a href="#section1">Jump to Section 1 (smooth)</a>
  <a href="#section2">Jump to Section 2 (smooth)</a>
</nav>
```

---

## 📸 Scroll Snap

Create scroll snapping effects:

```html
<!-- Scroll Snap Container -->
<div class="snap-x snap-mandatory overflow-x-auto flex gap-4">
  <div class="snap-start w-80 flex-shrink-0 h-64 bg-blue-500"></div>
  <div class="snap-start w-80 flex-shrink-0 h-64 bg-green-500"></div>
  <div class="snap-start w-80 flex-shrink-0 h-64 bg-red-500"></div>
</div>

<!-- Snap Types -->
<div class="snap-none">No snapping</div>
<div class="snap-x">Horizontal snap</div>
<div class="snap-y">Vertical snap</div>
<div class="snap-both">Both directions</div>

<!-- Snap Strictness -->
<div class="snap-mandatory">Must snap</div>
<div class="snap-proximity">Snap if close</div>

<!-- Snap Alignment -->
<div class="snap-start">Snap to start</div>
<div class="snap-end">Snap to end</div>
<div class="snap-center">Snap to center</div>

<!-- Full Screen Slider Example -->
<div class="h-screen snap-y snap-mandatory overflow-y-scroll">
  <section class="h-screen snap-start bg-blue-500 flex items-center justify-center text-white text-4xl">
    Slide 1
  </section>
  <section class="h-screen snap-start bg-green-500 flex items-center justify-center text-white text-4xl">
    Slide 2
  </section>
  <section class="h-screen snap-start bg-red-500 flex items-center justify-center text-white text-4xl">
    Slide 3
  </section>
</div>

<!-- Carousel with Snap -->
<div class="snap-x snap-mandatory overflow-x-auto flex gap-6 p-6">
  <div class="snap-center flex-shrink-0 w-64 h-96 bg-white rounded-lg shadow-lg"></div>
  <div class="snap-center flex-shrink-0 w-64 h-96 bg-white rounded-lg shadow-lg"></div>
  <div class="snap-center flex-shrink-0 w-64 h-96 bg-white rounded-lg shadow-lg"></div>
</div>
```

---

## 📝 Break Utilities

Control text and word breaking:

```html
<!-- Break Words -->
<p class="break-normal">Normal word breaking</p>
<p class="break-words">Break long words if needed</p>
<p class="break-all">Break at any character</p>
<p class="break-keep">Keep words together</p>

<!-- Hyphens -->
<p class="hyphens-none">No hyphens</p>
<p class="hyphens-manual">Manual hyphens only</p>
<p class="hyphens-auto">Auto hyphenation</p>

<!-- Example: Long URL -->
<div class="max-w-xs border p-4">
  <p class="break-words">
    https://verylongurl.com/with/many/segments/that/would/overflow
  </p>
</div>
```

---

## 📌 Content

Add content via CSS:

```html
<!-- Content Utilities -->
<div class="before:content-[''] before:block">
  Before pseudo-element
</div>

<div class="after:content-['→'] after:ml-2">
  Link after:content-['→']
</div>

<!-- Custom Content -->
<a href="#" class="after:content-['_↗'] after:text-blue-500">
  External Link
</a>

<!-- Decorative Elements -->
<h2 class="relative before:absolute before:left-0 before:top-1/2 before:-translate-y-1/2 before:w-1 before:h-full before:bg-blue-500 before:content-[''] pl-4">
  Heading with side bar
</h2>

<!-- Quote Styling -->
<blockquote class="before:content-['"'] after:content-['"'] text-xl italic">
  This is a quote
</blockquote>
```

---

## 🎯 Arbitrary Values

Use custom values when needed:

```html
<!-- Arbitrary Width -->
<div class="w-[137px]">Custom width: 137px</div>

<!-- Arbitrary Color -->
<div class="bg-[#1da1f2]">Twitter blue</div>

<!-- Arbitrary Grid -->
<div class="grid grid-cols-[200px_1fr_100px]">
  Custom grid template
</div>

<!-- Arbitrary Transform -->
<div class="rotate-[17deg]">Rotate 17 degrees</div>

<!-- Arbitrary Spacing -->
<div class="m-[13px]">Custom margin</div>

<!-- Arbitrary Font Size -->
<p class="text-[length:var(--font-size)]">CSS variable</p>

<!-- URL in Background -->
<div class="bg-[url('/img/hero.jpg')]">Custom background</div>

<!-- Complex Values -->
<div class="shadow-[0_35px_60px_-15px_rgba(0,0,0,0.3)]">
  Custom shadow
</div>

<!-- With Important -->
<div class="!m-4">Important margin (overrides other styles)</div>

<!-- Arbitrary Variants -->
<div class="[&>*]:p-4">All children get padding</div>
<div class="[&_p]:text-blue-600">All paragraph descendants blue</div>
```

---

## 🔢 Important Modifier

Override specificity with `!`:

```html
<!-- Force utility to override -->
<div class="!text-red-500">
  Always red, even if other styles apply
</div>

<!-- Use with any utility -->
<div class="!p-0">Force zero padding</div>
<div class="!hidden">Force hidden</div>
<div class="!flex">Force flex display</div>

<!-- Combine with states -->
<button class="hover:!bg-blue-700">
  Important hover state
</button>
```

---

## 📐 Accent Color

Style form controls:

```html
<!-- Checkbox Accent -->
<input type="checkbox" class="accent-blue-600">
<input type="checkbox" class="accent-green-500">
<input type="checkbox" class="accent-purple-600">

<!-- Radio Accent -->
<input type="radio" class="accent-pink-500">

<!-- Range Slider Accent -->
<input type="range" class="accent-red-500">

<!-- Progress Bar Accent -->
<progress value="70" max="100" class="accent-blue-600"></progress>
```

---

## 🎨 Caret Color

Style text cursor color:

```html
<!-- Custom Caret Color -->
<input type="text" class="caret-blue-600" placeholder="Blue cursor">
<input type="text" class="caret-red-500" placeholder="Red cursor">
<input type="text" class="caret-green-500" placeholder="Green cursor">

<!-- Auto Caret -->
<input type="text" class="caret-auto">

<!-- Combined with Focus -->
<input class="border rounded px-4 py-2 caret-blue-600 focus:caret-purple-600">
```

---

## 🔗 Appearance

Control native styling:

```html
<!-- Remove Native Styling -->
<select class="appearance-none">
  <!-- Custom styled select -->
</select>

<input type="checkbox" class="appearance-none w-6 h-6 border-2 border-gray-300 rounded checked:bg-blue-600">

<!-- Auto Appearance (default) -->
<select class="appearance-auto"></select>
```

---

## 📱 Columns

Multi-column text layout:

```html
<!-- Column Count -->
<div class="columns-1">Single column</div>
<div class="columns-2">Two columns</div>
<div class="columns-3">Three columns</div>
<div class="columns-4">Four columns</div>

<!-- Auto Columns -->
<div class="columns-auto">Auto columns</div>

<!-- Column Width -->
<div class="columns-3xs">3xs width columns</div>
<div class="columns-2xs">2xs width columns</div>
<div class="columns-xs">xs width columns</div>
<div class="columns-sm">sm width columns</div>
<div class="columns-md">md width columns</div>
<div class="columns-lg">lg width columns</div>

<!-- Newspaper Layout -->
<article class="columns-3 gap-8 text-justify">
  <p>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. 
    Text flows across multiple columns automatically.
  </p>
  <p>More paragraphs continue flowing...</p>
</article>

<!-- Break Inside -->
<div class="break-inside-auto">Can break inside (default)</div>
<div class="break-inside-avoid">Avoid breaking inside</div>
<div class="break-inside-avoid-page">Avoid page break inside</div>
<div class="break-inside-avoid-column">Avoid column break inside</div>
```

---

## 🎯 Complete Advanced Example

```html
<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Advanced Utilities Showcase</title>
    <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
</head>
<body class="bg-gray-50">
    
    <!-- Container -->
    <div class="container mx-auto px-4 py-8">
        
        <!-- Blend Mode Hero -->
        <section class="relative h-96 rounded-lg overflow-hidden mb-12">
            <img src="hero.jpg" alt="Hero" class="w-full h-full object-cover">
            <div class="absolute inset-0 bg-gradient-to-r from-purple-600 to-blue-600 mix-blend-multiply"></div>
            <div class="absolute inset-0 flex items-center justify-center">
                <h1 class="text-6xl font-bold text-white mix-blend-lighten">
                    Advanced Features
                </h1>
            </div>
        </section>
        
        <!-- Scroll Snap Carousel -->
        <section class="mb-12">
            <h2 class="text-3xl font-bold mb-6">Scroll Snap Gallery</h2>
            <div class="snap-x snap-mandatory overflow-x-auto flex gap-6 pb-4">
                <div class="snap-center flex-shrink-0 w-80 h-64 bg-gradient-to-br from-blue-500 to-purple-600 rounded-lg shadow-xl"></div>
                <div class="snap-center flex-shrink-0 w-80 h-64 bg-gradient-to-br from-green-500 to-teal-600 rounded-lg shadow-xl"></div>
                <div class="snap-center flex-shrink-0 w-80 h-64 bg-gradient-to-br from-red-500 to-pink-600 rounded-lg shadow-xl"></div>
                <div class="snap-center flex-shrink-0 w-80 h-64 bg-gradient-to-br from-yellow-500 to-orange-600 rounded-lg shadow-xl"></div>
            </div>
        </section>
        
        <!-- Multi-Column Text -->
        <section class="mb-12">
            <h2 class="text-3xl font-bold mb-6">Multi-Column Layout</h2>
            <article class="columns-3 gap-8 bg-white p-8 rounded-lg shadow text-justify">
                <p class="mb-4">
                    This text automatically flows across multiple columns, 
                    creating a newspaper-style layout. Perfect for long-form content.
                </p>
                <p class="mb-4">
                    The columns adjust automatically based on screen size and content,
                    providing an optimal reading experience.
                </p>
                <p>
                    You can control column count, width, and gaps using Tailwind utilities.
                </p>
            </article>
        </section>
        
        <!-- Form with Accent Colors -->
        <section class="bg-white p-8 rounded-lg shadow max-w-2xl">
            <h2 class="text-2xl font-bold mb-6">Styled Form Controls</h2>
            <form class="space-y-4">
                <div>
                    <label class="flex items-center gap-2">
                        <input type="checkbox" class="accent-blue-600 w-5 h-5">
                        <span>Blue checkbox</span>
                    </label>
                </div>
                <div>
                    <label class="flex items-center gap-2">
                        <input type="radio" name="color" class="accent-green-500 w-5 h-5">
                        <span>Green radio</span>
                    </label>
                </div>
                <div>
                    <input 
                        type="text" 
                        placeholder="Custom caret color" 
                        class="border border-gray-300 rounded-lg px-4 py-2 w-full caret-purple-600 focus:outline-none focus:ring-2 focus:ring-purple-500"
                    >
                </div>
                <div>
                    <input 
                        type="range" 
                        class="w-full accent-pink-500"
                    >
                </div>
            </form>
        </section>
        
    </div>

</body>
</html>
```

---

## ✨ Pro Tips

1. **Container**: Use `container mx-auto` for centered, responsive layouts
2. **Blend Modes**: Great for image overlays and creative effects
3. **Scroll Snap**: Perfect for carousels and full-page sections
4. **Arbitrary Values**: Use `[]` when you need exact custom values
5. **Will Change**: Only use for animations that actually need optimization
6. **Important**: Use `!` sparingly - semantic order is better
7. **Columns**: Great for articles and long-form content
8. **Accent Color**: Style form controls to match your brand

---

## 🎉 You've Mastered Everything!

Congratulations! You now have **100% complete** knowledge of Tailwind CSS, including:
- ✅ All core utilities
- ✅ Advanced layout systems
- ✅ Complete component library
- ✅ Animations, transforms & effects
- ✅ Accessibility features
- ✅ **Advanced utilities & special features**

You're ready to build anything with Tailwind CSS! 🚀

[Back to Tutorial Home](README.md) | [Practice Projects](practice-projects.md)

