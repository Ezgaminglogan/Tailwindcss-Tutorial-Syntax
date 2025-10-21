# 09 - Accessibility & Screen Readers

## ♿ Why Accessibility Matters

Accessible design ensures your website works for everyone, including users with disabilities who rely on screen readers, keyboard navigation, and other assistive technologies.

---

## 👁️ Screen Reader Utilities

### Screen Reader Only

Hide content visually but keep it available for screen readers:

```html
<!-- Visually hidden but readable by screen readers -->
<span class="sr-only">Skip to main content</span>

<!-- Hide from screen readers but visible -->
<div class="not-sr-only">Visible content</div>

<!-- Skip Navigation Link -->
<a href="#main-content" class="sr-only focus:not-sr-only focus:absolute focus:top-4 focus:left-4 focus:z-50 focus:px-4 focus:py-2 focus:bg-white focus:border">
  Skip to main content
</a>
```

**Common Use Cases:**
```html
<!-- Icon Button with SR Description -->
<button class="p-2 bg-blue-600 rounded">
  <svg class="w-6 h-6" aria-hidden="true"><!-- icon --></svg>
  <span class="sr-only">Close menu</span>
</button>

<!-- Form Labels -->
<label class="sr-only" for="search">Search</label>
<input id="search" type="search" placeholder="Search..." class="border rounded px-4 py-2">

<!-- Loading State -->
<div role="status">
  <div class="animate-spin h-8 w-8 border-4 border-blue-600 border-t-transparent rounded-full"></div>
  <span class="sr-only">Loading...</span>
</div>
```

---

## 🎯 Focus Management

### Focus Rings

Accessible focus indicators for keyboard navigation:

```html
<!-- Basic Focus Ring -->
<button class="focus:outline-none focus:ring-2 focus:ring-blue-500">
  Button with focus ring
</button>

<!-- Ring Width -->
<button class="focus:ring-1">Thin ring</button>
<button class="focus:ring-2">Default ring</button>
<button class="focus:ring-4">Thick ring</button>
<button class="focus:ring-8">Extra thick ring</button>

<!-- Ring Color -->
<button class="focus:ring-2 focus:ring-blue-500">Blue ring</button>
<button class="focus:ring-2 focus:ring-green-500">Green ring</button>
<button class="focus:ring-2 focus:ring-red-500">Red ring</button>

<!-- Ring Offset -->
<button class="focus:ring-2 focus:ring-blue-500 focus:ring-offset-2">
  Ring with offset
</button>

<button class="focus:ring-2 focus:ring-white focus:ring-offset-2 focus:ring-offset-blue-600 bg-blue-600 text-white px-4 py-2 rounded">
  Offset ring on dark background
</button>

<!-- Ring Opacity -->
<button class="focus:ring-2 focus:ring-blue-500 focus:ring-opacity-50">
  50% opacity ring
</button>
```

### Focus States

```html
<!-- Focus -->
<input class="border-2 border-gray-300 focus:border-blue-500 focus:ring-2 focus:ring-blue-200">

<!-- Focus Visible (only keyboard focus) -->
<button class="focus-visible:ring-2 focus-visible:ring-blue-500">
  Ring only on keyboard focus
</button>

<!-- Focus Within (when child is focused) -->
<form class="border-2 border-gray-300 p-4 focus-within:border-blue-500 focus-within:shadow-lg">
  <input class="border rounded px-4 py-2" placeholder="Focus me">
</form>

<!-- Accessible Card Link -->
<a href="#" class="block group rounded-lg border-2 border-transparent p-6 hover:border-blue-500 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2">
  <h3 class="text-xl font-bold group-hover:text-blue-600">Card Title</h3>
  <p class="text-gray-600">Card description</p>
</a>
```

---

## ⌨️ Keyboard Navigation

### Tab Index

```html
<!-- Make non-interactive elements focusable -->
<div tabindex="0" class="focus:ring-2 focus:ring-blue-500">
  Focusable div
</div>

<!-- Remove from tab order -->
<button tabindex="-1">Not in tab order</button>

<!-- Custom tab order (avoid if possible) -->
<input tabindex="2">
<input tabindex="1">
<input tabindex="3">
```

### Interactive States

```html
<!-- Hover and Focus Together -->
<button class="bg-blue-600 hover:bg-blue-700 focus:bg-blue-700 focus:ring-2 focus:ring-blue-300">
  Accessible button
</button>

<!-- Active State -->
<button class="bg-blue-600 active:bg-blue-800 active:scale-95 transition">
  Press feedback
</button>

<!-- Disabled State -->
<button disabled class="bg-gray-400 cursor-not-allowed opacity-50" aria-disabled="true">
  Disabled button
</button>
```

---

## 🖱️ Pointer & Touch

### Pointer Events

```html
<!-- Disable pointer events -->
<div class="pointer-events-none">
  Can't interact with this
</div>

<!-- Enable pointer events -->
<div class="pointer-events-auto">
  Can interact with this
</div>

<!-- Use Case: Overlay that allows clicking through -->
<div class="relative">
  <img src="photo.jpg" alt="Photo">
  <div class="absolute inset-0 bg-black opacity-50 pointer-events-none"></div>
  <button class="absolute bottom-4 right-4 pointer-events-auto">Click me</button>
</div>
```

### Touch Actions

```html
<!-- Control touch gestures -->
<div class="touch-auto">Auto touch behavior</div>
<div class="touch-none">No touch gestures</div>
<div class="touch-pan-x">Only horizontal panning</div>
<div class="touch-pan-y">Only vertical panning</div>
<div class="touch-pinch-zoom">Allow pinch zoom</div>
```

---

## 📱 Resize

Control textarea/element resizing:

```html
<!-- Resize Control -->
<textarea class="resize-none">Cannot resize</textarea>
<textarea class="resize-y">Resize vertically only</textarea>
<textarea class="resize-x">Resize horizontally only</textarea>
<textarea class="resize">Resize both directions</textarea>
```

---

## 🎯 ARIA Attributes & Semantic HTML

### Proper Button Usage

```html
<!-- ❌ Bad: Using div as button -->
<div onclick="doSomething()">Click me</div>

<!-- ✅ Good: Using button element -->
<button type="button" class="bg-blue-600 text-white px-4 py-2 rounded">
  Click me
</button>

<!-- ✅ Good: Link styled as button -->
<a href="/page" class="inline-block bg-blue-600 text-white px-4 py-2 rounded">
  Go to page
</a>
```

### ARIA Labels

```html
<!-- Button with icon only -->
<button aria-label="Close dialog" class="p-2">
  <svg class="w-6 h-6"><!-- X icon --></svg>
</button>

<!-- Descriptive link -->
<a href="/learn-more" aria-label="Learn more about our services">
  Read more →
</a>

<!-- Live Region for Dynamic Content -->
<div aria-live="polite" aria-atomic="true" class="sr-only">
  <span id="status-message"></span>
</div>

<!-- Progress Bar -->
<div role="progressbar" aria-valuenow="75" aria-valuemin="0" aria-valuemax="100" class="w-full bg-gray-200 rounded-full h-2">
  <div class="bg-blue-600 h-2 rounded-full" style="width: 75%"></div>
</div>
```

### Form Accessibility

```html
<!-- Accessible Form -->
<form class="space-y-4">
  <!-- Proper Label Association -->
  <div>
    <label for="email" class="block text-gray-700 font-medium mb-2">
      Email Address <span class="text-red-500" aria-label="required">*</span>
    </label>
    <input 
      type="email" 
      id="email"
      name="email"
      required
      aria-required="true"
      aria-describedby="email-error"
      class="border border-gray-300 rounded-lg px-4 py-2 w-full focus:outline-none focus:ring-2 focus:ring-blue-500"
    >
    <p id="email-error" class="text-red-600 text-sm mt-1 hidden">
      Please enter a valid email address
    </p>
  </div>

  <!-- Fieldset for Radio Groups -->
  <fieldset class="border border-gray-300 rounded p-4">
    <legend class="text-lg font-semibold px-2">Choose a plan</legend>
    <div class="space-y-2 mt-2">
      <label class="flex items-center gap-2">
        <input type="radio" name="plan" value="basic" class="focus:ring-2 focus:ring-blue-500">
        <span>Basic Plan</span>
      </label>
      <label class="flex items-center gap-2">
        <input type="radio" name="plan" value="pro" class="focus:ring-2 focus:ring-blue-500">
        <span>Pro Plan</span>
      </label>
    </div>
  </fieldset>

  <!-- Error Summary -->
  <div role="alert" class="bg-red-100 border border-red-400 text-red-700 px-4 py-3 rounded hidden">
    <strong>Please fix the following errors:</strong>
    <ul class="list-disc list-inside mt-2">
      <li>Email is required</li>
      <li>Password must be at least 8 characters</li>
    </ul>
  </div>

  <button type="submit" class="w-full bg-blue-600 text-white py-3 rounded-lg font-semibold hover:bg-blue-700 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2">
    Submit Form
  </button>
</form>
```

---

## 🎨 Color Contrast

### Accessible Color Combinations

```html
<!-- ✅ Good Contrast (WCAG AA) -->
<div class="bg-blue-600 text-white p-4">
  High contrast text (4.5:1+)
</div>

<div class="bg-gray-100 text-gray-900 p-4">
  High contrast on light background
</div>

<!-- ⚠️ Poor Contrast (Avoid) -->
<div class="bg-gray-300 text-gray-400 p-4">
  Low contrast - hard to read
</div>

<!-- ✅ Focus Indicators -->
<button class="bg-white text-gray-900 border-2 border-gray-900 px-4 py-2 focus:outline-none focus:ring-4 focus:ring-blue-500">
  High contrast focus
</button>
```

### Text Size for Readability

```html
<!-- Minimum 16px (text-base) for body text -->
<p class="text-base">This is readable body text</p>

<!-- Larger for headings -->
<h1 class="text-4xl font-bold">Main Heading</h1>
<h2 class="text-2xl font-semibold">Subheading</h2>

<!-- Avoid text smaller than 14px -->
<p class="text-sm">Small but still readable (14px)</p>
```

---

## 🔊 Motion & Animations

### Respect User Preferences

```html
<!-- Reduce motion for users who prefer it -->
<div class="motion-reduce:animate-none animate-bounce">
  Bouncing element (respects prefers-reduced-motion)
</div>

<button class="transition-transform motion-reduce:transition-none hover:scale-110">
  Scales on hover (respects motion preference)
</button>

<!-- Skip animations for accessibility -->
<style>
  @media (prefers-reduced-motion: reduce) {
    * {
      animation-duration: 0.01ms !important;
      transition-duration: 0.01ms !important;
    }
  }
</style>
```

---

## 📋 Complete Accessible Component Examples

### Accessible Modal

```html
<div role="dialog" aria-labelledby="modal-title" aria-describedby="modal-desc" aria-modal="true" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50">
  <div class="bg-white rounded-lg shadow-2xl p-6 max-w-md w-full m-4" role="document">
    <div class="flex items-center justify-between mb-4">
      <h2 id="modal-title" class="text-2xl font-bold">Modal Title</h2>
      <button 
        aria-label="Close modal"
        class="text-gray-500 hover:text-gray-700 focus:outline-none focus:ring-2 focus:ring-blue-500 rounded p-1"
      >
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
        </svg>
      </button>
    </div>
    <p id="modal-desc" class="text-gray-700 mb-6">
      This is the modal content.
    </p>
    <div class="flex gap-3">
      <button class="flex-1 border border-gray-300 text-gray-700 py-2 rounded hover:bg-gray-50 focus:outline-none focus:ring-2 focus:ring-gray-500">
        Cancel
      </button>
      <button class="flex-1 bg-blue-600 text-white py-2 rounded hover:bg-blue-700 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2">
        Confirm
      </button>
    </div>
  </div>
</div>
```

### Accessible Navigation

```html
<nav aria-label="Main navigation" class="bg-white shadow">
  <div class="max-w-6xl mx-auto px-6 py-4">
    <ul class="flex items-center gap-6">
      <li>
        <a 
          href="/" 
          aria-current="page"
          class="text-blue-600 font-semibold focus:outline-none focus:ring-2 focus:ring-blue-500 rounded px-2 py-1"
        >
          Home
        </a>
      </li>
      <li>
        <a 
          href="/about" 
          class="text-gray-700 hover:text-blue-600 focus:outline-none focus:ring-2 focus:ring-blue-500 rounded px-2 py-1"
        >
          About
        </a>
      </li>
      <li>
        <a 
          href="/contact" 
          class="text-gray-700 hover:text-blue-600 focus:outline-none focus:ring-2 focus:ring-blue-500 rounded px-2 py-1"
        >
          Contact
        </a>
      </li>
    </ul>
  </div>
</nav>
```

### Accessible Card

```html
<article class="bg-white rounded-lg shadow-lg overflow-hidden group">
  <img src="photo.jpg" alt="Beautiful landscape with mountains" class="w-full h-48 object-cover group-hover:scale-105 transition">
  <div class="p-6">
    <h3 class="text-xl font-bold mb-2">
      <a 
        href="/article" 
        class="hover:text-blue-600 focus:outline-none focus:text-blue-600"
      >
        Article Title
        <span class="sr-only">(opens article page)</span>
      </a>
    </h3>
    <p class="text-gray-600 mb-4">
      Article description goes here...
    </p>
    <time datetime="2025-10-21" class="text-sm text-gray-500">
      October 21, 2025
    </time>
  </div>
</article>
```

---

## ✅ Accessibility Checklist

### Interactive Elements
- [ ] All interactive elements are keyboard accessible
- [ ] Focus indicators are visible and high contrast
- [ ] Tab order is logical
- [ ] No keyboard traps

### Content
- [ ] Images have alt text
- [ ] Icons have labels (visible or sr-only)
- [ ] Text has sufficient contrast (4.5:1 minimum)
- [ ] Text is at least 16px for body content

### Forms
- [ ] All inputs have associated labels
- [ ] Required fields are marked
- [ ] Error messages are clear and associated with fields
- [ ] Success/error feedback is provided

### Navigation
- [ ] Skip links are provided
- [ ] Landmark regions are used (nav, main, footer)
- [ ] Current page is indicated in navigation

### Media
- [ ] Videos have captions
- [ ] Audio has transcripts
- [ ] Autoplay is avoided or can be paused

### Testing
- [ ] Test with keyboard only
- [ ] Test with screen reader
- [ ] Check color contrast
- [ ] Validate HTML
- [ ] Test with reduced motion

---

## 🎯 Pro Tips

1. **Always use semantic HTML** - Use `<button>`, `<nav>`, `<main>`, etc.
2. **Don't rely on color alone** - Use icons, text, or patterns
3. **Test with real users** - Include people who use assistive tech
4. **Use ARIA sparingly** - Semantic HTML is better when possible
5. **Keyboard test everything** - Can you do everything with Tab and Enter?
6. **Focus indicators are required** - Never use `outline: none` without replacement
7. **Respect user preferences** - Honor reduced motion, high contrast, etc.

---

## 🔗 Next Steps

You've completed the Tailwind CSS tutorial! Now you know:
- ✅ All core utilities
- ✅ Advanced layouts and responsive design
- ✅ Complete component library
- ✅ Animations and effects
- ✅ **Accessibility best practices**

Continue to [Practice Projects](practice-projects.md) to build real applications! 🚀

