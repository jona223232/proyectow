# 🌷 Plan de Ejecución: Proyecto Web "Pageflor" (HTML y CSS)

**Objetivo:** Crear un sitio web elegante, funcional y profesional para un comerciante mayorista de flores, utilizando exclusivamente HTML para la estructura y CSS para el estilo.

## 🏗️ FASE 1: Estructura Inicial y Archivos Base

**Meta:** Establecer la jerarquía de archivos y el esqueleto HTML5.

| Tarea | Archivo / Carpeta | Descripción |
| :--- | :--- | :--- |
| **1.1. Configuración** | `pageflor/` | Crear la carpeta raíz del proyecto. |
| **1.2. Archivos HTML** | `index.html`, `catalogo.html`, `historia.html`, `contacto.html` | Crear los cuatro archivos HTML principales con la estructura mínima (Doctype, `<head>`, `<body>`). |
| **1.3. Estilos** | `pageflor/css/styles.css` | Crear la carpeta `css` y el archivo de estilos principal (`styles.css`). |
| **1.4. Enlace CSS** | Todos los `.html` | Incluir el enlace a `styles.css` en la sección `<head>` de **todas** las páginas. |
| **1.5. Estructura Base** | Todos los `.html` | Definir las etiquetas semánticas: `<header>`, `<nav>`, `<main>`, `<footer>`. |

***

## 📝 FASE 2: Contenido HTML Completo (Estructuración Lógica)

**Meta:** Introducir todo el contenido del negocio y las clases necesarias para el diseño, sin preocuparse por la apariencia visual.

### 2.1. Navegación (`<nav>`)
* **Contenido:** Lista de enlaces (`<ul>`/`<li>`) a las cuatro páginas principales (`index.html`, `catalogo.html`, `historia.html`, `contacto.html`).

### 2.2. Portada (`index.html`)
* **Hero Section:** `<section class="hero">` con un mensaje principal (`<h1>`) sobre la calidad.
* **Intro al Negocio:** `<section class="intro">` con párrafos que destacan el **compromiso y profesionalismo**.
* **CTA:** Botón (`<a href>`) para Catálogo y Contacto.

### 2.3. Página de Catálogo (`catalogo.html`)
* **Grid:** `<section class="catalogo-grid">` como contenedor principal.
* **Tarjetas:** Crear al menos 6 `<article class="flor-card">` simulando productos. Cada tarjeta debe contener: `<h3>` (Nombre), `<img>` (Placeholder para foto), `<p>` (Breve descripción).

### 2.4. Página de Historia (`historia.html`)
* **Trayectoria:** `<section class="trayectoria">` con párrafos sobre el fundador (Daniel) y la dedicación al campo.
* **Valores:** Lista (`<ul class="valores">`) destacando **Confianza, Calidad y Cuidado**.

### 2.5. Página de Contacto (`contacto.html`)
* **Formulario:** `<form class="form-mayorista">` con `<label>` e `<input>` para Nombre, Empresa, Email, Teléfono. Usar `<textarea>` para el mensaje (pedido/volumen).
* **Info:** `<div class="info-contacto">` con lista de dirección, email y teléfono para distribución mayorista.

***

## 🎨 FASE 3: Estilos Globales y Tipografía (CSS Base)

**Meta:** Establecer la base visual: limpieza, elegancia, y tonos naturales.

| Selector CSS | Acciones Específicas de CSS |
| :--- | :--- |
| `*` | Aplicar `margin: 0; padding: 0; box-sizing: border-box;` (Reset Básico). |
| `:root` | **Variables de Color (Elegancia):** Definir `--color-primario` (verde oliva suave), `--color-fondo` (blanco roto/crema), `--color-texto` (gris oscuro). |
| `body` | Establecer una `font-family` **limpia y moderna** (ej. sans-serif) para el **profesionalismo**. Aplicar `--color-fondo` como fondo general. |
| `header, footer` | Aplicar `background-color` suave y `padding` generoso. |
| `nav ul` | **Flexbox:** Usar `display: flex;` para alinear los enlaces horizontalmente; remover `list-style: none;`. |
| `a` | Remover `text-decoration: none;` y definir un color de *hover* sutil. |

***

## 🖼️ FASE 4: Estilos de Componentes (CSS Detallado)

**Meta:** Aplicar los estilos específicos para que las secciones cumplan su propósito visual.

| Clase CSS | Acciones Específicas de CSS |
| :--- | :--- |
| `.hero` | **Vitrina:** Definir `min-height`, usar `background-image` (placeholder) con `background-size: cover`. Centrar el texto principal. |
| `.intro` | Aplicar `padding` y `margin` amplios para dar sensación de **frescura y espacio**. |
| `.catalogo-grid` | **Visualización Amplia:** Usar `display: grid;` con `grid-template-columns` para **3 columnas** en pantallas grandes. Añadir `gap`. |
| `.flor-card` | **Elegancia:** Aplicar un *hover* sutil (ej. ligero `box-shadow`). Asegurar que la imagen sea el foco visual (`img` con `object-fit: cover`). |
| `.form-mayorista` | **Confianza:** Diseño limpio para los *inputs* y *textareas* (bordes suaves, buen *padding*), reflejando profesionalismo. |

***

## 📱 FASE 5: Adaptación a Dispositivos (CSS Responsivo)

**Meta:** Asegurar la funcionalidad en móviles y tabletas.

| Selector CSS | Acciones Específicas de CSS |
| :--- | :--- |
| `@media (max-width: 768px)` | **Punto de Quiebre (Breakpoint):** Usar esta media query para todos los ajustes de *tablet* y móvil. |
| `.catalogo-grid` | Redefinir `grid-template-columns` a **1 o 2 columnas** para asegurar que las fotos de las flores se vean grandes en móvil. |
| `nav ul` | Cambiar `display: flex` a `flex-direction: column` para que la navegación sea vertical. |
| `.trayectoria` | Desactivar cualquier diseño de columna (si se usó `flex`) a favor de un apilamiento vertical (`flex-direction: column`). |
| `body, section` | Reducir el `padding` general para optimizar el uso del espacio en pantallas pequeñas. |