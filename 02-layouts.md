# 02 - Layouts & Flexbox

## 🎯 Flexbox Basics

Flexbox is the most common layout method in Tailwind. It arranges items in rows or columns.

### Creating a Flex Container

```html
<div class="flex">
  <div>Item 1</div>
  <div>Item 2</div>
  <div>Item 3</div>
</div>
```

---

## 📐 Flex Direction

```html
<!-- Row (default - horizontal) -->
<div class="flex flex-row">
  <div>1</div>
  <div>2</div>
  <div>3</div>
</div>

<!-- Column (vertical) -->
<div class="flex flex-col">
  <div>1</div>
  <div>2</div>
  <div>3</div>
</div>

<!-- Reverse -->
<div class="flex flex-row-reverse">
  <div>1</div>
  <div>2</div>
  <div>3</div>
</div>
```

---

## ↔️ Justify Content (Horizontal Alignment)

```html
<!-- Start (default) -->
<div class="flex justify-start">
  <div>Item 1</div>
  <div>Item 2</div>
</div>

<!-- End -->
<div class="flex justify-end">
  <div>Item 1</div>
  <div>Item 2</div>
</div>

<!-- Center -->
<div class="flex justify-center">
  <div>Item 1</div>
  <div>Item 2</div>
</div>

<!-- Space Between -->
<div class="flex justify-between">
  <div>Item 1</div>
  <div>Item 2</div>
  <div>Item 3</div>
</div>

<!-- Space Around -->
<div class="flex justify-around">
  <div>Item 1</div>
  <div>Item 2</div>
</div>

<!-- Space Evenly -->
<div class="flex justify-evenly">
  <div>Item 1</div>
  <div>Item 2</div>
</div>
```

---

## ↕️ Align Items (Vertical Alignment)

```html
<!-- Start (top) -->
<div class="flex items-start h-32">
  <div>Item 1</div>
  <div>Item 2</div>
</div>

<!-- Center (middle) -->
<div class="flex items-center h-32">
  <div>Item 1</div>
  <div>Item 2</div>
</div>

<!-- End (bottom) -->
<div class="flex items-end h-32">
  <div>Item 1</div>
  <div>Item 2</div>
</div>

<!-- Stretch (fill height) -->
<div class="flex items-stretch h-32">
  <div>Item 1</div>
  <div>Item 2</div>
</div>
```

---

## 🔄 Gap (Spacing Between Items)

Instead of margins, use `gap` for spacing:

```html
<!-- Horizontal and Vertical Gap -->
<div class="flex gap-4">
  <div>Item 1</div>
  <div>Item 2</div>
  <div>Item 3</div>
</div>

<!-- Horizontal Gap Only -->
<div class="flex gap-x-6">
  <div>Item 1</div>
  <div>Item 2</div>
</div>

<!-- Vertical Gap Only -->
<div class="flex flex-col gap-y-8">
  <div>Item 1</div>
  <div>Item 2</div>
</div>

<!-- Different Gap Sizes -->
<div class="flex gap-2">Small gap (8px)</div>
<div class="flex gap-4">Medium gap (16px)</div>
<div class="flex gap-8">Large gap (32px)</div>
```

---

## 📊 Flex Grow & Shrink

```html
<!-- Flex 1 - Takes remaining space -->
<div class="flex">
  <div class="flex-1 bg-blue-500">Takes remaining space</div>
  <div class="bg-red-500">Fixed width content</div>
</div>

<!-- Multiple flex items -->
<div class="flex">
  <div class="flex-1 bg-blue-500">Equal space 1</div>
  <div class="flex-1 bg-green-500">Equal space 2</div>
  <div class="flex-1 bg-red-500">Equal space 3</div>
</div>

<!-- Flex None - Don't grow or shrink -->
<div class="flex">
  <div class="flex-none w-32 bg-blue-500">Fixed 32</div>
  <div class="flex-1 bg-green-500">Takes rest</div>
</div>
```

---

## 🎨 Common Layout Patterns

### 1. Navbar Layout

```html
<nav class="flex justify-between items-center bg-white shadow-lg px-6 py-4">
  <div class="text-xl font-bold">Logo</div>
  <ul class="flex gap-6">
    <li>Home</li>
    <li>About</li>
    <li>Contact</li>
  </ul>
</nav>
```

**Visual:**
```
┌────────────────────────────────────────┐
│ Logo              Home About Contact   │
└────────────────────────────────────────┘
```

---

### 2. Centered Container

```html
<div class="flex justify-center items-center min-h-screen bg-gray-100">
  <div class="bg-white p-8 rounded-lg shadow-lg">
    <h1 class="text-2xl font-bold">Centered Content</h1>
    <p>This is perfectly centered!</p>
  </div>
</div>
```

**Visual:**
```
┌────────────────────────────┐
│                            │
│     ┌─────────────┐        │
│     │   Content   │        │
│     └─────────────┘        │
│                            │
└────────────────────────────┘
```

---

### 3. Card Grid

```html
<div class="flex gap-4">
  <div class="flex-1 bg-white p-6 rounded-lg shadow">Card 1</div>
  <div class="flex-1 bg-white p-6 rounded-lg shadow">Card 2</div>
  <div class="flex-1 bg-white p-6 rounded-lg shadow">Card 3</div>
</div>
```

**Visual:**
```
┌──────┐  ┌──────┐  ┌──────┐
│Card 1│  │Card 2│  │Card 3│
└──────┘  └──────┘  └──────┘
```

---

### 4. Sidebar Layout

```html
<div class="flex h-screen">
  <!-- Sidebar -->
  <aside class="w-64 bg-gray-800 text-white p-6">
    <h2 class="text-xl font-bold mb-4">Sidebar</h2>
    <ul class="flex flex-col gap-2">
      <li>Dashboard</li>
      <li>Users</li>
      <li>Settings</li>
    </ul>
  </aside>
  
  <!-- Main Content -->
  <main class="flex-1 bg-gray-100 p-8">
    <h1 class="text-3xl font-bold">Main Content</h1>
    <p>Content goes here...</p>
  </main>
</div>
```

**Visual:**
```
┌────────┬─────────────────────┐
│Sidebar │   Main Content      │
│        │                     │
│Dashboard│                    │
│Users   │                     │
│Settings│                     │
└────────┴─────────────────────┘
```

---

### 5. Header + Content + Footer

```html
<div class="flex flex-col min-h-screen">
  <!-- Header -->
  <header class="bg-blue-600 text-white p-6">
    <h1 class="text-2xl font-bold">Header</h1>
  </header>
  
  <!-- Main Content (grows to fill space) -->
  <main class="flex-1 bg-gray-100 p-8">
    <p>Main content that takes remaining space</p>
  </main>
  
  <!-- Footer -->
  <footer class="bg-gray-800 text-white p-6 text-center">
    <p>&copy; 2025 My Website</p>
  </footer>
</div>
```

**Visual:**
```
┌─────────────────────┐
│      Header         │
├─────────────────────┤
│                     │
│   Main Content      │
│                     │
│                     │
├─────────────────────┤
│      Footer         │
└─────────────────────┘
```

---

## 🏗️ Grid Layout

For more complex grids, use CSS Grid:

```html
<!-- 3 Column Grid -->
<div class="grid grid-cols-3 gap-4">
  <div class="bg-blue-500 p-4">1</div>
  <div class="bg-blue-500 p-4">2</div>
  <div class="bg-blue-500 p-4">3</div>
  <div class="bg-blue-500 p-4">4</div>
  <div class="bg-blue-500 p-4">5</div>
  <div class="bg-blue-500 p-4">6</div>
</div>

<!-- 2 Column Grid -->
<div class="grid grid-cols-2 gap-6">
  <div>Column 1</div>
  <div>Column 2</div>
</div>

<!-- 4 Column Grid -->
<div class="grid grid-cols-4 gap-4">
  <div>1</div>
  <div>2</div>
  <div>3</div>
  <div>4</div>
</div>
```

---

## 📦 Complete Layout Example

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Layout Example</title>
    <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
</head>
<body>
    
    <!-- Full Page Layout -->
    <div class="flex flex-col min-h-screen">
        
        <!-- Navbar -->
        <nav class="flex justify-between items-center bg-white shadow-lg px-6 py-4">
            <div class="text-xl font-bold text-blue-600">MyApp</div>
            <ul class="flex gap-6">
                <li class="cursor-pointer hover:text-blue-600">Home</li>
                <li class="cursor-pointer hover:text-blue-600">About</li>
                <li class="cursor-pointer hover:text-blue-600">Contact</li>
            </ul>
        </nav>
        
        <!-- Main Content Area -->
        <main class="flex-1 bg-gray-100 p-8">
            <div class="max-w-6xl mx-auto">
                <h1 class="text-4xl font-bold mb-8">Welcome!</h1>
                
                <!-- Card Grid -->
                <div class="grid grid-cols-3 gap-6">
                    <div class="bg-white p-6 rounded-lg shadow-lg">
                        <h2 class="text-xl font-bold mb-2">Card 1</h2>
                        <p class="text-gray-600">Some content here</p>
                    </div>
                    <div class="bg-white p-6 rounded-lg shadow-lg">
                        <h2 class="text-xl font-bold mb-2">Card 2</h2>
                        <p class="text-gray-600">Some content here</p>
                    </div>
                    <div class="bg-white p-6 rounded-lg shadow-lg">
                        <h2 class="text-xl font-bold mb-2">Card 3</h2>
                        <p class="text-gray-600">Some content here</p>
                    </div>
                </div>
            </div>
        </main>
        
        <!-- Footer -->
        <footer class="bg-gray-800 text-white p-6 text-center">
            <p>&copy; 2025 MyApp. All rights reserved.</p>
        </footer>
        
    </div>

</body>
</html>
```

---

## ✅ Practice Exercise

Create a dashboard layout with:
1. Top navbar with logo (left) and menu items (right)
2. Sidebar on the left (fixed width 256px)
3. Main content area that takes remaining space
4. Footer at the bottom

---

## 🔗 Next Steps

Continue to [03 - Forms & Inputs](03-forms.md) to learn how to build beautiful forms!

