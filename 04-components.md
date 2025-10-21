# 04 - Buttons & Cards

## 🔘 Buttons

### Basic Button

```html
<button class="bg-blue-500 text-white px-6 py-2 rounded">
  Click Me
</button>
```

---

## 🎨 Button Variations

### Primary Button

```html
<button class="bg-blue-600 text-white px-6 py-3 rounded-lg font-semibold hover:bg-blue-700 transition-colors">
  Primary Button
</button>
```

### Secondary Button

```html
<button class="bg-gray-600 text-white px-6 py-3 rounded-lg font-semibold hover:bg-gray-700 transition-colors">
  Secondary Button
</button>
```

### Success Button

```html
<button class="bg-green-600 text-white px-6 py-3 rounded-lg font-semibold hover:bg-green-700 transition-colors">
  Success Button
</button>
```

### Danger Button

```html
<button class="bg-red-600 text-white px-6 py-3 rounded-lg font-semibold hover:bg-red-700 transition-colors">
  Delete
</button>
```

### Warning Button

```html
<button class="bg-yellow-500 text-white px-6 py-3 rounded-lg font-semibold hover:bg-yellow-600 transition-colors">
  Warning
</button>
```

---

## 🎯 Button Styles

### Outline Button

```html
<button class="border-2 border-blue-600 text-blue-600 px-6 py-3 rounded-lg font-semibold hover:bg-blue-600 hover:text-white transition-colors">
  Outline Button
</button>
```

### Ghost Button

```html
<button class="text-blue-600 px-6 py-3 rounded-lg font-semibold hover:bg-blue-100 transition-colors">
  Ghost Button
</button>
```

### Rounded/Pill Button

```html
<button class="bg-purple-600 text-white px-8 py-3 rounded-full font-semibold hover:bg-purple-700">
  Pill Button
</button>
```

---

## 📏 Button Sizes

```html
<!-- Small -->
<button class="bg-blue-600 text-white px-3 py-1 rounded text-sm">
  Small
</button>

<!-- Medium (Default) -->
<button class="bg-blue-600 text-white px-6 py-2 rounded">
  Medium
</button>

<!-- Large -->
<button class="bg-blue-600 text-white px-8 py-4 rounded text-lg">
  Large
</button>

<!-- Full Width -->
<button class="bg-blue-600 text-white px-6 py-3 rounded w-full">
  Full Width Button
</button>
```

---

## 🚫 Button States

### Disabled Button

```html
<button class="bg-gray-400 text-white px-6 py-3 rounded cursor-not-allowed" disabled>
  Disabled
</button>
```

### Loading Button

```html
<button class="bg-blue-600 text-white px-6 py-3 rounded flex items-center gap-2">
  <svg class="animate-spin h-5 w-5" fill="none" viewBox="0 0 24 24">
    <circle class="opacity-25" cx="12" cy="12" r="10" stroke="currentColor" stroke-width="4"></circle>
    <path class="opacity-75" fill="currentColor" d="M4 12a8 8 0 018-8V0C5.373 0 0 5.373 0 12h4zm2 5.291A7.962 7.962 0 014 12H0c0 3.042 1.135 5.824 3 7.938l3-2.647z"></path>
  </svg>
  Loading...
</button>
```

---

## 🃏 Cards

### Basic Card

```html
<div class="bg-white rounded-lg shadow-lg p-6">
  <h2 class="text-xl font-bold mb-2">Card Title</h2>
  <p class="text-gray-600">This is a basic card component.</p>
</div>
```

---

## 🎨 Card Variations

### Card with Image

```html
<div class="bg-white rounded-lg shadow-lg overflow-hidden max-w-sm">
  <!-- Image -->
  <div class="h-48 bg-gradient-to-r from-blue-500 to-purple-600"></div>
  
  <!-- Content -->
  <div class="p-6">
    <h2 class="text-xl font-bold mb-2">Beautiful Card</h2>
    <p class="text-gray-600 mb-4">This card includes an image at the top.</p>
    <button class="bg-blue-600 text-white px-4 py-2 rounded hover:bg-blue-700">
      Read More
    </button>
  </div>
</div>
```

### Card with Border

```html
<div class="bg-white border-2 border-gray-200 rounded-lg p-6 hover:border-blue-500 transition-colors">
  <h2 class="text-xl font-bold mb-2">Bordered Card</h2>
  <p class="text-gray-600">This card has a border that changes on hover.</p>
</div>
```

### Card with Shadow Hover Effect

```html
<div class="bg-white rounded-lg shadow-md hover:shadow-2xl transition-shadow p-6">
  <h2 class="text-xl font-bold mb-2">Hover Me!</h2>
  <p class="text-gray-600">Shadow increases on hover.</p>
</div>
```

---

## 📊 Card Layouts

### Profile Card

```html
<div class="bg-white rounded-lg shadow-lg p-6 max-w-sm">
  <!-- Avatar -->
  <div class="flex justify-center mb-4">
    <div class="w-24 h-24 bg-gradient-to-br from-blue-400 to-purple-600 rounded-full"></div>
  </div>
  
  <!-- Info -->
  <h2 class="text-2xl font-bold text-center mb-1">John Doe</h2>
  <p class="text-gray-600 text-center mb-4">Web Developer</p>
  
  <!-- Stats -->
  <div class="flex justify-around border-t border-gray-200 pt-4">
    <div class="text-center">
      <p class="text-2xl font-bold text-blue-600">1.2K</p>
      <p class="text-gray-600 text-sm">Followers</p>
    </div>
    <div class="text-center">
      <p class="text-2xl font-bold text-purple-600">847</p>
      <p class="text-gray-600 text-sm">Following</p>
    </div>
  </div>
  
  <!-- Button -->
  <button class="w-full bg-blue-600 text-white py-3 rounded-lg font-semibold hover:bg-blue-700 mt-4">
    Follow
  </button>
</div>
```

---

### Product Card

```html
<div class="bg-white rounded-lg shadow-lg overflow-hidden max-w-sm">
  <!-- Product Image -->
  <div class="h-64 bg-gradient-to-br from-orange-400 to-pink-600"></div>
  
  <!-- Content -->
  <div class="p-6">
    <div class="flex justify-between items-start mb-2">
      <h3 class="text-xl font-bold">Product Name</h3>
      <span class="bg-green-100 text-green-800 px-2 py-1 rounded text-sm font-semibold">New</span>
    </div>
    
    <p class="text-gray-600 mb-4">Beautiful product description goes here.</p>
    
    <div class="flex items-center justify-between">
      <span class="text-3xl font-bold text-blue-600">$49.99</span>
      <button class="bg-blue-600 text-white px-6 py-2 rounded-lg hover:bg-blue-700">
        Add to Cart
      </button>
    </div>
  </div>
</div>
```

---

### Stats Card

```html
<div class="bg-white rounded-lg shadow-lg p-6">
  <div class="flex items-center justify-between">
    <div>
      <p class="text-gray-600 text-sm font-medium">Total Users</p>
      <p class="text-3xl font-bold text-gray-900 mt-1">12,543</p>
      <p class="text-green-600 text-sm mt-2">↑ 12% from last month</p>
    </div>
    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center">
      <svg class="w-8 h-8 text-blue-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4.354a4 4 0 110 5.292M15 21H3v-1a6 6 0 0112 0v1zm0 0h6v-1a6 6 0 00-9-5.197M13 7a4 4 0 11-8 0 4 4 0 018 0z"></path>
      </svg>
    </div>
  </div>
</div>
```

---

## 🎯 Button Groups

```html
<div class="flex gap-2">
  <button class="bg-blue-600 text-white px-4 py-2 rounded-lg">Option 1</button>
  <button class="bg-gray-200 text-gray-700 px-4 py-2 rounded-lg">Option 2</button>
  <button class="bg-gray-200 text-gray-700 px-4 py-2 rounded-lg">Option 3</button>
</div>
```

### Connected Button Group

```html
<div class="inline-flex rounded-lg shadow-sm">
  <button class="bg-blue-600 text-white px-4 py-2 rounded-l-lg border-r border-blue-700">
    Left
  </button>
  <button class="bg-blue-600 text-white px-4 py-2 border-r border-blue-700">
    Middle
  </button>
  <button class="bg-blue-600 text-white px-4 py-2 rounded-r-lg">
    Right
  </button>
</div>
```

---

## 🎨 Icon Buttons

```html
<!-- Square Icon Button -->
<button class="bg-blue-600 text-white w-10 h-10 rounded-lg flex items-center justify-center hover:bg-blue-700">
  <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4v16m8-8H4"></path>
  </svg>
</button>

<!-- Round Icon Button -->
<button class="bg-purple-600 text-white w-12 h-12 rounded-full flex items-center justify-center hover:bg-purple-700">
  <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
  </svg>
</button>

<!-- Button with Icon and Text -->
<button class="bg-green-600 text-white px-4 py-2 rounded-lg flex items-center gap-2 hover:bg-green-700">
  <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4v16m8-8H4"></path>
  </svg>
  Add New
</button>
```

---

## 📦 Complete Example

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Buttons & Cards</title>
    <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
</head>
<body class="bg-gray-100 p-8">
    
    <div class="max-w-6xl mx-auto">
        <h1 class="text-4xl font-bold mb-8">Component Gallery</h1>
        
        <!-- Buttons Section -->
        <section class="mb-12">
            <h2 class="text-2xl font-bold mb-4">Buttons</h2>
            <div class="flex flex-wrap gap-4">
                <button class="bg-blue-600 text-white px-6 py-3 rounded-lg hover:bg-blue-700">Primary</button>
                <button class="bg-green-600 text-white px-6 py-3 rounded-lg hover:bg-green-700">Success</button>
                <button class="bg-red-600 text-white px-6 py-3 rounded-lg hover:bg-red-700">Danger</button>
                <button class="border-2 border-blue-600 text-blue-600 px-6 py-3 rounded-lg hover:bg-blue-600 hover:text-white">Outline</button>
            </div>
        </section>
        
        <!-- Cards Section -->
        <section>
            <h2 class="text-2xl font-bold mb-4">Cards</h2>
            <div class="grid grid-cols-3 gap-6">
                <!-- Card 1 -->
                <div class="bg-white rounded-lg shadow-lg p-6">
                    <h3 class="text-xl font-bold mb-2">Card Title</h3>
                    <p class="text-gray-600 mb-4">Some quick example text to build on the card.</p>
                    <button class="bg-blue-600 text-white px-4 py-2 rounded">Learn More</button>
                </div>
                
                <!-- Card 2 -->
                <div class="bg-white rounded-lg shadow-lg p-6">
                    <h3 class="text-xl font-bold mb-2">Another Card</h3>
                    <p class="text-gray-600 mb-4">Different content in this card component.</p>
                    <button class="bg-purple-600 text-white px-4 py-2 rounded">Explore</button>
                </div>
                
                <!-- Card 3 -->
                <div class="bg-white rounded-lg shadow-lg p-6">
                    <h3 class="text-xl font-bold mb-2">Third Card</h3>
                    <p class="text-gray-600 mb-4">More example content for demonstration.</p>
                    <button class="bg-green-600 text-white px-4 py-2 rounded">View</button>
                </div>
            </div>
        </section>
    </div>

</body>
</html>
```

---

## ✅ Practice Exercise

Create a pricing card with:
- Plan name (e.g., "Pro Plan")
- Price ($29/month)
- List of features
- "Choose Plan" button
- Hover effect that lifts the card

---

## 🔗 Next Steps

Continue to [05 - CRUD Examples](05-crud-examples.md) to build complete CRUD interfaces!

