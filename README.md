# Taller Guiado 2: CSS Moderno y Flexbox

## Objetivo
Transformar la estructura HTML del Taller 1 en un diseño profesional usando CSS moderno, variables CSS, y Flexbox para crear layouts flexibles y atractivos.

## Conceptos Aplicados

### CSS Moderno
- **Variables CSS (Custom Properties)**: Para mantener consistencia en colores, espaciado y tipografía
- **Reset CSS**: Normalización de estilos por defecto del navegador
- **Box-sizing**: border-box para un modelo de caja más predecible
- **Clamp()**: Tipografía responsiva sin media queries

### Flexbox
- **Contenedores flex**: `display: flex` para layouts flexibles
- **Justify-content**: Alineación horizontal de elementos
- **Align-items**: Alineación vertical de elementos
- **Flex-wrap**: Permitir salto de línea en elementos flex
- **Gap**: Espaciado uniforme entre elementos flex

### Efectos Visuales
- **Gradientes**: Fondos y textos con gradientes lineales
- **Sombras**: Box-shadow para profundidad
- **Transiciones**: Animaciones suaves en hover
- **Transform**: Escalado y rotación en interacciones

## Estructura del Proyecto

```
Taller-Guiado-2/
├── index.html          # HTML con enlace a CSS
├── styles.css          # Estilos completos con Flexbox
└── README.md          # Este archivo
```

## Características Implementadas

### 1. Variables CSS
```css
:root {
    --color-primary: #3498db;
    --color-secondary: #2c3e50;
    --spacing-sm: 1rem;
    --spacing-md: 2rem;
    --transition-normal: 0.3s ease;
}
```

### 2. Header con Flexbox
- **Navegación horizontal**: Flex para distribuir elementos
- **Efectos hover**: Transiciones suaves y animaciones
- **Header fijo**: Position fixed con backdrop-filter

### 3. Hero Section
- **Layout flex**: Imagen y texto lado a lado
- **Estadísticas**: Cards con hover effects
- **Botones**: Gradientes y estados hover

### 4. Grid de Proyectos
- **Flexbox responsive**: Flex-wrap para adaptabilidad
- **Cards interactivas**: Hover effects con overlay
- **Imágenes**: Transform scale en hover

### 5. Sección Habilidades
- **Barras de progreso**: Animadas con CSS
- **Layout flex**: Distribución automática de categorías
- **Data attributes**: Para controlar niveles de habilidad

### 6. Formulario de Contacto
- **Layout flex**: Información y formulario lado a lado
- **Estados focus**: Bordes animados en inputs
- **Validación visual**: Estilos para campos requeridos

### 7. Footer
- **Flexbox layout**: Distribución de contenido
- **Enlaces sociales**: Círculos con hover effects
- **Gradiente de fondo**: Consistente con el header

## Técnicas CSS Destacadas

### Flexbox Patterns
```css
/* Centrado perfecto */
.hero {
    display: flex;
    align-items: center;
    justify-content: center;
}

/* Distribución espaciada */
.nav-menu {
    display: flex;
    gap: 2rem;
    justify-content: space-between;
}

/* Cards responsivas */
.proyectos-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 2rem;
    justify-content: center;
}
```

### Efectos Visuales
```css
/* Gradiente en texto */
.highlight {
    background: linear-gradient(45deg, var(--color-primary), var(--color-accent));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

/* Hover con transform */
.proyecto-card:hover {
    transform: translateY(-10px);
    box-shadow: var(--shadow-lg);
}
```

### Variables CSS
```css
/* Definición */
:root {
    --color-primary: #3498db;
    --spacing-md: 2rem;
}

/* Uso */
.elemento {
    color: var(--color-primary);
    padding: var(--spacing-md);
}
```

## Responsive Design

### Flexbox Responsive
- **Flex-wrap**: Elementos se adaptan automáticamente
- **Min-width**: Tamaños mínimos para cards
- **Clamp()**: Tipografía que escala con viewport

### Técnicas Aplicadas
```css
/* Tipografía responsiva */
.hero-title {
    font-size: clamp(2.5rem, 5vw, 4rem);
}

/* Cards responsivas */
.proyecto-card {
    flex: 1;
    min-width: 350px;
    max-width: 400px;
}
```

## Mejores Prácticas

### Organización CSS
1. **Reset y variables** al inicio
2. **Componentes** agrupados por sección
3. **Estados hover** junto a elementos base
4. **Comentarios** para separar secciones

### Performance
- **Transiciones eficientes**: Solo propiedades que no causan reflow
- **Transform vs position**: Usar transform para animaciones
- **Will-change**: Para animaciones complejas

### Accesibilidad
- **Focus visible**: Estados de foco claros
- **Contraste**: Colores con contraste adecuado
- **Hover y focus**: Estados consistentes

## Próximos Pasos

Este CSS será la base para:
- **Taller Guiado 3**: Agregar media queries para responsive completo
- **Taller Guiado 4**: Comparar con frameworks CSS

## Validación

Para validar el CSS:
1. Ir a [W3C CSS Validator](https://jigsaw.w3.org/css-validator/)
2. Subir el archivo `styles.css`
3. Verificar que no hay errores

## Notas para Estudiantes

- **Variables CSS**: Facilitan mantenimiento y consistencia
- **Flexbox**: Ideal para layouts unidimensionales
- **Mobile-first**: Aunque no hay media queries, el diseño es adaptable
- **Performance**: Transiciones suaves mejoran UX

## Recursos Adicionales

- [CSS Flexbox Guide](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [CSS Variables](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties)
- [CSS Transitions](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Transitions)
