# CSS Position — Notes

## 1) position: static
- The default position type for all elements  
- The element stays in the normal document flow  
- top, left, right, bottom have no effect  

css
.box {
  position: static;
  top: 50px; /* No effect */
}

---

## 2) position: relative

- The element stays in the normal flow
- It moves relative to its original position
- The original space is preserved
- Commonly used as a parent for absolute elements

.box {
  position: relative;
  top: 20px;
  left: 30px;
}

---

## 3) position: absolute

- Removed from the normal document flow
- Positioned relative to the closest positioned ancestor
- If no ancestor has position set, it is positioned relative to the page (body)

.parent {
  position: relative;
}

.child {
  position: absolute;
  top: 10px;
  right: 10px;
}

---

## 4) position: fixed

- Positioned relative to the viewport
- Does not move when the page scrolls
- Useful for floating buttons, fixed headers, side panels

.button {
  position: fixed;
  bottom: 20px;
  right: 20px;
}

---

## 5) position: sticky

- Acts like relative until a certain scroll position
- Once the scroll reaches the defined point, it becomes fixed
- Great for sticky headers and menus

.header {
  position: sticky;
  top: 0;
  background: white;
}
---

Tooltip Example (absolute positioning)

<div class="box">
  Hover me
  <span class="tooltip">Hello!</span>
</div>

.box {
  position: relative;
}

.tooltip {
  position: absolute;
  top: -20px;
  left: 0;
  background: black;
  color: white;
  padding: 4px 8px;
}
