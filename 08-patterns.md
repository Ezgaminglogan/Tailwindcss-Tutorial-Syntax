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

## ✨ Pro Tips

1. Use `max-w-` classes to control content width
2. Use `mx-auto` to center containers
3. Use `gap-` instead of margins for spacing in flex/grid
4. Use `focus:` states for accessibility
5. Combine hover with `transition-` for smooth effects

## 🎉 You're Done!

Congratulations! You now know Tailwind CSS fundamentals. Keep practicing and building projects!

