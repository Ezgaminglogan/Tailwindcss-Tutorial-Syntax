# 07 - Responsive Design

## 📱 Breakpoints

Tailwind uses these breakpoints:
- `sm:` - 640px and up
- `md:` - 768px and up
- `lg:` - 1024px and up
- `xl:` - 1280px and up
- `2xl:` - 1536px and up

## 🎯 Mobile-First Approach

```html
<!-- Stack on mobile, row on desktop -->
<div class="flex flex-col md:flex-row gap-4">
  <div class="bg-blue-500 p-4">Item 1</div>
  <div class="bg-green-500 p-4">Item 2</div>
</div>

<!-- 1 column mobile, 3 columns desktop -->
<div class="grid grid-cols-1 md:grid-cols-3 gap-4">
  <div>Card 1</div>
  <div>Card 2</div>
  <div>Card 3</div>
</div>

<!-- Hide on mobile, show on desktop -->
<div class="hidden md:block">
  Desktop only content
</div>

<!-- Show on mobile, hide on desktop -->
<div class="block md:hidden">
  Mobile only content
</div>
```

## 📦 Responsive Text

```html
<h1 class="text-2xl md:text-4xl lg:text-6xl font-bold">
  Responsive Heading
</h1>

<p class="text-sm md:text-base lg:text-lg">
  Responsive paragraph text
</p>
```

## ✅ Practice

Create a card grid that shows:
- 1 column on mobile
- 2 columns on tablet
- 3 columns on desktop

## 🔗 Next: [Common Patterns](08-patterns.md)

