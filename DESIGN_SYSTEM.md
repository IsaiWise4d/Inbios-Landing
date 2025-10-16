# 🎨 INBIOS Design System

Sistema de diseño completo para el proyecto INBIOS con variables personalizadas de Tailwind CSS.

---

## 📋 Tabla de Contenidos

1. [Colores](#-colores)
2. [Tipografía](#-tipografía)
3. [Espaciados](#-espaciados)
4. [Bordes y Radios](#-bordes-y-radios)
5. [Sombras](#-sombras)
6. [Ejemplos de Uso](#-ejemplos-de-uso)

---

## 🎨 Colores

### Colores Principales
```css
--color-primary: #D4AF37        /* Dorado INBIOS */
--color-primary-light: #F4D03F  /* Dorado Claro */
--color-primary-dark: #B8941F   /* Dorado Oscuro */
```

**Uso en Tailwind:**
```html
<div class="bg-[--color-primary]">
<p class="text-[--color-primary]">
<button class="border-[--color-primary]">
```

### Colores de Fondo
```css
--color-background: #000000           /* Negro Principal */
--color-background-secondary: #0A0A0A /* Negro Secundario */
--color-surface: #1A1A1A              /* Superficie */
```

### Colores de Texto
```css
--color-text-primary: #FFFFFF    /* Texto Principal */
--color-text-secondary: #E5E5E5  /* Texto Secundario */
--color-text-muted: #9CA3AF      /* Texto Apagado */
--color-text-disabled: #6B7280   /* Texto Deshabilitado */
```

### Colores de Estado
```css
--color-success: #10B981   /* Verde - Éxito */
--color-warning: #F59E0B   /* Amarillo - Advertencia */
--color-error: #EF4444     /* Rojo - Error */
--color-info: #3B82F6      /* Azul - Información */
```

---

## 📝 Tipografía

### Familias de Fuentes
```css
--font-sans: system-ui, sans-serif  /* Fuente Principal */
--font-serif: Georgia, serif        /* Fuente Serif */
--font-mono: 'Fira Code', monospace /* Fuente Monoespaciada */
```

**Uso:**
```html
<p class="font-[family-name:--font-sans]">
```

### Tamaños de Fuente
| Variable | Tamaño | Uso Recomendado |
|----------|--------|-----------------|
| `--font-size-xs` | 12px | Notas, detalles pequeños |
| `--font-size-sm` | 14px | Texto secundario, labels |
| `--font-size-base` | 16px | Texto principal del cuerpo |
| `--font-size-lg` | 18px | Texto destacado |
| `--font-size-xl` | 20px | Subtítulos pequeños |
| `--font-size-2xl` | 24px | Subtítulos |
| `--font-size-3xl` | 30px | Títulos de sección |
| `--font-size-4xl` | 36px | Títulos principales |
| `--font-size-5xl` | 48px | Hero titles |
| `--font-size-6xl` | 60px | Títulos extra grandes |

**Uso:**
```html
<h1 class="text-[--font-size-5xl]">
<p class="text-[--font-size-base]">
```

### Pesos de Fuente
```css
--font-weight-light: 300      /* Ligera */
--font-weight-normal: 400     /* Normal */
--font-weight-medium: 500     /* Media */
--font-weight-semibold: 600   /* Semi-negrita */
--font-weight-bold: 700       /* Negrita */
--font-weight-extrabold: 800  /* Extra negrita */
```

---

## 📏 Espaciados

| Variable | Tamaño | Uso |
|----------|--------|-----|
| `--spacing-xs` | 4px | Espacios mínimos |
| `--spacing-sm` | 8px | Espacios pequeños |
| `--spacing-md` | 16px | Espacios estándar |
| `--spacing-lg` | 24px | Espacios grandes |
| `--spacing-xl` | 32px | Espacios extra grandes |
| `--spacing-2xl` | 48px | Separación de secciones |
| `--spacing-3xl` | 64px | Separación máxima |

**Uso:**
```html
<div class="p-[--spacing-md]">
<div class="gap-[--spacing-lg]">
<section class="mb-[--spacing-3xl]">
```

---

## 🔲 Bordes y Radios

### Border Radius
```css
--radius-sm: 4px      /* Botones pequeños */
--radius-md: 8px      /* Cards, inputs */
--radius-lg: 12px     /* Cards grandes */
--radius-xl: 16px     /* Modales */
--radius-2xl: 24px    /* Elementos especiales */
--radius-full: 9999px /* Círculos, pills */
```

**Uso:**
```html
<button class="rounded-[--radius-full]">
<div class="rounded-[--radius-xl]">
```

---

## 🌟 Sombras

### Sombras Estándar
```css
--shadow-sm: Small shadow
--shadow-md: Medium shadow
--shadow-lg: Large shadow
--shadow-xl: Extra large shadow
--shadow-2xl: Double extra large shadow
```

### Sombras Personalizadas
```css
--shadow-gold: 0 0 30px rgba(212, 175, 55, 0.6)
--shadow-gold-soft: 0 20px 60px -15px rgba(212, 175, 55, 0.3)
```

**Uso:**
```html
<div class="shadow-[--shadow-gold]">
```

---

## 🎯 Ejemplos de Uso

### Botón Dorado Principal
```html
<button class="
  bg-gradient-to-r from-[--color-primary] to-[--color-primary-light]
  text-[--color-background]
  font-[--font-weight-semibold]
  text-[--font-size-base]
  px-[--spacing-xl]
  py-[--spacing-md]
  rounded-[--radius-full]
  shadow-[--shadow-gold]
  hover:scale-105
  transition-transform duration-[--transition-base]
">
  Contáctanos
</button>
```

### Card con Glass Effect
```html
<div class="
  glass-effect
  p-[--spacing-xl]
  rounded-[--radius-2xl]
  shadow-[--shadow-xl]
">
  <h3 class="text-[--font-size-2xl] text-[--color-primary] font-[--font-weight-bold]">
    Título
  </h3>
  <p class="text-[--font-size-base] text-[--color-text-secondary]">
    Contenido
  </p>
</div>
```

### Texto con Gradiente
```html
<h1 class="text-gradient text-[--font-size-5xl] font-[--font-weight-extrabold]">
  INBIOS
</h1>
```

---

## 🔧 Transiciones

```css
--transition-fast: 150ms   /* Hover rápido */
--transition-base: 300ms   /* Transición estándar */
--transition-slow: 500ms   /* Animaciones lentas */
```

**Uso:**
```html
<div class="transition-all duration-[--transition-base]">
```

---

## 📚 Z-Index

```css
--z-base: 0           /* Contenido base */
--z-dropdown: 10      /* Dropdowns */
--z-sticky: 20        /* Elementos sticky */
--z-fixed: 30         /* Header, footer fijos */
--z-modal-backdrop: 40 /* Fondo de modales */
--z-modal: 50         /* Modales */
--z-popover: 60       /* Popovers */
--z-tooltip: 70       /* Tooltips */
```

---

## 🎨 Clases Utility Personalizadas

### `.text-gradient`
Aplica un gradiente dorado al texto.

```html
<h1 class="text-gradient">Texto con gradiente</h1>
```

### `.glass-effect`
Aplica efecto glassmorphism con blur.

```html
<div class="glass-effect p-6">Contenido</div>
```

### `.hover-lift`
Efecto de elevación al hacer hover.

```html
<div class="hover-lift">Se eleva al hover</div>
```

### `.gradient-gold`
Background con gradiente dorado.

```html
<div class="gradient-gold p-4">Fondo dorado</div>
```

---

## 📱 Breakpoints (Tailwind)

- `sm`: 640px
- `md`: 768px
- `lg`: 1024px
- `xl`: 1280px
- `2xl`: 1536px

---

## ✅ Mejores Prácticas

1. **Usa variables en lugar de valores hardcoded**
   ```html
   <!-- ❌ Evitar -->
   <div class="bg-[#D4AF37]">
   
   <!-- ✅ Mejor -->
   <div class="bg-[--color-primary]">
   ```

2. **Mantén consistencia con los espaciados**
   ```html
   <!-- ✅ Usar variables de espaciado -->
   <div class="p-[--spacing-lg] gap-[--spacing-md]">
   ```

3. **Reutiliza las clases utility personalizadas**
   ```html
   <!-- ✅ Usar utilities -->
   <h1 class="text-gradient">Título</h1>
   ```

4. **Combina variables con Tailwind**
   ```html
   <button class="
     bg-[--color-primary]
     hover:bg-[--color-primary-dark]
     transition-colors
     duration-[--transition-base]
   ">
   ```

---

## 🚀 Próximos Pasos

- [ ] Agregar más variantes de color para estados
- [ ] Crear componentes reutilizables
- [ ] Documentar patrones de diseño comunes
- [ ] Agregar animaciones personalizadas

---

**Mantenido por:** Equipo INBIOS  
**Última actualización:** Octubre 2025
