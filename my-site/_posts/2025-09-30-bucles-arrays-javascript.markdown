---
layout: post
title:  "📚 Bucles y Arrays en JavaScript"
date:   2025-09-30 01:00:00 -0300
categories: Javascript
background: '/img/posts/bios.jpg'
author: "Mateo Romero"
---

## En este artículo investigaremos sobre los siguientes temas:
* Comprender qué son los **arrays** y cómo almacenan varios valores en una sola variable.
* Usar **bucles (for, while)** para repetir instrucciones.
* Combinar arrays y bucles en ejemplos prácticos.

---

## 🧩 Arrays

Un **array** es una lista de valores almacenados en una sola variable.

```javascript
let frutas = ["Manzana", "Banana", "Naranja"];
console.log(frutas[0]); // Manzana
console.log(frutas[1]); // Banana
console.log(frutas.length); // 3 (cantidad de elementos)
```

---

## 🧩 Bucles

### 🔹 Bucle `for`

Sirve para repetir una acción un número conocido de veces.

```javascript
for (let i = 0; i < 5; i++) {
  console.log("Repetición número " + i);
}
```

👉 Imprime del 0 al 4.

---

### 🔹 Bucle `while`

Se repite **mientras** una condición sea verdadera.

```javascript
let contador = 1;
while (contador <= 3) {
  console.log("Contador: " + contador);
  contador++;
}
```

---

## 🧩 Arrays con bucles

Recorremos un array usando un bucle `for`.

```javascript
let alumnos = ["Ana", "Juan", "Pedro", "Lucía"];

for (let i = 0; i < alumnos.length; i++) {
  console.log("Alumno: " + alumnos[i]);
}
```




