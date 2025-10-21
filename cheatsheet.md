# 📚 Tailwind CSS Complete Cheatsheet

Quick reference for all Tailwind CSS utilities covered in this tutorial.

---

## 🎨 Colors

```
text-{color}-{shade}      Text color
bg-{color}-{shade}        Background
border-{color}-{shade}    Border color
decoration-{color}        Text decoration color

Colors: gray, red, orange, yellow, green, blue, indigo, purple, pink
Shades: 50, 100, 200, 300, 400, 500, 600, 700, 800, 900
```

---

## 📏 Spacing

```
p-{size}    Padding all sides          m-{size}    Margin all sides
pt-{size}   Padding top                mt-{size}   Margin top
pr-{size}   Padding right              mr-{size}   Margin right
pb-{size}   Padding bottom             mb-{size}   Margin bottom
pl-{size}   Padding left               ml-{size}   Margin left
px-{size}   Padding horizontal         mx-{size}   Margin horizontal
py-{size}   Padding vertical           my-{size}   Margin vertical

Sizes: 0, 0.5, 1, 2, 3, 4, 5, 6, 8, 10, 12, 16, 20, 24, 32, 40, 48, 56, 64

space-x-{size}    Horizontal space between children
space-y-{size}    Vertical space between children
```

---

## 📝 Typography

### Font Size
```
text-xs      12px       text-sm      14px
text-base    16px       text-lg      18px
text-xl      20px       text-2xl     24px
text-3xl     30px       text-4xl     36px
text-5xl     48px       text-6xl     60px
```

### Font Weight
```
font-thin        100      font-normal      400
font-light       300      font-medium      500
font-semibold    600      font-bold        700
font-extrabold   800      font-black       900
```

### Text Alignment & Transform
```
text-left        text-center        text-right
text-justify

uppercase        lowercase          capitalize
normal-case
```

### Text Decoration
```
underline        line-through       no-underline
decoration-solid   decoration-double   decoration-dotted
decoration-dashed  decoration-wavy
decoration-{size}  (1, 2, 4, 8)
```

### Line Height & Letter Spacing
```
leading-none     leading-tight      leading-snug
leading-normal   leading-relaxed    leading-loose

tracking-tighter   tracking-tight     tracking-normal
tracking-wide      tracking-wider     tracking-widest
```

### Text Overflow
```
truncate              Truncate with ellipsis
text-ellipsis         Ellipsis overflow
text-clip             Clip overflow
whitespace-nowrap     No wrap
whitespace-pre        Preserve whitespace
line-clamp-{n}        Clamp to n lines
```

---

## 📍 Position

```
static       relative      absolute      fixed      sticky

top-{size}   right-{size}  bottom-{size}  left-{size}
inset-{size}             All sides
inset-x-{size}           Left & right
inset-y-{size}           Top & bottom

Sizes: 0, 1, 2, 3, 4, 5, 6, 8, 10, 12, 16, 20, ...
      auto, 1/2, 1/3, 1/4, full
```

### Z-Index
```
z-0    z-10   z-20   z-30   z-40   z-50   z-auto
```

### Overflow
```
overflow-auto      overflow-hidden    overflow-visible
overflow-scroll    overflow-clip
overflow-x-auto    overflow-y-hidden  (directional)
```

---

## 📦 Layout & Flexbox

### Display
```
block          inline-block    inline
flex           inline-flex
grid           inline-grid
hidden         (display: none)
```

### Flexbox
```
flex-row         flex-col
flex-row-reverse flex-col-reverse

justify-start    justify-end      justify-center
justify-between  justify-around   justify-evenly

items-start      items-center     items-end
items-baseline   items-stretch

flex-1           flex-auto        flex-none
flex-grow        flex-grow-0
flex-shrink      flex-shrink-0
```

### Gap
```
gap-{size}       Both directions
gap-x-{size}     Horizontal only
gap-y-{size}     Vertical only
```

---

## 🏗️ Grid

```
grid-cols-{n}      Number of columns (1-12)
grid-rows-{n}      Number of rows (1-6)

col-span-{n}       Span n columns
row-span-{n}       Span n rows
col-start-{n}      Start at column n
col-end-{n}        End at column n
row-start-{n}      Start at row n
row-end-{n}        End at row n

grid-flow-row      grid-flow-col      grid-flow-dense
```

---

## 🔲 Sizing

### Width
```
w-0      w-px     w-0.5    w-1      w-2      w-3      w-4...
w-1/2    w-1/3    w-2/3    w-1/4    w-3/4
w-full   w-screen w-min    w-max    w-fit

max-w-xs   max-w-sm   max-w-md   max-w-lg
max-w-xl   max-w-2xl  max-w-full
max-w-screen-sm  max-w-screen-md  ...
```

### Height
```
h-0      h-px     h-full   h-screen h-min    h-max
max-h-screen  max-h-full  min-h-screen  min-h-full
```

### Aspect Ratio
```
aspect-auto      aspect-square    aspect-video
aspect-[4/3]     aspect-[21/9]    (custom)
```

---

## 🎯 Borders

```
border           border-{n}   (0, 2, 4, 8)
border-t         border-r     border-b     border-l
border-x         border-y

rounded          rounded-{size}
rounded-none     rounded-sm     rounded-md
rounded-lg       rounded-xl     rounded-2xl    rounded-3xl
rounded-full

rounded-t-{size}   rounded-r-{size}
rounded-b-{size}   rounded-l-{size}
```

### Divide
```
divide-x         divide-y
divide-{color}   divide-{size}
divide-solid     divide-dashed   divide-dotted
```

---

## 🌟 Shadows

```
shadow-none   shadow-sm     shadow
shadow-md     shadow-lg     shadow-xl     shadow-2xl

drop-shadow-none    drop-shadow-sm    drop-shadow
drop-shadow-lg      drop-shadow-xl    drop-shadow-2xl
```

---

## 🎨 Opacity & Visibility

```
opacity-0     opacity-25    opacity-50
opacity-75    opacity-100

visible       invisible     (visibility)
```

---

## 🖱️ Cursor & User Select

```
cursor-auto      cursor-default    cursor-pointer
cursor-wait      cursor-text       cursor-move
cursor-help      cursor-not-allowed
cursor-none      cursor-grab       cursor-grabbing

select-none      select-text       select-all      select-auto
```

---

## 🔄 Transforms

```
scale-{n}        (0, 50, 75, 90, 95, 100, 105, 110, 125, 150)
scale-x-{n}      scale-y-{n}

rotate-{deg}     (0, 1, 2, 3, 6, 12, 45, 90, 180)
-rotate-{deg}    (negative rotation)

translate-x-{size}    translate-y-{size}
-translate-x-{size}   -translate-y-{size}

skew-x-{deg}     skew-y-{deg}
-skew-x-{deg}    -skew-y-{deg}

origin-center    origin-top       origin-top-right
origin-right     origin-bottom-right
origin-bottom    origin-bottom-left
origin-left      origin-top-left
```

---

## 🎬 Animations

```
animate-none     animate-spin      animate-ping
animate-pulse    animate-bounce
```

---

## ⏱️ Transitions

```
transition-none         transition-all       transition-colors
transition-opacity      transition-shadow    transition-transform

duration-75     duration-100    duration-150
duration-200    duration-300    duration-500
duration-700    duration-1000

delay-75        delay-100       delay-150       delay-200
delay-300       delay-500       delay-700       delay-1000

ease-linear     ease-in         ease-out        ease-in-out
```

---

## 🎭 Filters

```
blur-none    blur-sm      blur      blur-md
blur-lg      blur-xl      blur-2xl  blur-3xl

brightness-0     brightness-50     brightness-75
brightness-100   brightness-125    brightness-150

contrast-0       contrast-50       contrast-75
contrast-100     contrast-125      contrast-150

grayscale-0      grayscale         (black & white)

saturate-0       saturate-50       saturate-100
saturate-150     saturate-200

sepia-0          sepia             (sepia tone)

invert-0         invert            (invert colors)

hue-rotate-0     hue-rotate-15     hue-rotate-30
hue-rotate-60    hue-rotate-90     hue-rotate-180
```

---

## 🪟 Backdrop Filters

```
backdrop-blur-none    backdrop-blur-sm      backdrop-blur
backdrop-blur-md      backdrop-blur-lg      backdrop-blur-xl

backdrop-brightness-{n}    (50, 75, 100, 125, 150)
backdrop-contrast-{n}      (50, 75, 100, 125, 150)
backdrop-grayscale-0       backdrop-grayscale
backdrop-saturate-{n}      (0, 50, 100, 150, 200)
```

---

## 🌈 Gradients

```
bg-gradient-to-t     bg-gradient-to-tr    bg-gradient-to-r
bg-gradient-to-br    bg-gradient-to-b     bg-gradient-to-bl
bg-gradient-to-l     bg-gradient-to-tl

from-{color}-{shade}
via-{color}-{shade}   (optional middle color)
to-{color}-{shade}

Example: bg-gradient-to-r from-blue-500 via-purple-500 to-pink-500
```

---

## 🖼️ Background

```
bg-cover        bg-contain      bg-auto
bg-center       bg-top          bg-bottom
bg-left         bg-right
bg-repeat       bg-no-repeat
bg-fixed        bg-local        bg-scroll

object-cover    object-contain  object-fill
object-none     object-scale-down
object-center   object-top      object-bottom
object-left     object-right
```

---

## 🎯 Interactive States

```
hover:           On mouse hover
focus:           On keyboard/input focus
focus-visible:   On keyboard focus only
focus-within:    When child has focus
active:          When clicking/pressing
disabled:        When disabled
visited:         For visited links

group            Enable group-hover on children
group-hover:     Style when parent is hovered
peer             Enable peer states
peer-checked:    When sibling is checked
peer-focus:      When sibling is focused

first:           First child
last:            Last child
odd:             Odd children
even:            Even children
empty:           When empty

required:        Required form fields
invalid:         Invalid form fields
valid:           Valid form fields
placeholder-shown:  When placeholder is shown
```

---

## 🌙 Dark Mode

```
dark:{utility}   Apply utility in dark mode

Example: bg-white dark:bg-gray-900 text-black dark:text-white
```

---

## ♿ Accessibility

```
sr-only          Screen reader only (visually hidden)
not-sr-only      Not screen reader only
focus:not-sr-only  Show on focus (skip links)

ring-{n}         Focus ring width (0, 1, 2, 4, 8)
ring-{color}     Focus ring color
ring-offset-{n}  Ring offset (0, 1, 2, 4, 8)
ring-opacity-{n} Ring opacity (0-100)
ring-inset       Inset ring

motion-reduce:   Respect reduced motion preference
```

---

## 📦 Container & Layout

```
container        Responsive container with max-width
mx-auto          Center container

columns-{n}      Multi-column layout (1-12)
columns-auto     Auto columns
break-inside-avoid     Avoid breaking inside
break-inside-auto      Allow breaking inside

break-normal     Normal word breaking
break-words      Break long words
break-all        Break at any character
break-keep       Keep words together
```

---

## 🎨 Blend Modes

```
mix-blend-normal      mix-blend-multiply    mix-blend-screen
mix-blend-overlay     mix-blend-darken      mix-blend-lighten
mix-blend-color-dodge mix-blend-color-burn  mix-blend-hard-light
mix-blend-soft-light  mix-blend-difference  mix-blend-exclusion
mix-blend-hue         mix-blend-saturation  mix-blend-color
mix-blend-luminosity

bg-blend-{mode}       Background blend modes (same options)

isolate              Create new stacking context
isolation-auto       Auto isolation
```

---

## 📜 Scroll Features

```
scroll-smooth        Smooth scrolling
scroll-auto          Auto scrolling

snap-none            No scroll snap
snap-x               Horizontal snap
snap-y               Vertical snap
snap-both            Both directions
snap-mandatory       Must snap
snap-proximity       Snap if close

snap-start           Snap to start
snap-end             Snap to end
snap-center          Snap to center
```

---

## 🎯 Special Utilities

```
appearance-none      Remove native styling
appearance-auto      Auto appearance

will-change-auto          will-change-scroll
will-change-contents      will-change-transform

pointer-events-none       Disable pointer events
pointer-events-auto       Enable pointer events

touch-auto          touch-none          touch-pan-x
touch-pan-y         touch-pinch-zoom

resize-none         resize-y            resize-x        resize

accent-{color}      Form control accent color
caret-{color}       Text cursor color

content-none        content-['text']    (for pseudo-elements)
```

---

## 🔧 Arbitrary Values

```
w-[137px]           Custom width
bg-[#1da1f2]        Custom color
text-[17px]         Custom size
rotate-[17deg]      Custom rotation
grid-cols-[200px_1fr_100px]   Custom grid

[&>*]:p-4           All children get padding
[&_p]:text-blue     All p descendants blue

!text-red-500       Force important (override)
```

---

## 📱 Responsive Breakpoints

```
sm:    640px+     Tablets
md:    768px+     Small laptops
lg:    1024px+    Desktops
xl:    1280px+    Large desktops
2xl:   1536px+    Extra large screens

Example: hidden md:block lg:flex
```

---

## 🚀 Common Patterns

### Button
```html
<button class="bg-blue-600 text-white px-6 py-3 rounded-lg font-semibold hover:bg-blue-700 transition">
```

### Card
```html
<div class="bg-white rounded-lg shadow-lg p-6 hover:shadow-2xl transition">
```

### Input
```html
<input class="border border-gray-300 rounded-lg px-4 py-2 w-full focus:outline-none focus:ring-2 focus:ring-blue-500">
```

### Badge
```html
<span class="bg-blue-100 text-blue-800 px-3 py-1 rounded-full text-sm font-semibold">
```

### Center Content
```html
<div class="flex items-center justify-center min-h-screen">
```

### Glass Effect (Backdrop Blur)
```html
<div class="backdrop-blur-md bg-white/20 rounded-lg p-6">
```

### Animated Button
```html
<button class="hover:scale-110 hover:shadow-lg transition-all duration-300">
```

### Group Hover Card
```html
<div class="group">
  <img class="group-hover:scale-110 transition">
  <h3 class="group-hover:text-blue-600 transition">Title</h3>
</div>
```

---

## 💡 Pro Tips

1. **Responsive**: Use mobile-first approach (default → sm: → md: → lg:)
2. **Dark Mode**: Add `dark:` variants for better UX
3. **Transitions**: Always combine `hover:` with `transition` for smooth effects
4. **Group**: Use `group` and `group-hover:` for coordinated hover effects
5. **Peer**: Use `peer` for reactive sibling relationships
6. **Arbitrary Values**: Use `[value]` for custom values: `w-[350px]`
7. **Important**: Use `!` prefix for important: `!text-red-500`

---

## 🎯 Utility Order (Best Practice)

1. Layout & Display (`flex`, `grid`, `block`)
2. Position (`relative`, `absolute`)
3. Sizing (`w-`, `h-`, `max-w-`)
4. Spacing (`p-`, `m-`, `gap-`)
5. Typography (`text-`, `font-`)
6. Colors (`text-`, `bg-`, `border-`)
7. Borders & Shadows (`border`, `rounded`, `shadow`)
8. Effects & Transforms (`opacity`, `scale`, `rotate`)
9. Transitions & Animations (`transition`, `animate-`)
10. Interactive States (`hover:`, `focus:`)
11. Responsive (`md:`, `lg:`)
12. Dark Mode (`dark:`)

Example:
```html
<button class="flex items-center gap-2 px-6 py-3 text-sm font-semibold text-white bg-blue-600 rounded-lg shadow-md hover:bg-blue-700 hover:shadow-lg active:scale-95 transition-all md:px-8 dark:bg-blue-500">
```

---

## 👨‍💻 Created By

**EzGgamingLogan**

Made with ❤️ and Tailwind CSS

[View Full Tutorial](README.md) | [View Full Credits](CREDITS.md)
