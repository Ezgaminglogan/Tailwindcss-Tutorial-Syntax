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

<!-- Responsive Grid -->
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-4">
  <div>Responsive item</div>
  <div>Responsive item</div>
  <div>Responsive item</div>
  <div>Responsive item</div>
</div>
```

---

## 📐 Advanced Grid Features

### Column & Row Spanning

```html
<!-- Column Span -->
<div class="grid grid-cols-3 gap-4">
  <div class="col-span-2 bg-blue-500 p-4">Spans 2 columns</div>
  <div class="bg-green-500 p-4">1 column</div>
  <div class="bg-red-500 p-4">1 column</div>
  <div class="col-span-2 bg-purple-500 p-4">Spans 2 columns</div>
</div>

<!-- Column Span Full -->
<div class="grid grid-cols-4 gap-4">
  <div class="col-span-4 bg-blue-500 p-4">Full width</div>
  <div class="col-span-2 bg-green-500 p-4">Half width</div>
  <div class="col-span-2 bg-red-500 p-4">Half width</div>
  <div class="bg-purple-500 p-4">Quarter</div>
  <div class="col-span-3 bg-yellow-500 p-4">Three quarters</div>
</div>

<!-- Row Span -->
<div class="grid grid-cols-3 grid-rows-3 gap-4">
  <div class="row-span-2 bg-blue-500 p-4">Spans 2 rows</div>
  <div class="bg-green-500 p-4">Normal</div>
  <div class="row-span-3 bg-red-500 p-4">Spans 3 rows</div>
  <div class="bg-purple-500 p-4">Normal</div>
  <div class="col-span-2 bg-yellow-500 p-4">Spans 2 cols</div>
</div>
```

**Visual Example:**
```
┌──────────────┬──────┐
│  col-span-2  │  1   │
├──────┬───────┴──────┤
│  1   │  col-span-2  │
└──────┴──────────────┘
```

### Grid Column/Row Start & End

```html
<!-- Precise Grid Placement -->
<div class="grid grid-cols-6 gap-4">
  <div class="col-start-1 col-end-3 bg-blue-500 p-4">
    Column 1 to 3
  </div>
  <div class="col-start-4 col-end-7 bg-green-500 p-4">
    Column 4 to 7
  </div>
</div>

<!-- Row Placement -->
<div class="grid grid-rows-3 gap-4">
  <div class="row-start-2 row-end-4 bg-purple-500 p-4">
    Rows 2 to 4
  </div>
</div>
```

### Grid Auto Flow

```html
<!-- Flow Row (default) -->
<div class="grid grid-cols-3 grid-flow-row gap-4">
  <div>1</div>
  <div>2</div>
  <div>3</div>
  <div>4</div>
</div>

<!-- Flow Column -->
<div class="grid grid-rows-3 grid-flow-col gap-4">
  <div>1</div>
  <div>2</div>
  <div>3</div>
  <div>4</div>
</div>

<!-- Dense (fills gaps) -->
<div class="grid grid-cols-3 grid-flow-dense gap-4">
  <div class="col-span-2">Wide item</div>
  <div>Item</div>
  <div>Item</div>
</div>
```

### Grid Template Columns/Rows

```html
<!-- Auto-fit columns -->
<div class="grid grid-cols-[repeat(auto-fit,minmax(200px,1fr))] gap-4">
  <div>Auto-sized item</div>
  <div>Auto-sized item</div>
  <div>Auto-sized item</div>
</div>

<!-- Custom Grid Template -->
<div class="grid grid-cols-[200px_1fr_100px] gap-4">
  <div>200px</div>
  <div>Flexible</div>
  <div>100px</div>
</div>
```

---

## 🔄 Space Between

Use `space-x` and `space-y` to add spacing between child elements:

```html
<!-- Horizontal Space Between -->
<div class="flex space-x-4">
  <div class="bg-blue-500 p-4">Item 1</div>
  <div class="bg-blue-500 p-4">Item 2</div>
  <div class="bg-blue-500 p-4">Item 3</div>
</div>

<!-- Vertical Space Between -->
<div class="flex flex-col space-y-6">
  <div class="bg-green-500 p-4">Item 1</div>
  <div class="bg-green-500 p-4">Item 2</div>
  <div class="bg-green-500 p-4">Item 3</div>
</div>

<!-- Different Spacing Sizes -->
<div class="flex space-x-2">Small spacing (8px)</div>
<div class="flex space-x-4">Medium spacing (16px)</div>
<div class="flex space-x-8">Large spacing (32px)</div>

<!-- Reverse Space (useful with flex-reverse) -->
<div class="flex flex-row-reverse space-x-4 space-x-reverse">
  <div>Item 1</div>
  <div>Item 2</div>
  <div>Item 3</div>
</div>
```

---

## ➗ Divide

Add borders between child elements:

```html
<!-- Vertical Divider -->
<div class="flex divide-x divide-gray-300">
  <div class="px-4">Section 1</div>
  <div class="px-4">Section 2</div>
  <div class="px-4">Section 3</div>
</div>

<!-- Horizontal Divider -->
<div class="divide-y divide-gray-300">
  <div class="py-4">Row 1</div>
  <div class="py-4">Row 2</div>
  <div class="py-4">Row 3</div>
</div>

<!-- Divider Styles -->
<div class="divide-y divide-blue-500 divide-dashed">
  <div class="py-2">Dashed divider</div>
  <div class="py-2">Dashed divider</div>
</div>

<!-- Divider Width -->
<div class="divide-y-2 divide-gray-400">
  <div class="py-2">Thick divider</div>
  <div class="py-2">Thick divider</div>
</div>

<!-- Common Use: List with Dividers -->
<ul class="divide-y divide-gray-200 bg-white rounded-lg shadow">
  <li class="px-6 py-4">List item 1</li>
  <li class="px-6 py-4">List item 2</li>
  <li class="px-6 py-4">List item 3</li>
</ul>
```

---

## 📏 Aspect Ratio

Maintain consistent aspect ratios for elements:

```html
<!-- Square (1:1) -->
<div class="aspect-square bg-blue-500">
  Square box
</div>

<!-- Video (16:9) -->
<div class="aspect-video bg-gray-200">
  <iframe src="video.mp4" class="w-full h-full"></iframe>
</div>

<!-- Custom Aspect Ratios -->
<div class="aspect-[4/3] bg-green-500">4:3 ratio</div>
<div class="aspect-[21/9] bg-purple-500">21:9 ratio</div>

<!-- Responsive Images -->
<div class="aspect-square overflow-hidden rounded-lg">
  <img src="image.jpg" class="w-full h-full object-cover">
</div>
```

---

## 🖼️ Object Fit & Position

Control how images/videos fit their containers:

```html
<!-- Object Fit -->
<img src="image.jpg" class="w-full h-64 object-cover"> <!-- Covers container -->
<img src="image.jpg" class="w-full h-64 object-contain"> <!-- Fits inside -->
<img src="image.jpg" class="w-full h-64 object-fill"> <!-- Stretches -->
<img src="image.jpg" class="w-full h-64 object-none"> <!-- Original size -->
<img src="image.jpg" class="w-full h-64 object-scale-down"> <!-- Scale down if needed -->

<!-- Object Position -->
<img src="image.jpg" class="object-cover object-center">
<img src="image.jpg" class="object-cover object-top">
<img src="image.jpg" class="object-cover object-bottom">
<img src="image.jpg" class="object-cover object-left">
<img src="image.jpg" class="object-cover object-right">

<!-- Combined Example: Avatar -->
<div class="w-24 h-24 rounded-full overflow-hidden">
  <img src="avatar.jpg" class="w-full h-full object-cover object-center">
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

