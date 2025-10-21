# 03 - Forms & Inputs

## 📝 Basic Input Fields

### Text Input

```html
<input 
  type="text" 
  placeholder="Enter your name"
  class="border border-gray-300 rounded-lg px-4 py-2 w-full focus:outline-none focus:ring-2 focus:ring-blue-500"
>
```

**Key Classes:**
- `border border-gray-300` - Border
- `rounded-lg` - Rounded corners
- `px-4 py-2` - Padding
- `w-full` - Full width
- `focus:outline-none` - Remove default outline
- `focus:ring-2 focus:ring-blue-500` - Blue ring on focus

---

## 🎨 Input Variations

### Email Input

```html
<input 
  type="email" 
  placeholder="name@example.com"
  class="border border-gray-300 rounded-lg px-4 py-2 w-full focus:outline-none focus:border-blue-500"
>
```

### Password Input

```html
<input 
  type="password" 
  placeholder="Enter password"
  class="border border-gray-300 rounded-lg px-4 py-2 w-full focus:outline-none focus:ring-2 focus:ring-purple-500"
>
```

### Number Input

```html
<input 
  type="number" 
  placeholder="Age"
  class="border border-gray-300 rounded-lg px-4 py-2 w-full"
>
```

### Date Input

```html
<input 
  type="date" 
  class="border border-gray-300 rounded-lg px-4 py-2 w-full"
>
```

---

## 📋 Textarea

```html
<textarea 
  placeholder="Enter your message"
  rows="4"
  class="border border-gray-300 rounded-lg px-4 py-2 w-full resize-none focus:outline-none focus:ring-2 focus:ring-blue-500"
></textarea>
```

**Additional Classes:**
- `resize-none` - Disable resize handle
- `resize-y` - Allow vertical resize only
- `resize-x` - Allow horizontal resize only

---

## 📂 Select Dropdown

```html
<select class="border border-gray-300 rounded-lg px-4 py-2 w-full bg-white focus:outline-none focus:ring-2 focus:ring-blue-500">
  <option>Select an option</option>
  <option value="1">Option 1</option>
  <option value="2">Option 2</option>
  <option value="3">Option 3</option>
</select>
```

---

## ✅ Checkboxes

```html
<div class="flex items-center gap-2">
  <input 
    type="checkbox" 
    id="agree" 
    class="w-4 h-4 text-blue-600 rounded focus:ring-2 focus:ring-blue-500"
  >
  <label for="agree" class="text-gray-700">I agree to terms and conditions</label>
</div>
```

---

## 🔘 Radio Buttons

```html
<div class="flex flex-col gap-2">
  <div class="flex items-center gap-2">
    <input 
      type="radio" 
      id="male" 
      name="gender" 
      class="w-4 h-4 text-blue-600"
    >
    <label for="male" class="text-gray-700">Male</label>
  </div>
  
  <div class="flex items-center gap-2">
    <input 
      type="radio" 
      id="female" 
      name="gender" 
      class="w-4 h-4 text-blue-600"
    >
    <label for="female" class="text-gray-700">Female</label>
  </div>
</div>
```

---

## 🏷️ Input with Label

```html
<div class="mb-4">
  <label for="email" class="block text-gray-700 font-medium mb-2">
    Email Address
  </label>
  <input 
    type="email" 
    id="email"
    placeholder="you@example.com"
    class="border border-gray-300 rounded-lg px-4 py-2 w-full focus:outline-none focus:ring-2 focus:ring-blue-500"
  >
</div>
```

---

## 📊 Form Layout Examples

### Vertical Form

```html
<form class="max-w-md mx-auto bg-white p-8 rounded-lg shadow-lg">
  <h2 class="text-2xl font-bold mb-6 text-gray-900">Sign Up</h2>
  
  <!-- Name -->
  <div class="mb-4">
    <label class="block text-gray-700 font-medium mb-2">Full Name</label>
    <input 
      type="text" 
      placeholder="John Doe"
      class="border border-gray-300 rounded-lg px-4 py-2 w-full focus:outline-none focus:ring-2 focus:ring-blue-500"
    >
  </div>
  
  <!-- Email -->
  <div class="mb-4">
    <label class="block text-gray-700 font-medium mb-2">Email</label>
    <input 
      type="email" 
      placeholder="john@example.com"
      class="border border-gray-300 rounded-lg px-4 py-2 w-full focus:outline-none focus:ring-2 focus:ring-blue-500"
    >
  </div>
  
  <!-- Password -->
  <div class="mb-6">
    <label class="block text-gray-700 font-medium mb-2">Password</label>
    <input 
      type="password" 
      placeholder="••••••••"
      class="border border-gray-300 rounded-lg px-4 py-2 w-full focus:outline-none focus:ring-2 focus:ring-blue-500"
    >
  </div>
  
  <!-- Submit Button -->
  <button 
    type="submit"
    class="w-full bg-blue-600 text-white py-3 rounded-lg font-semibold hover:bg-blue-700 transition-colors"
  >
    Sign Up
  </button>
</form>
```

---

### Two-Column Form

```html
<form class="max-w-4xl mx-auto bg-white p-8 rounded-lg shadow-lg">
  <h2 class="text-2xl font-bold mb-6">Contact Information</h2>
  
  <div class="grid grid-cols-2 gap-4">
    <!-- First Name -->
    <div>
      <label class="block text-gray-700 font-medium mb-2">First Name</label>
      <input 
        type="text" 
        class="border border-gray-300 rounded-lg px-4 py-2 w-full"
      >
    </div>
    
    <!-- Last Name -->
    <div>
      <label class="block text-gray-700 font-medium mb-2">Last Name</label>
      <input 
        type="text" 
        class="border border-gray-300 rounded-lg px-4 py-2 w-full"
      >
    </div>
    
    <!-- Email (Full Width) -->
    <div class="col-span-2">
      <label class="block text-gray-700 font-medium mb-2">Email</label>
      <input 
        type="email" 
        class="border border-gray-300 rounded-lg px-4 py-2 w-full"
      >
    </div>
    
    <!-- Phone -->
    <div>
      <label class="block text-gray-700 font-medium mb-2">Phone</label>
      <input 
        type="tel" 
        class="border border-gray-300 rounded-lg px-4 py-2 w-full"
      >
    </div>
    
    <!-- Country -->
    <div>
      <label class="block text-gray-700 font-medium mb-2">Country</label>
      <select class="border border-gray-300 rounded-lg px-4 py-2 w-full bg-white">
        <option>United States</option>
        <option>Canada</option>
        <option>UK</option>
      </select>
    </div>
  </div>
  
  <button 
    type="submit"
    class="mt-6 bg-green-600 text-white px-8 py-3 rounded-lg font-semibold hover:bg-green-700"
  >
    Submit
  </button>
</form>
```

---

## 🎯 Input States

### Success State

```html
<div class="mb-4">
  <input 
    type="text" 
    value="john@example.com"
    class="border-2 border-green-500 rounded-lg px-4 py-2 w-full bg-green-50"
  >
  <p class="text-green-600 text-sm mt-1">✓ Email is valid</p>
</div>
```

### Error State

```html
<div class="mb-4">
  <input 
    type="text" 
    value="invalidemail"
    class="border-2 border-red-500 rounded-lg px-4 py-2 w-full bg-red-50"
  >
  <p class="text-red-600 text-sm mt-1">✗ Please enter a valid email</p>
</div>
```

### Disabled State

```html
<input 
  type="text" 
  disabled
  value="Disabled input"
  class="border border-gray-300 rounded-lg px-4 py-2 w-full bg-gray-100 text-gray-500 cursor-not-allowed"
>
```

---

## 🔍 Search Input

```html
<div class="relative">
  <input 
    type="search" 
    placeholder="Search..."
    class="border border-gray-300 rounded-full px-4 py-2 pl-10 w-full focus:outline-none focus:ring-2 focus:ring-blue-500"
  >
  <svg class="absolute left-3 top-2.5 w-5 h-5 text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"></path>
  </svg>
</div>
```

---

## 📦 Complete Login Form Example

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login Form</title>
    <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
</head>
<body class="bg-gradient-to-br from-blue-500 to-purple-600 min-h-screen flex items-center justify-center p-4">
    
    <!-- Login Form -->
    <div class="bg-white rounded-2xl shadow-2xl p-8 w-full max-w-md">
        <h2 class="text-3xl font-bold text-gray-900 text-center mb-8">Welcome Back</h2>
        
        <form>
            <!-- Email -->
            <div class="mb-4">
                <label class="block text-gray-700 font-medium mb-2">Email Address</label>
                <input 
                    type="email" 
                    placeholder="you@example.com"
                    class="border border-gray-300 rounded-lg px-4 py-3 w-full focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-transparent"
                >
            </div>
            
            <!-- Password -->
            <div class="mb-6">
                <label class="block text-gray-700 font-medium mb-2">Password</label>
                <input 
                    type="password" 
                    placeholder="••••••••"
                    class="border border-gray-300 rounded-lg px-4 py-3 w-full focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-transparent"
                >
            </div>
            
            <!-- Remember Me & Forgot Password -->
            <div class="flex items-center justify-between mb-6">
                <div class="flex items-center gap-2">
                    <input type="checkbox" id="remember" class="w-4 h-4">
                    <label for="remember" class="text-sm text-gray-600">Remember me</label>
                </div>
                <a href="#" class="text-sm text-blue-600 hover:underline">Forgot password?</a>
            </div>
            
            <!-- Submit Button -->
            <button 
                type="submit"
                class="w-full bg-blue-600 text-white py-3 rounded-lg font-semibold hover:bg-blue-700 transition-colors"
            >
                Sign In
            </button>
        </form>
        
        <!-- Sign Up Link -->
        <p class="text-center text-gray-600 mt-6">
            Don't have an account? 
            <a href="#" class="text-blue-600 font-semibold hover:underline">Sign up</a>
        </p>
    </div>

</body>
</html>
```

---

## ✅ Practice Exercise

Create a registration form with:
- First Name and Last Name (side by side)
- Email field
- Password field with strength indicator
- Confirm Password field
- Terms & Conditions checkbox
- Sign Up button (full width, green)

---

## 🔗 Next Steps

Continue to [04 - Buttons & Cards](04-components.md) to learn about common UI components!

