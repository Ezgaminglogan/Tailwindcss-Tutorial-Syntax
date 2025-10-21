# 05 - CRUD Interface Examples

## 📋 What is CRUD?

**CRUD** stands for:
- **C**reate - Add new records
- **R**ead - View/List records
- **U**pdate - Edit existing records
- **D**elete - Remove records

---

## 📊 Simple Data Table

```html
<div class="bg-white rounded-lg shadow-lg overflow-hidden">
  <table class="w-full">
    <thead class="bg-gray-800 text-white">
      <tr>
        <th class="px-6 py-3 text-left">ID</th>
        <th class="px-6 py-3 text-left">Name</th>
        <th class="px-6 py-3 text-left">Email</th>
        <th class="px-6 py-3 text-left">Actions</th>
      </tr>
    </thead>
    <tbody class="divide-y divide-gray-200">
      <tr class="hover:bg-gray-50">
        <td class="px-6 py-4">1</td>
        <td class="px-6 py-4">John Doe</td>
        <td class="px-6 py-4">john@example.com</td>
        <td class="px-6 py-4">
          <button class="text-blue-600 hover:underline mr-3">Edit</button>
          <button class="text-red-600 hover:underline">Delete</button>
        </td>
      </tr>
      <tr class="hover:bg-gray-50">
        <td class="px-6 py-4">2</td>
        <td class="px-6 py-4">Jane Smith</td>
        <td class="px-6 py-4">jane@example.com</td>
        <td class="px-6 py-4">
          <button class="text-blue-600 hover:underline mr-3">Edit</button>
          <button class="text-red-600 hover:underline">Delete</button>
        </td>
      </tr>
    </tbody>
  </table>
</div>
```

---

## ➕ Create Form Modal

```html
<!-- Modal Overlay -->
<div class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center p-4">
  
  <!-- Modal Content -->
  <div class="bg-white rounded-lg shadow-2xl max-w-md w-full">
    
    <!-- Modal Header -->
    <div class="flex justify-between items-center border-b px-6 py-4">
      <h2 class="text-2xl font-bold">Add New User</h2>
      <button class="text-gray-500 hover:text-gray-700">
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
        </svg>
      </button>
    </div>
    
    <!-- Modal Body -->
    <form class="p-6">
      <div class="mb-4">
        <label class="block text-gray-700 font-medium mb-2">Full Name</label>
        <input 
          type="text" 
          placeholder="Enter name"
          class="border border-gray-300 rounded-lg px-4 py-2 w-full focus:outline-none focus:ring-2 focus:ring-blue-500"
        >
      </div>
      
      <div class="mb-4">
        <label class="block text-gray-700 font-medium mb-2">Email</label>
        <input 
          type="email" 
          placeholder="Enter email"
          class="border border-gray-300 rounded-lg px-4 py-2 w-full focus:outline-none focus:ring-2 focus:ring-blue-500"
        >
      </div>
      
      <div class="mb-6">
        <label class="block text-gray-700 font-medium mb-2">Role</label>
        <select class="border border-gray-300 rounded-lg px-4 py-2 w-full bg-white">
          <option>User</option>
          <option>Admin</option>
          <option>Manager</option>
        </select>
      </div>
      
      <!-- Modal Footer -->
      <div class="flex gap-3">
        <button 
          type="button"
          class="flex-1 border border-gray-300 text-gray-700 py-2 rounded-lg font-semibold hover:bg-gray-50"
        >
          Cancel
        </button>
        <button 
          type="submit"
          class="flex-1 bg-blue-600 text-white py-2 rounded-lg font-semibold hover:bg-blue-700"
        >
          Add User
        </button>
      </div>
    </form>
    
  </div>
</div>
```

---

## 🗑️ Delete Confirmation

```html
<div class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center p-4">
  <div class="bg-white rounded-lg shadow-2xl max-w-md w-full p-6">
    
    <!-- Icon -->
    <div class="flex justify-center mb-4">
      <div class="w-16 h-16 bg-red-100 rounded-full flex items-center justify-center">
        <svg class="w-8 h-8 text-red-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 9v2m0 4h.01m-6.938 4h13.856c1.54 0 2.502-1.667 1.732-3L13.732 4c-.77-1.333-2.694-1.333-3.464 0L3.34 16c-.77 1.333.192 3 1.732 3z"></path>
        </svg>
      </div>
    </div>
    
    <h2 class="text-2xl font-bold text-center mb-2">Delete User?</h2>
    <p class="text-gray-600 text-center mb-6">
      Are you sure you want to delete this user? This action cannot be undone.
    </p>
    
    <div class="flex gap-3">
      <button class="flex-1 border border-gray-300 text-gray-700 py-2 rounded-lg font-semibold hover:bg-gray-50">
        Cancel
      </button>
      <button class="flex-1 bg-red-600 text-white py-2 rounded-lg font-semibold hover:bg-red-700">
        Delete
      </button>
    </div>
    
  </div>
</div>
```

---

## ✏️ Edit Form

```html
<div class="bg-white rounded-lg shadow-lg p-6 max-w-2xl mx-auto">
  <h2 class="text-2xl font-bold mb-6">Edit User</h2>
  
  <form>
    <div class="grid grid-cols-2 gap-4 mb-4">
      <div>
        <label class="block text-gray-700 font-medium mb-2">First Name</label>
        <input 
          type="text" 
          value="John"
          class="border border-gray-300 rounded-lg px-4 py-2 w-full"
        >
      </div>
      <div>
        <label class="block text-gray-700 font-medium mb-2">Last Name</label>
        <input 
          type="text" 
          value="Doe"
          class="border border-gray-300 rounded-lg px-4 py-2 w-full"
        >
      </div>
    </div>
    
    <div class="mb-4">
      <label class="block text-gray-700 font-medium mb-2">Email</label>
      <input 
        type="email" 
        value="john@example.com"
        class="border border-gray-300 rounded-lg px-4 py-2 w-full"
      >
    </div>
    
    <div class="mb-6">
      <label class="block text-gray-700 font-medium mb-2">Role</label>
      <select class="border border-gray-300 rounded-lg px-4 py-2 w-full bg-white">
        <option>User</option>
        <option selected>Admin</option>
        <option>Manager</option>
      </select>
    </div>
    
    <div class="flex gap-3">
      <button 
        type="button"
        class="border border-gray-300 text-gray-700 px-6 py-2 rounded-lg hover:bg-gray-50"
      >
        Cancel
      </button>
      <button 
        type="submit"
        class="bg-blue-600 text-white px-6 py-2 rounded-lg hover:bg-blue-700"
      >
        Save Changes
      </button>
    </div>
  </form>
</div>
```

---

## 📋 Complete CRUD Dashboard

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>User Management</title>
    <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
</head>
<body class="bg-gray-100">
    
    <!-- Dashboard Container -->
    <div class="flex h-screen">
        
        <!-- Sidebar -->
        <aside class="w-64 bg-gray-800 text-white">
            <div class="p-6">
                <h1 class="text-2xl font-bold">Admin Panel</h1>
            </div>
            <nav class="px-4">
                <a href="#" class="block px-4 py-3 rounded bg-gray-700 mb-2">Dashboard</a>
                <a href="#" class="block px-4 py-3 rounded hover:bg-gray-700 mb-2">Users</a>
                <a href="#" class="block px-4 py-3 rounded hover:bg-gray-700 mb-2">Products</a>
                <a href="#" class="block px-4 py-3 rounded hover:bg-gray-700">Settings</a>
            </nav>
        </aside>
        
        <!-- Main Content -->
        <main class="flex-1 overflow-auto">
            
            <!-- Header -->
            <header class="bg-white shadow-sm">
                <div class="px-8 py-4 flex justify-between items-center">
                    <h2 class="text-2xl font-bold">User Management</h2>
                    <button class="bg-blue-600 text-white px-4 py-2 rounded-lg hover:bg-blue-700 flex items-center gap-2">
                        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4v16m8-8H4"></path>
                        </svg>
                        Add New User
                    </button>
                </div>
            </header>
            
            <!-- Content Area -->
            <div class="p-8">
                
                <!-- Search & Filter -->
                <div class="bg-white rounded-lg shadow p-6 mb-6">
                    <div class="flex gap-4">
                        <input 
                            type="search" 
                            placeholder="Search users..."
                            class="flex-1 border border-gray-300 rounded-lg px-4 py-2"
                        >
                        <select class="border border-gray-300 rounded-lg px-4 py-2 bg-white">
                            <option>All Roles</option>
                            <option>Admin</option>
                            <option>User</option>
                            <option>Manager</option>
                        </select>
                        <button class="bg-gray-200 text-gray-700 px-6 py-2 rounded-lg hover:bg-gray-300">
                            Filter
                        </button>
                    </div>
                </div>
                
                <!-- Data Table -->
                <div class="bg-white rounded-lg shadow-lg overflow-hidden">
                    <table class="w-full">
                        <thead class="bg-gray-800 text-white">
                            <tr>
                                <th class="px-6 py-3 text-left">ID</th>
                                <th class="px-6 py-3 text-left">Name</th>
                                <th class="px-6 py-3 text-left">Email</th>
                                <th class="px-6 py-3 text-left">Role</th>
                                <th class="px-6 py-3 text-left">Status</th>
                                <th class="px-6 py-3 text-left">Actions</th>
                            </tr>
                        </thead>
                        <tbody class="divide-y divide-gray-200">
                            <tr class="hover:bg-gray-50">
                                <td class="px-6 py-4">1</td>
                                <td class="px-6 py-4 font-medium">John Doe</td>
                                <td class="px-6 py-4">john@example.com</td>
                                <td class="px-6 py-4">
                                    <span class="bg-purple-100 text-purple-800 px-3 py-1 rounded-full text-sm">Admin</span>
                                </td>
                                <td class="px-6 py-4">
                                    <span class="bg-green-100 text-green-800 px-3 py-1 rounded-full text-sm">Active</span>
                                </td>
                                <td class="px-6 py-4">
                                    <button class="text-blue-600 hover:underline mr-3">Edit</button>
                                    <button class="text-red-600 hover:underline">Delete</button>
                                </td>
                            </tr>
                            <tr class="hover:bg-gray-50">
                                <td class="px-6 py-4">2</td>
                                <td class="px-6 py-4 font-medium">Jane Smith</td>
                                <td class="px-6 py-4">jane@example.com</td>
                                <td class="px-6 py-4">
                                    <span class="bg-blue-100 text-blue-800 px-3 py-1 rounded-full text-sm">User</span>
                                </td>
                                <td class="px-6 py-4">
                                    <span class="bg-green-100 text-green-800 px-3 py-1 rounded-full text-sm">Active</span>
                                </td>
                                <td class="px-6 py-4">
                                    <button class="text-blue-600 hover:underline mr-3">Edit</button>
                                    <button class="text-red-600 hover:underline">Delete</button>
                                </td>
                            </tr>
                            <tr class="hover:bg-gray-50">
                                <td class="px-6 py-4">3</td>
                                <td class="px-6 py-4 font-medium">Bob Johnson</td>
                                <td class="px-6 py-4">bob@example.com</td>
                                <td class="px-6 py-4">
                                    <span class="bg-green-100 text-green-800 px-3 py-1 rounded-full text-sm">Manager</span>
                                </td>
                                <td class="px-6 py-4">
                                    <span class="bg-gray-100 text-gray-800 px-3 py-1 rounded-full text-sm">Inactive</span>
                                </td>
                                <td class="px-6 py-4">
                                    <button class="text-blue-600 hover:underline mr-3">Edit</button>
                                    <button class="text-red-600 hover:underline">Delete</button>
                                </td>
                            </tr>
                        </tbody>
                    </table>
                </div>
                
                <!-- Pagination -->
                <div class="flex justify-between items-center mt-6">
                    <p class="text-gray-600">Showing 1 to 3 of 12 entries</p>
                    <div class="flex gap-2">
                        <button class="border border-gray-300 px-4 py-2 rounded hover:bg-gray-50">Previous</button>
                        <button class="bg-blue-600 text-white px-4 py-2 rounded">1</button>
                        <button class="border border-gray-300 px-4 py-2 rounded hover:bg-gray-50">2</button>
                        <button class="border border-gray-300 px-4 py-2 rounded hover:bg-gray-50">3</button>
                        <button class="border border-gray-300 px-4 py-2 rounded hover:bg-gray-50">Next</button>
                    </div>
                </div>
                
            </div>
        </main>
    </div>

</body>
</html>
```

---

## 🎯 Product CRUD Example

```html
<!-- Product Card with Actions -->
<div class="bg-white rounded-lg shadow-lg overflow-hidden">
  <div class="h-48 bg-gradient-to-br from-blue-400 to-purple-600"></div>
  <div class="p-4">
    <h3 class="text-lg font-bold mb-1">Product Name</h3>
    <p class="text-gray-600 text-sm mb-3">Product description goes here</p>
    <div class="flex items-center justify-between">
      <span class="text-xl font-bold text-blue-600">$29.99</span>
      <div class="flex gap-2">
        <button class="bg-blue-600 text-white p-2 rounded hover:bg-blue-700">
          <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M11 5H6a2 2 0 00-2 2v11a2 2 0 002 2h11a2 2 0 002-2v-5m-1.414-9.414a2 2 0 112.828 2.828L11.828 15H9v-2.828l8.586-8.586z"></path>
          </svg>
        </button>
        <button class="bg-red-600 text-white p-2 rounded hover:bg-red-700">
          <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16"></path>
          </svg>
        </button>
      </div>
    </div>
  </div>
</div>
```

---

## ✅ Practice Exercise

Build a simple blog post CRUD with:
1. List view showing all posts (title, author, date)
2. Add new post button (opens modal)
3. Edit button for each post
4. Delete button with confirmation
5. Search functionality

---

## 🔗 Next Steps

Continue to [06 - Navigation](06-navigation.md) to learn about different navigation patterns!

