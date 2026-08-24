# 🎨 Cómo Personalizar tu Cuaderno Python

¡Ahora que tienes el proyecto, puedes hacerlo tuyo! Aquí te muestro cómo modificarlo.

## 📝 Cambiar el nombre personalizado

En el archivo `Python Interactivo.html`, busca esta línea (está alrededor de la línea 729):

```javascript
headerLeft.appendChild(el("h1",{}, "¡Hola, Skarlet! 👋"));
```

**Cambia "Skarlet" por tu nombre:**

```javascript
headerLeft.appendChild(el("h1",{}, "¡Hola, Tu Nombre! 👋"));
```

Luego también cambia esta línea (alrededor de la línea 814):

```javascript
finale.appendChild(el("h2",{}, "¡Terminaste el curso, Skarlet!"));
```

Por:

```javascript
finale.appendChild(el("h2",{}, "¡Terminaste el curso, Tu Nombre!"));
```

---

## 🎨 Cambiar los colores

### Encontrar la sección de colores

Busca esta parte al inicio del `<style>` (línea 22):

```css
:root{
  /* Tema Claro (Por defecto) */
  --paper: #FBF7EC;
  --paper-line: #E7DFC8;
  --ink: #2B2A4A;
  --ink-soft: #5B5876;
  --violet: #6C5CE7;
  --violet-dark: #4E3FC4;
  --coral: #FF6B81;
  --mint: #00C9A7;
  --amber: #FFB020;
  --sky: #3DA5D9;
  --lilac: #B983FF;
  --leaf: #2FBF71;
  --code-bg: #211C36;
  --code-text: #EDEBFA;
  --bg-page: #ffffff;
  --bg-opt-hover: #F6F4FF;
}
```

### Cambiar colores individuales

- `--violet`: Color principal (botones, títulos)
- `--mint`: Color de respuestas correctas (verde)
- `--coral`: Color de respuestas incorrectas (rojo)
- `--amber`: Color de puntos (amarillo)
- `--paper`: Fondo general (color papel)
- `--ink`: Color del texto principal (negro)

**Ejemplo:** Para cambiar el color principal de violeta a azul:

```css
--violet: #0066FF; /* Azul en lugar de violeta */
--violet-dark: #0052CC; /* Azul oscuro */
```

### Usar un generador de colores

1. Abre [Color Picker](https://www.google.com/search?q=color+picker)
2. Elige un color
3. Copia el código hexadecimal (#RRGGBB)
4. Pégalo en el archivo

---

## 📚 Agregar una nueva lección

Busca la sección `var MODULES = [` (alrededor de la línea 469).

Verás algo así:

```javascript
var MODULES = [
  {
    id:"intro", emoji:"🐍", title:"¡Bienvenida a Python!",
    explain:"Python es uno de los lenguajes...",
    example: 'print("¡Hola, Skarlet!")',
    exercise:{
      question:'¿Qué crees que hace...',
      options:["Muestra...","Guarda...","Borra...","Le pregunta..."],
      correct:0,
      hint:"Piensa en...",
      explainGood:"print() es..."
    }
  },
  // ... más lecciones
];
```

### Agregar tu propia lección

Copia este bloque y agrégalo ANTES del último `]`:

```javascript
  {
    id:"tu-leccion", emoji:"🚀", title:"Mi Primera Lección",
    explain:"Aquí explicas qué aprenderá el usuario. Puedes usar varias líneas.",
    example: 'print("Ejemplo de código")\nprint("En dos líneas")',
    exercise:{
      question:"¿Qué hace el código?",
      options:["Opción 1","Opción 2","Opción 3","Opción 4"],
      correct:0, // El índice de la respuesta correcta (0, 1, 2, o 3)
      hint:"Una pista para ayudar al usuario.",
      explainGood:"Aquí explicas por qué esa es la respuesta correcta."
    }
  }
```

### Explicación de cada campo

- `id`: Nombre único (sin espacios ni mayúsculas)
- `emoji`: Un emoji del tema
- `title`: Nombre de la lección
- `explain`: Texto explicativo
- `example`: Código de ejemplo (usa `\n` para saltos de línea)
- `question`: La pregunta del ejercicio
- `options`: Array con 4 opciones de respuesta
- `correct`: Índice de la respuesta correcta (0, 1, 2, o 3)
- `hint`: Pista si el usuario la pide
- `explainGood`: Explicación de por qué es correcta

---

## 🎯 Cambiar los puntos por lección

Busca esta línea (alrededor de la línea 650):

```javascript
state.points += 10; // Suma 10 puntos
```

Cambia `10` por el número que quieras (ejemplo: `25`):

```javascript
state.points += 25; // Ahora suma 25 puntos
```

---

## 💬 Cambiar los mensajes de felicitación

Busca estas líneas (línea 568):

```javascript
var GOOD_MSG = ["¡Exacto! 🎉","¡Perfecto! 🐍","¡Así se hace! ✨","¡Lo lograste! 🚀","¡Correcto, vas genial! 🌟"];
```

Puedes agregar más mensajes o cambiar los existentes:

```javascript
var GOOD_MSG = ["¡Genial! ⭐","¡Eres increíble! 🌟","¡Lo clavaste! 🎯","¡Así se hace! 💪"];
```

---

## 🎨 Cambiar emojis de las lecciones

En cada módulo, cambia el `emoji`:

```javascript
{
  id:"intro", emoji:"🐍", title:"¡Bienvenida a Python!",
  // Cambiar 🐍 por otro emoji: 🚀, ⭐, 💡, 🔥, etc.
```

---

## 📱 Cambiar el título de la página

En la sección `<head>`, busca:

```html
<title>Python Interactivo — Cuaderno de código</title>
```

Cámbialo por:

```html
<title>Mi Cuaderno Python - Por [Tu Nombre]</title>
```

---

## 🌙 Personalizar tema oscuro

En la sección de estilos, busca `body.dark-theme`:

```css
body.dark-theme {
  --paper: #1a1a24;
  --paper-line: #2d2d3d;
  --ink: #e0e0e8;
  --ink-soft: #a0a0b0;
  --bg-page: #252533;
  --bg-opt-hover: #36364a;
  --code-bg: #11111a;
}
```

Puedes cambiar estos colores para personalizar cómo se ve en modo oscuro.

---

## 💾 Guardar tus cambios

1. Abre el archivo con un editor de texto (VS Code, Notepad++)
2. Realiza los cambios
3. Presiona **Ctrl + S** (o **Cmd + S** en Mac)
4. Recarga la página en el navegador (F5)
5. ¡Verás tus cambios!

---

## 🐛 Consejos para evitar errores

- **No borres comas:** Cada elemento del array necesita una coma después (excepto el último)
- **Cuida las comillas:** Usa comillas simples `'` dentro de `''` y dobles `"` dentro de `""`
- **Indenta correctamente:** Esto ayuda a leer el código
- **Haz copias de seguridad:** Antes de hacer cambios grandes, haz una copia del archivo
- **Abre la consola:** Presiona F12 en el navegador para ver errores

---

## ✅ Ejemplos prácticos

### Ejemplo 1: Cambiar color principal a rojo

Busca:
```css
--violet: #6C5CE7;
--violet-dark: #4E3FC4;
```

Cambia por:
```css
--violet: #FF0000;
--violet-dark: #CC0000;
```

### Ejemplo 2: Agregar 2 nuevas lecciones

Duplica un bloque de `{...}` dentro de `MODULES`, cambia `id`, `title`, `emoji`, etc.

### Ejemplo 3: Aumentar puntos a 50 por lección

Busca:
```javascript
state.points += 10;
```

Cambia por:
```javascript
state.points += 50;
```

---

## 🚀 ¡Diviértete personalizando!

Este es TU proyecto. No tengas miedo de experimentar. Si algo sale mal:
1. Cierra sin guardar
2. O vuelve a descargar el archivo original

¡Buena suerte! 🎓✨
