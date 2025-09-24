---
layout: post
title:  "Eventos y Condicionales en JavaScript"
date:   2025-09-23 01:00:00 -0300
categories: Sistemas Operativos
background: '/img/posts/bios.jpg'
author: "Mateo Romero"
---

## 🎯 **En este artículo vamos a buscar los siguientes objetivos:**

* Entender qué son los eventos `onclick` y `onmouseover`.
* Aplicar **condicionales (`if`, `else if`, `else`)** para cambiar el comportamiento según la situación.
* Hacer pequeños ejercicios interactivos con botones y elementos HTML.

---

## 🧩 **Parte 1: Eventos en HTML/JS**

Un **evento** es una acción del usuario o del navegador: hacer clic, mover el mouse, presionar una tecla, etc.

Ejemplos:

* `onclick` → cuando el usuario hace clic.
* `onmouseover` → cuando el puntero pasa por encima.
* `onmouseout` → cuando el puntero se va.

### Ejemplo 1: `onclick`

`onclick` es una función propia de los botones, e indica que debe hacer el botón al ser clickeado.
En este caso, al clickear sobre el botón, el mismo cambia el texto en pantalla por el definido dentro del script. Es decir, al hacer click se llama a la función "`cambiarTexto()`" definida en el script.

```html
<p id="texto">Haz clic en el botón</p>
<button onclick="cambiarTexto()">Click aquí</button>

<script>
function cambiarTexto() {
  document.getElementById("texto").textContent = "¡Hiciste clic en el botón!";
}
</script>
```

---

### Ejemplo 2: `onmouseover` y `onmouseout`

En este caso `onmouseover` y `onmouseout`, son acciones que responden cuando se pasa el mouse por encima de un elemento y cuando el mouse deja de estar sobre ese elemento. El navegador, al detectar cualquiera
de los dos casos, llama a las funciones definidas en el script.

```html
<p id="parrafo" onmouseover="cambiarColor()" onmouseout="volverColor()">
  Pasa el mouse por encima de este texto.
</p>

<script>
function cambiarColor() {
  document.getElementById("parrafo").style.color = "red";
}
function volverColor() {
  document.getElementById("parrafo").style.color = "black";
}
</script>
```

---

## 🧩 **Parte 2: Condicionales**

Las **condicionales** permiten que el programa tome decisiones.

Sintaxis básica:

```javascript
if (condicion) {
  // código si la condición es verdadera
} else if (otraCondicion) {
  // código si la otra condición es verdadera
} else {
  // código si ninguna es verdadera
}
```

---

### Ejemplo 3: Uso con input

```html
<input type="number" id="edad" placeholder="Escribe tu edad">
<button onclick="verificarEdad()">Verificar</button>
<p id="resultado"></p>

<script>
function verificarEdad() {
  let valor = document.getElementById("edad").value;

  if (valor >= 18) {
    document.getElementById("resultado").textContent = "Eres mayor de edad ✅";
  } else {
    document.getElementById("resultado").textContent = "Eres menor de edad ❌";
  }
}
</script>
```

---

## 🎲 **Actividades prácticas**

1. Hacer un botón que **cambie el color de fondo** de la página cada vez que lo clickeás.
2. Hacer un párrafo que se ponga en **negrita** cuando pases el mouse por encima y vuelva a la normalidad cuando lo saques.
3. Crear un input donde el usuario escriba un número y al hacer clic en un botón, muestre si el número es **par o impar**.
4. Hacer un mini cuestionario de 1 pregunta con opciones (ej: "¿2+2=4?") y mostrar si la respuesta es correcta o incorrecta.

---

👉 Con esto los alumnos ya pueden:

* Manejar **eventos simples**.
* Usar **condicionales** para tomar decisiones.
* Empezar a crear páginas **interactivas**.

---
