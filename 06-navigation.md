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

---

## 📑 Tabs

Tab navigation for switching between views:

```html
<!-- Basic Tabs -->
<div class="border-b border-gray-200">
  <nav class="flex gap-4">
    <button class="border-b-2 border-blue-600 text-blue-600 px-4 py-2 font-semibold">
      Profile
    </button>
    <button class="border-b-2 border-transparent text-gray-600 px-4 py-2 font-semibold hover:text-gray-800">
      Settings
    </button>
    <button class="border-b-2 border-transparent text-gray-600 px-4 py-2 font-semibold hover:text-gray-800">
      Notifications
    </button>
  </nav>
</div>

<!-- Pills Style Tabs -->
<div class="flex gap-2 bg-gray-100 p-1 rounded-lg">
  <button class="bg-white text-blue-600 px-4 py-2 rounded-md font-semibold shadow-sm">
    Overview
  </button>
  <button class="text-gray-600 px-4 py-2 rounded-md font-semibold hover:text-gray-800">
    Analytics
  </button>
  <button class="text-gray-600 px-4 py-2 rounded-md font-semibold hover:text-gray-800">
    Reports
  </button>
</div>

<!-- Full-width Tabs -->
<div class="grid grid-cols-3 gap-2 bg-gray-100 p-2 rounded-lg">
  <button class="bg-white text-center px-4 py-2 rounded font-semibold shadow">
    Tab 1
  </button>
  <button class="text-center px-4 py-2 rounded font-semibold hover:bg-gray-200">
    Tab 2
  </button>
  <button class="text-center px-4 py-2 rounded font-semibold hover:bg-gray-200">
    Tab 3
  </button>
</div>

<!-- Tabs with Icons -->
<div class="flex gap-4 border-b border-gray-200">
  <button class="border-b-2 border-blue-600 text-blue-600 px-4 py-2 font-semibold flex items-center gap-2">
    <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z"></path>
    </svg>
    Profile
  </button>
  <button class="border-b-2 border-transparent text-gray-600 px-4 py-2 font-semibold hover:text-gray-800 flex items-center gap-2">
    <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10.325 4.317c.426-1.756 2.924-1.756 3.35 0a1.724 1.724 0 002.573 1.066c1.543-.94 3.31.826 2.37 2.37a1.724 1.724 0 001.065 2.572c1.756.426 1.756 2.924 0 3.35a1.724 1.724 0 00-1.066 2.573c.94 1.543-.826 3.31-2.37 2.37a1.724 1.724 0 00-2.572 1.065c-.426 1.756-2.924 1.756-3.35 0a1.724 1.724 0 00-2.573-1.066c-1.543.94-3.31-.826-2.37-2.37a1.724 1.724 0 00-1.065-2.572c-1.756-.426-1.756-2.924 0-3.35a1.724 1.724 0 001.066-2.573c-.94-1.543.826-3.31 2.37-2.37.996.608 2.296.07 2.572-1.065z"></path>
      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"></path>
    </svg>
    Settings
  </button>
</div>

<!-- Tab Content Example -->
<div class="bg-white rounded-lg shadow-lg">
  <!-- Tabs -->
  <div class="border-b border-gray-200 px-6">
    <nav class="flex gap-6">
      <button class="border-b-2 border-blue-600 text-blue-600 py-4 font-semibold">
        Details
      </button>
      <button class="border-b-2 border-transparent text-gray-600 py-4 font-semibold hover:text-gray-800">
        Reviews
      </button>
      <button class="border-b-2 border-transparent text-gray-600 py-4 font-semibold hover:text-gray-800">
        Specifications
      </button>
    </nav>
  </div>
  
  <!-- Tab Content -->
  <div class="p-6">
    <p>This is the content for the active tab.</p>
  </div>
</div>
```

---

## 🔽 Dropdown Menus

Interactive dropdown components:

```html
<!-- Basic Dropdown (requires JavaScript) -->
<div class="relative inline-block">
  <button class="bg-blue-600 text-white px-4 py-2 rounded-lg flex items-center gap-2">
    Menu
    <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
    </svg>
  </button>
  
  <!-- Dropdown Content (toggle with JS) -->
  <div class="absolute right-0 mt-2 w-48 bg-white rounded-lg shadow-lg py-2 z-10 hidden">
    <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-gray-100">Profile</a>
    <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-gray-100">Settings</a>
    <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-gray-100">Logout</a>
  </div>
</div>

<!-- Dropdown with Icons -->
<div class="relative inline-block">
  <button class="bg-gray-100 text-gray-800 px-4 py-2 rounded-lg flex items-center gap-2 hover:bg-gray-200">
    Options
    <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 20 20">
      <path fill-rule="evenodd" d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" clip-rule="evenodd"></path>
    </svg>
  </button>
  
  <div class="absolute right-0 mt-2 w-56 bg-white rounded-lg shadow-lg py-2 z-10 hidden">
    <a href="#" class="flex items-center gap-3 px-4 py-2 text-gray-800 hover:bg-gray-100">
      <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M11 5H6a2 2 0 00-2 2v11a2 2 0 002 2h11a2 2 0 002-2v-5m-1.414-9.414a2 2 0 112.828 2.828L11.828 15H9v-2.828l8.586-8.586z"></path>
      </svg>
      Edit
    </a>
    <a href="#" class="flex items-center gap-3 px-4 py-2 text-gray-800 hover:bg-gray-100">
      <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 16H6a2 2 0 01-2-2V6a2 2 0 012-2h8a2 2 0 012 2v2m-6 12h8a2 2 0 002-2v-8a2 2 0 00-2-2h-8a2 2 0 00-2 2v8a2 2 0 002 2z"></path>
      </svg>
      Duplicate
    </a>
    <div class="border-t border-gray-200 my-2"></div>
    <a href="#" class="flex items-center gap-3 px-4 py-2 text-red-600 hover:bg-red-50">
      <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16"></path>
      </svg>
      Delete
    </a>
  </div>
</div>

<!-- User Menu Dropdown -->
<div class="relative inline-block">
  <button class="flex items-center gap-2 text-gray-700 hover:text-gray-900">
    <img src="avatar.jpg" class="w-8 h-8 rounded-full">
    <span class="font-medium">John Doe</span>
    <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 20 20">
      <path fill-rule="evenodd" d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" clip-rule="evenodd"></path>
    </svg>
  </button>
  
  <div class="absolute right-0 mt-2 w-48 bg-white rounded-lg shadow-lg py-2 z-10 hidden">
    <div class="px-4 py-2 border-b border-gray-200">
      <p class="text-sm font-semibold">John Doe</p>
      <p class="text-xs text-gray-500">john@example.com</p>
    </div>
    <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-gray-100">My Profile</a>
    <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-gray-100">Settings</a>
    <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-gray-100">Billing</a>
    <div class="border-t border-gray-200"></div>
    <a href="#" class="block px-4 py-2 text-red-600 hover:bg-red-50">Sign out</a>
  </div>
</div>
```

---

## 🍞 Breadcrumbs

Navigation trail showing the user's location:

```html
<!-- Basic Breadcrumbs -->
<nav class="flex" aria-label="Breadcrumb">
  <ol class="flex items-center space-x-2">
    <li><a href="#" class="text-blue-600 hover:underline">Home</a></li>
    <li><span class="text-gray-400">/</span></li>
    <li><a href="#" class="text-blue-600 hover:underline">Products</a></li>
    <li><span class="text-gray-400">/</span></li>
    <li><span class="text-gray-600">Electronics</span></li>
  </ol>
</nav>

<!-- Breadcrumbs with Arrows -->
<nav class="flex" aria-label="Breadcrumb">
  <ol class="flex items-center space-x-2">
    <li><a href="#" class="text-gray-600 hover:text-blue-600">Home</a></li>
    <li>
      <svg class="w-4 h-4 text-gray-400" fill="currentColor" viewBox="0 0 20 20">
        <path fill-rule="evenodd" d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z" clip-rule="evenodd"></path>
      </svg>
    </li>
    <li><a href="#" class="text-gray-600 hover:text-blue-600">Category</a></li>
    <li>
      <svg class="w-4 h-4 text-gray-400" fill="currentColor" viewBox="0 0 20 20">
        <path fill-rule="evenodd" d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z" clip-rule="evenodd"></path>
      </svg>
    </li>
    <li><span class="text-gray-900 font-medium">Current Page</span></li>
  </ol>
</nav>

<!-- Breadcrumbs with Background -->
<nav class="bg-gray-100 rounded-lg px-4 py-3">
  <ol class="flex items-center space-x-2 text-sm">
    <li>
      <a href="#" class="flex items-center text-gray-600 hover:text-blue-600">
        <svg class="w-4 h-4 mr-2" fill="currentColor" viewBox="0 0 20 20">
          <path d="M10.707 2.293a1 1 0 00-1.414 0l-7 7a1 1 0 001.414 1.414L4 10.414V17a1 1 0 001 1h2a1 1 0 001-1v-2a1 1 0 011-1h2a1 1 0 011 1v2a1 1 0 001 1h2a1 1 0 001-1v-6.586l.293.293a1 1 0 001.414-1.414l-7-7z"></path>
        </svg>
        Home
      </a>
    </li>
    <li><span class="text-gray-400">/</span></li>
    <li><a href="#" class="text-gray-600 hover:text-blue-600">Library</a></li>
    <li><span class="text-gray-400">/</span></li>
    <li><span class="text-gray-900 font-medium">Data</span></li>
  </ol>
</nav>
```

---

## 📄 Pagination

Navigate through pages of content:

```html
<!-- Basic Pagination -->
<div class="flex items-center gap-2">
  <button class="px-4 py-2 border border-gray-300 rounded hover:bg-gray-50 disabled:opacity-50 disabled:cursor-not-allowed" disabled>
    Previous
  </button>
  <button class="px-4 py-2 bg-blue-600 text-white rounded">1</button>
  <button class="px-4 py-2 border border-gray-300 rounded hover:bg-gray-50">2</button>
  <button class="px-4 py-2 border border-gray-300 rounded hover:bg-gray-50">3</button>
  <button class="px-4 py-2 border border-gray-300 rounded hover:bg-gray-50">4</button>
  <button class="px-4 py-2 border border-gray-300 rounded hover:bg-gray-50">5</button>
  <button class="px-4 py-2 border border-gray-300 rounded hover:bg-gray-50">
    Next
  </button>
</div>

<!-- Pagination with Icons -->
<nav class="flex items-center gap-2">
  <button class="p-2 border border-gray-300 rounded hover:bg-gray-50">
    <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7"></path>
    </svg>
  </button>
  
  <div class="flex gap-1">
    <button class="w-10 h-10 bg-blue-600 text-white rounded font-semibold">1</button>
    <button class="w-10 h-10 border border-gray-300 rounded hover:bg-gray-50">2</button>
    <button class="w-10 h-10 border border-gray-300 rounded hover:bg-gray-50">3</button>
    <span class="w-10 h-10 flex items-center justify-center">...</span>
    <button class="w-10 h-10 border border-gray-300 rounded hover:bg-gray-50">10</button>
  </div>
  
  <button class="p-2 border border-gray-300 rounded hover:bg-gray-50">
    <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"></path>
    </svg>
  </button>
</nav>

<!-- Pagination with Info -->
<div class="flex items-center justify-between">
  <p class="text-sm text-gray-700">
    Showing <span class="font-medium">1</span> to <span class="font-medium">10</span> of{' '}
    <span class="font-medium">97</span> results
  </p>
  
  <nav class="flex gap-2">
    <button class="px-3 py-2 text-sm border border-gray-300 rounded hover:bg-gray-50" disabled>
      Previous
    </button>
    <button class="px-3 py-2 text-sm bg-blue-600 text-white rounded">1</button>
    <button class="px-3 py-2 text-sm border border-gray-300 rounded hover:bg-gray-50">2</button>
    <button class="px-3 py-2 text-sm border border-gray-300 rounded hover:bg-gray-50">3</button>
    <button class="px-3 py-2 text-sm border border-gray-300 rounded hover:bg-gray-50">
      Next
    </button>
  </nav>
</div>

<!-- Simple Prev/Next -->
<div class="flex items-center justify-between">
  <button class="flex items-center gap-2 px-4 py-2 text-sm text-gray-700 border border-gray-300 rounded-lg hover:bg-gray-50">
    <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7"></path>
    </svg>
    Previous
  </button>
  
  <button class="flex items-center gap-2 px-4 py-2 text-sm text-gray-700 border border-gray-300 rounded-lg hover:bg-gray-50">
    Next
    <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"></path>
    </svg>
  </button>
</div>

<!-- Compact Pagination -->
<div class="inline-flex rounded-lg shadow-sm">
  <button class="px-3 py-2 text-sm border border-gray-300 rounded-l-lg hover:bg-gray-50">
    Prev
  </button>
  <button class="px-3 py-2 text-sm border-t border-b border-gray-300 bg-blue-600 text-white">
    1
  </button>
  <button class="px-3 py-2 text-sm border-t border-b border-gray-300 hover:bg-gray-50">
    2
  </button>
  <button class="px-3 py-2 text-sm border-t border-b border-gray-300 hover:bg-gray-50">
    3
  </button>
  <button class="px-3 py-2 text-sm border border-gray-300 rounded-r-lg hover:bg-gray-50">
    Next
  </button>
</div>
```

---

## 🔗 Next Steps

Continue to [07 - Responsive Design](07-responsive.md)!

