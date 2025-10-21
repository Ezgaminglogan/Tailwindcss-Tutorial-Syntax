# 06 - Navigation Patterns

## 🧭 Basic Navbar

```html
<nav class="bg-white shadow-lg">
  <div class="max-w-6xl mx-auto px-6 py-4 flex justify-between items-center">
    <div class="text-xl font-bold">Logo</div>
    <ul class="flex gap-6">
      <li><a href="#" class="hover:text-blue-600">Home</a></li>
      <li><a href="#" class="hover:text-blue-600">About</a></li>
      <li><a href="#" class="hover:text-blue-600">Contact</a></li>
    </ul>
  </div>
</nav>
```

## 🎨 Navbar with Button

```html
<nav class="bg-gray-900 text-white">
  <div class="max-w-6xl mx-auto px-6 py-4 flex justify-between items-center">
    <div class="text-2xl font-bold">MyApp</div>
    <ul class="flex gap-8">
      <li><a href="#" class="hover:text-blue-400">Home</a></li>
      <li><a href="#" class="hover:text-blue-400">Features</a></li>
      <li><a href="#" class="hover:text-blue-400">Pricing</a></li>
    </ul>
    <button class="bg-blue-600 px-6 py-2 rounded-lg hover:bg-blue-700">
      Get Started
    </button>
  </div>
</nav>
```

## 📱 Sidebar Navigation

```html
<aside class="w-64 bg-gray-800 text-white h-screen">
  <div class="p-6">
    <h1 class="text-2xl font-bold">Dashboard</h1>
  </div>
  <nav class="px-4">
    <a href="#" class="flex items-center gap-3 px-4 py-3 rounded bg-gray-700 mb-2">
      <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"></path>
      </svg>
      Dashboard
    </a>
    <a href="#" class="flex items-center gap-3 px-4 py-3 rounded hover:bg-gray-700 mb-2">
      Users
    </a>
    <a href="#" class="flex items-center gap-3 px-4 py-3 rounded hover:bg-gray-700">
      Settings
    </a>
  </nav>
</aside>
```

## 🔗 Next Steps

Continue to [07 - Responsive Design](07-responsive.md)!

