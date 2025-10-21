# 🎨 Visual Layout Diagrams

ASCII diagrams showing how layouts work in Tailwind CSS.

## 📐 Flexbox Layouts

### justify-start (default)
```
┌─────────────────────────────┐
│ [A] [B] [C]                 │
└─────────────────────────────┘
```

### justify-center
```
┌─────────────────────────────┐
│         [A] [B] [C]         │
└─────────────────────────────┘
```

### justify-end
```
┌─────────────────────────────┐
│                 [A] [B] [C] │
└─────────────────────────────┘
```

### justify-between
```
┌─────────────────────────────┐
│ [A]       [B]       [C]     │
└─────────────────────────────┘
```

### justify-around
```
┌─────────────────────────────┐
│  [A]     [B]     [C]        │
└─────────────────────────────┘
```

---

## 🔄 Flex Direction

### flex-row (default - horizontal)
```
┌───────────────────┐
│ [1] [2] [3] [4]   │
└───────────────────┘
```

### flex-col (vertical)
```
┌─────┐
│ [1] │
│ [2] │
│ [3] │
│ [4] │
└─────┘
```

---

## 📊 Grid Layouts

### grid-cols-2
```
┌─────────┬─────────┐
│    A    │    B    │
├─────────┼─────────┤
│    C    │    D    │
└─────────┴─────────┘
```

### grid-cols-3
```
┌──────┬──────┬──────┐
│  A   │  B   │  C   │
├──────┼──────┼──────┤
│  D   │  E   │  F   │
└──────┴──────┴──────┘
```

### grid-cols-4
```
┌────┬────┬────┬────┐
│ A  │ B  │ C  │ D  │
├────┼────┼────┼────┤
│ E  │ F  │ G  │ H  │
└────┴────┴────┴────┘
```

---

## 🏗️ Page Layouts

### Navbar Layout
```
┌─────────────────────────────┐
│ Logo        Menu    Button  │  ← Navbar
└─────────────────────────────┘
```
**Code:** `flex justify-between items-center`

---

### Sidebar Layout
```
┌────────┬────────────────────┐
│        │                    │
│ Side   │   Main Content     │
│ bar    │                    │
│        │                    │
└────────┴────────────────────┘
```
**Code:** `flex` with fixed width sidebar

---

### Header + Content + Footer
```
┌─────────────────────────────┐
│         Header              │  ← Fixed height
├─────────────────────────────┤
│                             │
│       Main Content          │  ← flex-1 (grows)
│                             │
├─────────────────────────────┤
│         Footer              │  ← Fixed height
└─────────────────────────────┘
```
**Code:** `flex flex-col min-h-screen`

---

### Dashboard Layout
```
┌────────┬────────────────────┐
│  Logo  │     Top Navbar     │
├────────┼────────────────────┤
│        │                    │
│ Side   │   Dashboard        │
│ Nav    │   Content          │
│        │                    │
└────────┴────────────────────┘
```

---

## 📱 Responsive Grids

### Mobile (1 column)
```
┌─────────┐
│    A    │
├─────────┤
│    B    │
├─────────┤
│    C    │
└─────────┘
```

### Tablet (2 columns)
```
┌──────┬──────┐
│  A   │  B   │
├──────┼──────┤
│  C   │  D   │
└──────┴──────┘
```

### Desktop (3 columns)
```
┌────┬────┬────┐
│ A  │ B  │ C  │
├────┼────┼────┤
│ D  │ E  │ F  │
└────┴────┴────┘
```

**Code:** `grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3`

---

## 🎯 Centering Techniques

### Horizontal Center
```
┌─────────────────────────────┐
│         [Content]           │
└─────────────────────────────┘
```
**Code:** `mx-auto` or `justify-center`

### Vertical Center
```
┌─────────┐
│         │
│[Content]│
│         │
└─────────┘
```
**Code:** `items-center` in flex

### Perfect Center (Both)
```
┌─────────────┐
│             │
│  [Content]  │
│             │
└─────────────┘
```
**Code:** `flex items-center justify-center`

---

## 📦 Card Layouts

### Basic Card
```
┌─────────────────┐
│  Card Title     │
│                 │
│  Card content   │
│  goes here...   │
│                 │
│     [Button]    │
└─────────────────┘
```

### Card with Image
```
┌─────────────────┐
│                 │
│     IMAGE       │
│                 │
├─────────────────┤
│  Title          │
│  Description    │
│     [Button]    │
└─────────────────┘
```

### Stats Card
```
┌─────────────────┐
│  Total Users    │
│                 │
│     12,543      │
│                 │
│  ↑ 12% increase │
└─────────────────┘
```

---

## 🔢 Spacing Examples

### No Gap
```
[A][B][C][D]
```

### gap-4
```
[A]  [B]  [C]  [D]
```

### gap-8
```
[A]    [B]    [C]    [D]
```

---

## 💡 Quick Reference

| Layout Type | Classes |
|-------------|---------|
| Horizontal flex | `flex flex-row` |
| Vertical flex | `flex flex-col` |
| Center both | `flex items-center justify-center` |
| Space between | `flex justify-between` |
| 3 col grid | `grid grid-cols-3` |
| Sidebar + Main | `flex` with `w-64` + `flex-1` |
| Full height | `min-h-screen` |
| Center block | `max-w-md mx-auto` |

