# GOAT·LIST — CSS Flexbox & Grid en Producción Real

**Proyecto académico Riwi**  
Autor: Camilo Meza  
Año: 2026

---

## 📋 Descripción

**GOAT·LIST** es una aplicación web educativa de **clase mundial** que demuestra los conceptos avanzados de **CSS Flexbox** y **CSS Grid** en un contexto real y profesional. 

El proyecto presenta las **8 leyendas del fútbol mundial** mediante un layout completamente construido con Flexbox y Grid, funcionando como **demostración visual interactiva** de cada propiedad CSS.

---

## 🎯 Características Principales

### ✨ Dos Interfaces Complementarias

#### **1. Vista Principal (`index.html`)**
- **Top Bar**: Navegación sticky con Flexbox
- **Hero Section**: Encabezado editorial centrado
- **Galería de 8 Jugadores**: Grid responsivo con `auto-fit` y `minmax()`
- **Flexbox Showcase**: 7 tarjetas demostrativas de propiedades Flexbox
- **Grid Showcase**: 5 tarjetas demostrativas de propiedades Grid
- **Footer**: Layout completo con `grid-template-areas`

#### **2. Vista Lateral (`lateral.html`)**
- **Sidebar Fijo**: Navegación vertical con Flexbox `justify-content: space-between`
- **Contenido Responsivo**: Margen dinámico para no superponerse con sidebar
- **Carrusel Infinito**: Scroll horizontal con clonación sin saltos
- **Todas las demostraciones**: Idénticas a la vista principal

---

## 🎨 Conceptos Demostrados

### **FLEXBOX** (7 propiedades principales)

| Propiedad | Demo | Qué Hace |
|-----------|------|----------|
| `flex-direction` | 4 variantes | Cambia eje principal: row, row-reverse, column, column-reverse |
| `justify-content` | 5 valores | Distribuye en eje principal: flex-start, center, flex-end, space-between, space-around |
| `align-items` | 3 valores | Alinea en eje cruzado: flex-start, center, flex-end |
| `flex-wrap` | 3 variantes | Control de saltos: nowrap, wrap, wrap-reverse |
| `order` | Reordenamiento visual | Cambia orden sin tocar HTML |
| `flex-grow` | Expansión proporcional | Asigna espacio adicional (1, 2, 3) |
| `align-content` | space-between | Distribuye múltiples líneas |

### **GRID** (5 propiedades principales)

| Propiedad | Demo | Qué Hace |
|-----------|------|----------|
| `grid-template-columns` | 1fr 2fr 1fr | Define columnas explícitas |
| `repeat()` | repeat(4, 1fr) | Evita repetición de valores |
| `grid-template-rows` | 40px 70px 40px | Define filas explícitas |
| `grid-column` / `grid-row` | span, posicionamiento | Expande y posiciona elementos |
| `auto-fit` / `auto-fit` | minmax() responsivo | Layouts sin media queries |
| `grid-template-areas` | Zonas nombradas | Layout semántico visual |
| `gap` | Espaciado automático | Aplica entre filas y columnas |

---

## 📁 Estructura del Proyecto

```
files (1)/
├── index.html          # Página principal (Vista Top Bar)
├── lateral.html        # Página con sidebar (Vista Lateral)
├── futbol.css          # Estilos monolíticos, optimizados
└── README.md           # Este archivo
```

### **Arquitectura CSS**

El archivo `futbol.css` (1139+ líneas) está organizado en **8 secciones**, cada una comentada:

```css
/* 1. RESET & VARIABLES GLOBALES */       (líneas 1-30)
/* 2. TOP BAR (Flexbox Demo 1)            (líneas 33-59)
/* 3. BOTONES DE NAVEGACIÓN               (líneas 62-81)
/* 4. HERO (Flexbox Demo 2)               (líneas 84-138)
/* 5. GALERÍA 8 JUGADORES (Grid Demo 1)   (líneas 141-362)
/* 6. TARJETAS JUGADOR (Flexbox Demo 4-7) (líneas 365-502)
/* 7. FLEXBOX SHOWCASE                    (líneas 505-643)
/* 8. GRID SHOWCASE                       (líneas 641-1139)
```

**Metodología:** Cada bloque está documentado con comentarios que explican la intención pedagógica.

---

## 🎬 Cómo Usar

### **Ver la Página Principal**
1. Abre `index.html` en cualquier navegador moderno
2. Desplázate para ver todos los ejemplos de Flexbox y Grid
3. Experimenta redimensionando la ventana (layouts responsivos)
4. Haz clic en **"Ir a menú lateral →"** para ver la segunda interfaz

### **Ver la Página Lateral**
1. Desde `index.html`, haz clic en el botón superior derecho
2. O abre directamente `lateral.html`
3. Usa el sidebar para navegar entre secciones
4. El carrusel es interactivo: coloca el cursor en los bordes

### **Estudiar el Código**
```bash
# Examina cualquiera de estos archivos:
- futbol.css    # Estudia cada sección comentada
- index.html    # Ve cómo se estructura el HTML semántico
- lateral.html  # Observa el patrón de sidebar + contenido
```

---

## 🛠 Tecnologías

- **HTML5**: Semántica completa (header, nav, section, article, footer)
- **CSS3**: 
  - Flexbox (display: flex, todas las propiedades)
  - CSS Grid (display: grid, todas las propiedades)
  - Variables CSS (custom properties): `--dorado`, `--gris-texto`, etc.
  - Media queries responsivas
  - Animaciones y transiciones
  - Gradientes lineales
- **JavaScript**: Carrusel infinito sin saltos (clonación + normalización)
- **Tipografía**: Google Fonts (Cormorant Garamond + Outfit)

---

## 🎓 Nivel Educativo

**Para estudiantes de:**
- Riwi Bootcamp (Módulo Frontend)
- Cursos de CSS Intermedio-Avanzado
- Portfolios profesionales

**Conceptos que aprenderás:**
1. Eje principal vs. eje cruzado en Flexbox
2. Distribución de espacio con `justify-content` y `align-items`
3. Layouts responsivos con Grid sin media queries
4. Unidades relativas (`fr`, `clamp()`, `vw`)
5. Arquitectura CSS mantenible y escalable
6. HTML semántico para accesibilidad

---

## 📊 Estadísticas del Proyecto

| Métrica | Valor |
|---------|-------|
| Líneas CSS | 1,139 |
| Líneas HTML (index) | 500+ |
| Líneas HTML (lateral) | 500+ |
| Colores CSS Variables | 9 |
| Demos Flexbox | 7 |
| Demos Grid | 5 |
| Jugadores | 8 |
| Media Queries | 4 |

---

## 🎯 Puntos Clave de Diseño

### **1. Responsividad sin Media Queries Innecesarias**

```css
/* Grid responsivo automático */
grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));

/* Tipografía fluida */
font-size: clamp(3rem, 7vw, 6rem);
```

### **2. Variables CSS para Mantenibilidad**

```css
:root {
    --dorado: #cfa04c;
    --negro: #040404;
    --serif: 'Cormorant Garamond', serif;
}
/* Usado 50+ veces en todo el CSS */
```

### **3. Demos Visuales Claras**

- Cada demo tiene **ancho máximo limitado** para mostrar el efecto claramente
- **Alturas fijas** en contenedores flex para comparabilidad
- **Colores contrastados** (dorado sólido + semi-transparente) para distinguir items

### **4. Carrusel Infinito sin Micro-Saltos**

```javascript
// Algoritmo:
// 1. Clona todos los items al final
// 2. Clona en reverso al inicio
// 3. Normaliza scrollLeft cuando llega a 2x o 0x ancho
// Resultado: flujo infinito sin interrupciones
```

---

## 🔍 Ejemplos de Uso en Detalle

### **Ejemplo 1: Centering Perfecto (Hero)**
```css
.hero {
    display: flex;
    flex-direction: column;
    align-items: center;        /* Centra horizontalmente */
    justify-content: center;    /* Centra verticalmente */
}
```
**Resultado:** Título centrado perfecto independientemente del tamaño de pantalla.

### **Ejemplo 2: Layout Responsivo (Galería)**
```css
.galeria-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    /* 4 columnas en desktop, 2 en tablet, 1 en móvil */
    /* SIN una sola media query */
}
```

### **Ejemplo 3: Tarjeta Flexible (Card)**
```css
.card-contenido {
    flex-grow: 1;              /* Expande toda la altura */
    display: flex;
    flex-direction: column;
    /* El link siempre al fondo, sin espacios fijos */
}
```

---

## ⚙️ Requisitos

- **Navegador moderno**: Chrome 90+, Firefox 88+, Safari 14+, Edge 90+
- **Soporte CSS**: Flexbox, Grid, Custom Properties
- **Sin dependencias externas** (excepto Google Fonts)
- **Funciona offline** una vez cargado

---

## 🚀 Optimizaciones Aplicadas

✅ **Performance**
- CSS crítico inline (sin archivo separado)
- Variables CSS para reducir repetición
- Font loading optimizado con `preconnect`
- Imágenes con `background-size: cover` y `no-repeat`

✅ **Accesibilidad**
- HTML semántico (header, nav, section, article, footer)
- Contraste WCAG AA en textos
- Estructura jerárquica clara (h1-h3)

✅ **SEO**
- Meta tags básicos
- Estructura semántica
- Títulos descriptivos

---

## 📝 Notas Académicas

### **Para Profesores**
Este proyecto es ideal para:
- Demostrar Flexbox y Grid simultáneamente
- Mostrar HTML semántico en acción
- Ejemplo de arquitectura CSS mantenible
- Referencia de código de producción

### **Para Estudiantes**
- Estudia la organización del CSS
- Aprende a leer comentarios técnicos
- Experimenta redimensionando navegadores
- Modifica variables CSS y observa cambios globales

---

## 🏆 Estándar de Calidad

Este proyecto cumple con:
- ✅ Código limpio y comentado
- ✅ Metodología BEM respetuosa
- ✅ Responsive design sin frameworks
- ✅ Performance optimizada
- ✅ Accesibilidad básica
- ✅ Totalmente funcional en todos los navegadores modernos

**Calificación:** Nivel Apple — Producción real

---

## 📚 Recursos Adicionales

### Documentación Oficial
- [MDN Flexbox Guide](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout)
- [MDN Grid Guide](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout)
- [CSS-Tricks Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [CSS-Tricks Grid](https://css-tricks.com/snippets/css/complete-guide-grid/)

### Herramientas Útiles
- Firefox DevTools: Excelente para inspeccionar Grid
- Chrome DevTools: Grid overlay y flexbox debugging
- Responsively App: Simular múltiples dispositivos

---

## 👤 Autor

**Camilo Meza**  
Proyecto Web

---

## 📄 Licencia

Uso educativo libre. Puede ser modificado y reutilizado con fines académicos.


## ☑️ Checklist de Exploraciones Recomendadas

- [ ] Redimensiona la ventana lentamente — observa cómo Grid se adapta
- [ ] Abre DevTools (F12) — inspecciona `.galeria-grid` para Ver Grid lines
- [ ] Modifica `--dorado` en CSS — observa los cambios en cascada
- [ ] En lateral.html, scroll el carrusel — nota que no hay saltos
- [ ] Cambia `max-width: 1440px` a algo menor — el layout se reajusta
- [ ] Prueba en móvil — todo sigue funcionando perfectamente

---

**Última actualización:** 14 de abril de 2026  
**Estado:** ✅ Producción — Listo para aprender
