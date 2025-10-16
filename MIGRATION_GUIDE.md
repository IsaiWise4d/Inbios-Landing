# 📋 Ejemplos de Migración a Design System

## Antes y Después de Usar Variables

### Header Component

#### ❌ ANTES (Hardcoded values)
```html
<header class="fixed top-6 left-0 right-0 z-50 px-4">
  <nav class="bg-black/80 backdrop-blur-xl rounded-full border border-white/10 
              shadow-2xl shadow-black/50 px-8 py-4 
              hover:shadow-[0_20px_60px_-15px_rgba(212,175,55,0.3)]">
    
    <a href="/" class="text-white/80 hover:text-[#D4AF37] transition-colors duration-300">
      Inicio
    </a>
    
    <button class="px-6 py-2.5 bg-gradient-to-r from-[#D4AF37] to-[#F4D03F] 
                   text-black font-semibold rounded-full">
      Contáctanos
    </button>
  </nav>
</header>
```

#### ✅ DESPUÉS (Con variables)
```html
<header class="fixed top-[--spacing-lg] left-0 right-0 z-[--z-fixed] px-[--spacing-md]">
  <nav class="glass-effect rounded-[--radius-full] 
              shadow-[--shadow-2xl] 
              px-[--spacing-xl] py-[--spacing-md] 
              hover:shadow-[--shadow-gold-soft] 
              transition-shadow duration-[--transition-base]">
    
    <a href="/" class="text-[--color-text-secondary] 
                       hover:text-[--color-primary] 
                       transition-colors duration-[--transition-base]">
      Inicio
    </a>
    
    <button class="px-[--spacing-xl] py-[--spacing-md] 
                   gradient-gold 
                   text-[--color-background] 
                   font-[--font-weight-semibold] 
                   rounded-[--radius-full]
                   shadow-[--shadow-gold]
                   hover:scale-105
                   transition-transform duration-[--transition-base]">
      Contáctanos
    </button>
  </nav>
</header>
```

### Beneficios
- ✅ **Mantenibilidad**: Cambiar el color dorado en un solo lugar
- ✅ **Consistencia**: Todos los componentes usan los mismos valores
- ✅ **Legibilidad**: Nombres descriptivos en lugar de valores hex
- ✅ **Escalabilidad**: Fácil agregar dark mode o temas

---

## Footer Component

#### ❌ ANTES
```html
<footer class="bg-black/95 backdrop-blur-sm px-6 py-8">
  <h3 class="text-sm font-semibold text-[#D4AF37] mb-2">Contacto</h3>
  <a href="#" class="text-xs text-gray-300 hover:text-[#D4AF37]">
    Email
  </a>
</footer>
```

#### ✅ DESPUÉS
```html
<footer class="bg-[--color-background]/95 backdrop-blur-sm 
               px-[--spacing-xl] py-[--spacing-2xl]">
  <h3 class="text-[--font-size-sm] 
             font-[--font-weight-semibold] 
             text-[--color-primary] 
             mb-[--spacing-sm]">
    Contacto
  </h3>
  <a href="#" class="text-[--font-size-xs] 
                     text-[--color-text-secondary] 
                     hover:text-[--color-primary]
                     transition-colors duration-[--transition-base]">
    Email
  </a>
</footer>
```

---

## Cards / Productos

#### ❌ ANTES
```html
<div class="bg-white/5 rounded-2xl p-6 border border-white/10 
            hover:shadow-[0_0_30px_rgba(212,175,55,0.6)]">
  <h3 class="text-2xl font-bold text-white mb-4">Producto</h3>
  <p class="text-sm text-gray-400">Descripción</p>
  <button class="mt-4 px-6 py-3 bg-[#D4AF37] text-black rounded-full">
    Ver más
  </button>
</div>
```

#### ✅ DESPUÉS
```html
<div class="bg-white/5 
            rounded-[--radius-2xl] 
            p-[--spacing-xl] 
            border border-white/10 
            hover:shadow-[--shadow-gold]
            transition-shadow duration-[--transition-base]">
  <h3 class="text-[--font-size-2xl] 
             font-[--font-weight-bold] 
             text-[--color-text-primary] 
             mb-[--spacing-md]">
    Producto
  </h3>
  <p class="text-[--font-size-sm] text-[--color-text-muted]">
    Descripción
  </p>
  <button class="mt-[--spacing-md] 
                 px-[--spacing-xl] 
                 py-[--spacing-lg] 
                 bg-[--color-primary] 
                 text-[--color-background] 
                 rounded-[--radius-full]
                 font-[--font-weight-semibold]
                 hover:bg-[--color-primary-dark]
                 transition-colors duration-[--transition-base]">
    Ver más
  </button>
</div>
```

---

## Hero Section

#### ❌ ANTES
```html
<section class="min-h-screen pt-32 pb-16">
  <h1 class="text-6xl font-extrabold text-white mb-6">
    <span class="bg-gradient-to-r from-[#D4AF37] to-[#F4D03F] 
                 bg-clip-text text-transparent">
      INBIOS
    </span>
  </h1>
  <p class="text-xl text-gray-300 mb-8">
    Soluciones biomédicas innovadoras
  </p>
</section>
```

#### ✅ DESPUÉS
```html
<section class="min-h-screen pt-[--spacing-3xl] pb-[--spacing-2xl]">
  <h1 class="text-[--font-size-6xl] 
             font-[--font-weight-extrabold] 
             text-[--color-text-primary] 
             mb-[--spacing-xl]">
    <span class="text-gradient">
      INBIOS
    </span>
  </h1>
  <p class="text-[--font-size-xl] 
            text-[--color-text-secondary] 
            mb-[--spacing-2xl]">
    Soluciones biomédicas innovadoras
  </p>
</section>
```

---

## Quick Reference - Conversión Común

| Antes | Después |
|-------|---------|
| `text-[#D4AF37]` | `text-[--color-primary]` |
| `bg-black` | `bg-[--color-background]` |
| `text-gray-300` | `text-[--color-text-secondary]` |
| `px-6` | `px-[--spacing-xl]` |
| `rounded-full` | `rounded-[--radius-full]` |
| `shadow-xl` | `shadow-[--shadow-xl]` |
| `duration-300` | `duration-[--transition-base]` |
| `text-2xl` | `text-[--font-size-2xl]` |
| `font-bold` | `font-[--font-weight-bold]` |

---

## 🎯 Checklist de Migración

- [ ] Reemplazar colores hex por variables CSS
- [ ] Usar variables de espaciado en lugar de valores fijos
- [ ] Aplicar clases utility personalizadas (`.text-gradient`, `.glass-effect`)
- [ ] Usar variables de transición
- [ ] Reemplazar z-index por variables
- [ ] Unificar border-radius con variables
- [ ] Aplicar sombras consistentes

---

## 💡 Tips

1. **Buscar y reemplazar masivo**: Usa tu editor para buscar `#D4AF37` y reemplazar por `--color-primary`
2. **Verifica visualmente**: Después de cambiar, asegúrate que todo se vea igual
3. **Documenta cambios custom**: Si necesitas un valor especial, agrégalo a `global.css`
4. **Testing responsive**: Verifica que las variables funcionen en todos los breakpoints
