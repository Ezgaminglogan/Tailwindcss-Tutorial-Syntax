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

## 🏷️ Badges

Small labels for status, counts, or categories:

```html
<!-- Basic Badges -->
<span class="bg-blue-100 text-blue-800 px-3 py-1 rounded-full text-sm font-semibold">
  New
</span>

<span class="bg-green-100 text-green-800 px-3 py-1 rounded-full text-sm font-semibold">
  Active
</span>

<span class="bg-red-100 text-red-800 px-3 py-1 rounded-full text-sm font-semibold">
  Urgent
</span>

<span class="bg-yellow-100 text-yellow-800 px-3 py-1 rounded-full text-sm font-semibold">
  Pending
</span>

<span class="bg-gray-100 text-gray-800 px-3 py-1 rounded-full text-sm font-semibold">
  Inactive
</span>

<!-- Badge with Icon -->
<span class="inline-flex items-center gap-1 bg-purple-100 text-purple-800 px-3 py-1 rounded-full text-sm font-semibold">
  <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 20 20">
    <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"></path>
  </svg>
  Premium
</span>

<!-- Badge with Dot -->
<span class="inline-flex items-center gap-2 bg-green-100 text-green-800 px-3 py-1 rounded-full text-sm font-semibold">
  <span class="w-2 h-2 bg-green-600 rounded-full"></span>
  Online
</span>

<!-- Counter Badge -->
<button class="relative bg-gray-200 p-3 rounded-lg">
  <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 17h5l-1.405-1.405A2.032 2.032 0 0118 14.158V11a6.002 6.002 0 00-4-5.659V5a2 2 0 10-4 0v.341C7.67 6.165 6 8.388 6 11v3.159c0 .538-.214 1.055-.595 1.436L4 17h5m6 0v1a3 3 0 11-6 0v-1m6 0H9"></path>
  </svg>
  <span class="absolute -top-1 -right-1 bg-red-500 text-white text-xs font-bold rounded-full w-5 h-5 flex items-center justify-center">
    3
  </span>
</button>

<!-- Removable Badge -->
<span class="inline-flex items-center gap-1 bg-blue-100 text-blue-800 px-3 py-1 rounded-full text-sm font-semibold">
  React
  <button class="hover:bg-blue-200 rounded-full p-0.5">
    <svg class="w-3 h-3" fill="currentColor" viewBox="0 0 20 20">
      <path d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z"></path>
    </svg>
  </button>
</span>
```

---

## ⚠️ Alerts

Notification messages for different contexts:

```html
<!-- Success Alert -->
<div class="bg-green-100 border border-green-400 text-green-700 px-4 py-3 rounded relative" role="alert">
  <strong class="font-bold">Success!</strong>
  <span class="block sm:inline"> Your changes have been saved.</span>
</div>

<!-- Error Alert -->
<div class="bg-red-100 border border-red-400 text-red-700 px-4 py-3 rounded relative">
  <strong class="font-bold">Error!</strong>
  <span class="block sm:inline"> Something went wrong. Please try again.</span>
</div>

<!-- Warning Alert -->
<div class="bg-yellow-100 border border-yellow-400 text-yellow-700 px-4 py-3 rounded relative">
  <strong class="font-bold">Warning!</strong>
  <span class="block sm:inline"> Your session will expire in 5 minutes.</span>
</div>

<!-- Info Alert -->
<div class="bg-blue-100 border border-blue-400 text-blue-700 px-4 py-3 rounded relative">
  <strong class="font-bold">Info:</strong>
  <span class="block sm:inline"> New features are available.</span>
</div>

<!-- Alert with Icon -->
<div class="bg-green-100 border-l-4 border-green-500 text-green-700 p-4 flex items-start gap-3">
  <svg class="w-6 h-6 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
    <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"></path>
  </svg>
  <div>
    <p class="font-bold">Payment successful!</p>
    <p class="text-sm">Your order has been confirmed.</p>
  </div>
</div>

<!-- Dismissible Alert -->
<div class="bg-blue-100 border border-blue-400 text-blue-700 px-4 py-3 rounded relative flex justify-between items-center">
  <span>This is a dismissible alert.</span>
  <button class="text-blue-700 hover:text-blue-900">
    <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
      <path fill-rule="evenodd" d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z" clip-rule="evenodd"></path>
    </svg>
  </button>
</div>
```

---

## 👤 Avatars

User profile images and placeholders:

```html
<!-- Basic Avatar -->
<img src="avatar.jpg" alt="User" class="w-12 h-12 rounded-full">

<!-- Avatar Sizes -->
<img src="avatar.jpg" class="w-8 h-8 rounded-full"> <!-- Small -->
<img src="avatar.jpg" class="w-12 h-12 rounded-full"> <!-- Medium -->
<img src="avatar.jpg" class="w-16 h-16 rounded-full"> <!-- Large -->
<img src="avatar.jpg" class="w-24 h-24 rounded-full"> <!-- XL -->

<!-- Avatar with Border -->
<img src="avatar.jpg" class="w-12 h-12 rounded-full border-2 border-white ring-2 ring-blue-500">

<!-- Avatar Placeholder (No Image) -->
<div class="w-12 h-12 rounded-full bg-gray-300 flex items-center justify-center text-gray-600 font-bold">
  JD
</div>

<!-- Avatar with Status Indicator -->
<div class="relative inline-block">
  <img src="avatar.jpg" class="w-12 h-12 rounded-full">
  <span class="absolute bottom-0 right-0 w-3 h-3 bg-green-500 border-2 border-white rounded-full"></span>
</div>

<!-- Avatar with Notification Badge -->
<div class="relative inline-block">
  <img src="avatar.jpg" class="w-12 h-12 rounded-full">
  <span class="absolute -top-1 -right-1 bg-red-500 text-white text-xs font-bold rounded-full w-5 h-5 flex items-center justify-center">
    5
  </span>
</div>

<!-- Avatar Group -->
<div class="flex -space-x-3">
  <img src="avatar1.jpg" class="w-10 h-10 rounded-full border-2 border-white">
  <img src="avatar2.jpg" class="w-10 h-10 rounded-full border-2 border-white">
  <img src="avatar3.jpg" class="w-10 h-10 rounded-full border-2 border-white">
  <div class="w-10 h-10 rounded-full bg-gray-300 border-2 border-white flex items-center justify-center text-xs font-bold">
    +5
  </div>
</div>

<!-- Square Avatar (for brand logos) -->
<img src="logo.jpg" class="w-12 h-12 rounded-lg">
```

---

## 📊 Progress Bars

Visual indicators for progress or completion:

```html
<!-- Basic Progress Bar -->
<div class="w-full bg-gray-200 rounded-full h-2">
  <div class="bg-blue-600 h-2 rounded-full" style="width: 60%"></div>
</div>

<!-- Progress Bar with Label -->
<div class="mb-2 flex justify-between items-center">
  <span class="text-sm font-medium text-gray-700">Progress</span>
  <span class="text-sm font-medium text-gray-700">75%</span>
</div>
<div class="w-full bg-gray-200 rounded-full h-2.5">
  <div class="bg-blue-600 h-2.5 rounded-full" style="width: 75%"></div>
</div>

<!-- Colored Progress Bars -->
<div class="w-full bg-gray-200 rounded-full h-2 mb-2">
  <div class="bg-green-600 h-2 rounded-full" style="width: 90%"></div>
</div>
<div class="w-full bg-gray-200 rounded-full h-2 mb-2">
  <div class="bg-yellow-500 h-2 rounded-full" style="width: 50%"></div>
</div>
<div class="w-full bg-gray-200 rounded-full h-2">
  <div class="bg-red-600 h-2 rounded-full" style="width: 25%"></div>
</div>

<!-- Striped Progress Bar -->
<div class="w-full bg-gray-200 rounded-full h-4 overflow-hidden">
  <div class="h-4 rounded-full bg-gradient-to-r from-blue-500 to-blue-600 animate-pulse" style="width: 60%"></div>
</div>

<!-- Multiple Progress Bars (Stacked) -->
<div class="w-full bg-gray-200 rounded-full h-4 flex overflow-hidden">
  <div class="bg-blue-600 h-4" style="width: 30%"></div>
  <div class="bg-green-600 h-4" style="width: 25%"></div>
  <div class="bg-yellow-500 h-4" style="width: 20%"></div>
  <div class="bg-red-600 h-4" style="width: 15%"></div>
</div>

<!-- Circular Progress (Using conic-gradient) -->
<div class="relative w-32 h-32">
  <svg class="w-full h-full" viewBox="0 0 100 100">
    <circle cx="50" cy="50" r="45" stroke="#e5e7eb" stroke-width="10" fill="none"></circle>
    <circle cx="50" cy="50" r="45" stroke="#3b82f6" stroke-width="10" fill="none" 
            stroke-dasharray="283" stroke-dashoffset="70" stroke-linecap="round" 
            transform="rotate(-90 50 50)"></circle>
  </svg>
  <div class="absolute inset-0 flex items-center justify-center text-xl font-bold">
    75%
  </div>
</div>
```

---

## ⏳ Spinners & Loaders

Loading indicators:

```html
<!-- Spinning Circle -->
<div class="animate-spin rounded-full h-8 w-8 border-b-2 border-blue-600"></div>

<!-- Spinning Border -->
<div class="animate-spin rounded-full h-12 w-12 border-4 border-gray-200 border-t-blue-600"></div>

<!-- Dotted Spinner -->
<div class="flex space-x-2">
  <div class="w-3 h-3 bg-blue-600 rounded-full animate-bounce"></div>
  <div class="w-3 h-3 bg-blue-600 rounded-full animate-bounce" style="animation-delay: 0.1s"></div>
  <div class="w-3 h-3 bg-blue-600 rounded-full animate-bounce" style="animation-delay: 0.2s"></div>
</div>

<!-- Pulsing Circle -->
<div class="relative">
  <div class="w-12 h-12 bg-blue-600 rounded-full animate-ping absolute"></div>
  <div class="w-12 h-12 bg-blue-600 rounded-full relative"></div>
</div>

<!-- Loading Button -->
<button class="bg-blue-600 text-white px-6 py-3 rounded-lg flex items-center gap-2" disabled>
  <svg class="animate-spin h-5 w-5" viewBox="0 0 24 24">
    <circle class="opacity-25" cx="12" cy="12" r="10" stroke="currentColor" stroke-width="4" fill="none"></circle>
    <path class="opacity-75" fill="currentColor" d="M4 12a8 8 0 018-8V0C5.373 0 0 5.373 0 12h4zm2 5.291A7.962 7.962 0 014 12H0c0 3.042 1.135 5.824 3 7.938l3-2.647z"></path>
  </svg>
  Loading...
</button>

<!-- Skeleton Loader -->
<div class="border border-gray-200 rounded-lg p-4 max-w-sm">
  <div class="animate-pulse flex space-x-4">
    <div class="rounded-full bg-gray-300 h-12 w-12"></div>
    <div class="flex-1 space-y-3 py-1">
      <div class="h-4 bg-gray-300 rounded w-3/4"></div>
      <div class="space-y-2">
        <div class="h-3 bg-gray-300 rounded"></div>
        <div class="h-3 bg-gray-300 rounded w-5/6"></div>
      </div>
    </div>
  </div>
</div>
```

---

## 🎭 Tooltips

Hover information displays:

```html
<!-- Basic Tooltip (CSS-only) -->
<div class="relative group inline-block">
  <button class="bg-blue-600 text-white px-4 py-2 rounded">
    Hover me
  </button>
  <div class="absolute bottom-full left-1/2 -translate-x-1/2 mb-2 hidden group-hover:block bg-gray-900 text-white text-xs rounded py-1 px-2 whitespace-nowrap">
    This is a tooltip
    <div class="absolute top-full left-1/2 -translate-x-1/2 border-4 border-transparent border-t-gray-900"></div>
  </div>
</div>

<!-- Tooltip Positions -->
<!-- Top -->
<div class="relative group inline-block">
  <button class="bg-blue-600 text-white px-4 py-2 rounded">Top</button>
  <span class="absolute bottom-full left-1/2 -translate-x-1/2 mb-2 hidden group-hover:block bg-gray-900 text-white text-xs rounded py-1 px-2">
    Top tooltip
  </span>
</div>

<!-- Bottom -->
<div class="relative group inline-block">
  <button class="bg-blue-600 text-white px-4 py-2 rounded">Bottom</button>
  <span class="absolute top-full left-1/2 -translate-x-1/2 mt-2 hidden group-hover:block bg-gray-900 text-white text-xs rounded py-1 px-2">
    Bottom tooltip
  </span>
</div>

<!-- Left -->
<div class="relative group inline-block">
  <button class="bg-blue-600 text-white px-4 py-2 rounded">Left</button>
  <span class="absolute right-full top-1/2 -translate-y-1/2 mr-2 hidden group-hover:block bg-gray-900 text-white text-xs rounded py-1 px-2">
    Left tooltip
  </span>
</div>

<!-- Right -->
<div class="relative group inline-block">
  <button class="bg-blue-600 text-white px-4 py-2 rounded">Right</button>
  <span class="absolute left-full top-1/2 -translate-y-1/2 ml-2 hidden group-hover:block bg-gray-900 text-white text-xs rounded py-1 px-2">
    Right tooltip
  </span>
</div>
```

---

## 📄 Empty States

Show when there's no content:

```html
<div class="text-center py-12 px-4">
  <svg class="mx-auto h-24 w-24 text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z"></path>
  </svg>
  <h3 class="mt-4 text-xl font-semibold text-gray-900">No documents found</h3>
  <p class="mt-2 text-gray-500">Get started by creating a new document.</p>
  <button class="mt-6 bg-blue-600 text-white px-6 py-3 rounded-lg hover:bg-blue-700">
    Create Document
  </button>
</div>
```

---

## ✅ Practice Exercise

Create a pricing card with:
- Plan name (e.g., "Pro Plan")
- Price ($29/month)
- List of features
- "Choose Plan" button
- Hover effect that lifts the card
- Add a "Popular" badge at the top-right corner

---

## 🔗 Next Steps

Continue to [05 - CRUD Examples](05-crud-examples.md) to build complete CRUD interfaces!

