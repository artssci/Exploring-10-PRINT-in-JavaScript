# 🎨 Interactive Coding Activity: Exploring *10 PRINT* in JavaScript

👩‍💻 **Goal:** Modify the *10 PRINT* pattern by changing numbers, adding randomness, and experimenting with colors.

## **1️⃣ Run the Code and Observe**
- Open **VS Code**, copy the *10 PRINT* code in a index.html file
- Run the *10 PRINT* code below using **Live Preview**.
- Watch how the pattern is generated on the screen.
- **Reflect:** What do you notice about the pattern? How does it work?

```js
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
  <title>10 Print Program</title>
</head>
<body>
    <script>
const canvas = document.createElement("canvas");
document.body.appendChild(canvas);
const ctx = canvas.getContext("2d");

canvas.width = window.innerWidth;
canvas.height = window.innerHeight;

const tileSize = 20;

function draw() {
  for (let y = 0; y < canvas.height; y += tileSize) {
    for (let x = 0; x < canvas.width; x += tileSize) {
      ctx.beginPath();
      if (Math.random() < 0.5) {
        ctx.moveTo(x, y);
        ctx.lineTo(x + tileSize, y + tileSize);
      } else {
        ctx.moveTo(x + tileSize, y);
        ctx.lineTo(x, y + tileSize);
      }
      ctx.strokeStyle = "black";
      ctx.stroke();
    }
  }
}

draw();

</script>
</body>
</html>

```

---

## **2️⃣ Modify the Grid Size**
- Find this line:  
  ```js
  const tileSize = 20;
  ```
- Change `20` to **10**, **50**, or another number.
- **Reflect:** How does changing `tileSize` affect the pattern?  

---

## **3️⃣ Introduce Randomness to Grid Size**
- Replace `const tileSize = 20;` with:
  ```js
  const tileSize = Math.floor(Math.random() * 40) + 10; // Random size between 10-50
  ```
- **Run the code multiple times** and see how the pattern changes.
- **Reflect:** How does randomness affect the structure of the pattern?

---

## **4️⃣ Add Random Colors**
- Find this line:
  ```js
  ctx.strokeStyle = "black";
  ```
- Replace it with:
  ```js
  ctx.strokeStyle = getRandomColor();
  ```
- **Add this function at the bottom of the script:**
  ```js
  function getRandomColor() {
    const r = Math.floor(Math.random() * 256);
    const g = Math.floor(Math.random() * 256);
    const b = Math.floor(Math.random() * 256);
    return `rgb(${r}, ${g}, ${b})`;
  }
  ```
- **Run the code** and see how each line now has a different color.
- **Reflect:** What happens if we use a fixed color vs. a random one?

---

## **5️⃣ Bonus: Add Randomness to the Line Direction**
- Find this part of the code:
  ```js
  if (Math.random() < 0.5) {
  ```
- Replace `0.5` with a different number (e.g., `0.3` or `0.7`).
- **Reflect:** How does changing this value affect the pattern balance?



This activity helps students **engage deeply** with the code, **experiment freely**, and **reflect on their learning**. 🚀
