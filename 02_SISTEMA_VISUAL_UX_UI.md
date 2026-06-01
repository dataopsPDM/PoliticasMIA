# 🎨 Sistema Visual, UX/UI y Branding (Estándar Plug & Play)

Este documento define las bases estéticas obligatorias para todas las aplicaciones y micro-servicios creados bajo el ecosistema de **Prodeman**. Todo nuevo proyecto debe acoplarse visualmente para garantizar una transición transparente ("seamless") desde **PortalUnico** hacia la aplicación de destino.

## 💎 Concepto Visual: Glassmorphism Premium
El estilo principal adoptado en toda la corporación es el **Glassmorphism**. La aplicación no debe sentirse como una web plana, sino como una interfaz moderna, limpia y profunda.

**Características del Cristal:**
*   **Transparencia**: Fondos semi-transparentes sobre layouts dinámicos o fondos oscuros (`rgba`).
*   **Blur**: Fuerte desenfoque de fondo (`backdrop-filter: blur(12px)`).
*   **Bordes Claros**: Bordes sutiles para simular el canto iluminado del cristal (Ej: `border-white/10`).
*   **Elevación**: Sombras profundas pero suaves, evitando contornos duros.

## 🎨 Paleta de Colores Corporativa
*   **Color Primario**: `#8c333d` (Rojo Prodeman). Debe utilizarse como acento, botones principales y bordes de focus.
*   **Fondos (Dark Mode Default)**: Gradiente o lisos basados en azules muy oscuros o violetas profundos (Ej: Entre `#1a1d29` y `#2a1f2b`).
*   **Estados (Acentos)**: 
    *   ✅ Success / Activo: `#22c55e` (Esmeralda).
    *   ⚠️ Warning / Mantenimiento: `#fbbf24` o `#f97316` (Ámbar / Naranja).
    *   ❌ Error / Inactivo: `#ef4444` (Rojo brillante).
    *   ℹ️ Info: `#3b82f6` (Azul).

## 📐 Reglas de Tailwind CSS
1.  **Espaciado Consistente**: Usar exclusivamente los múltiplos de Tailwind (ej: `p-4`, `m-2`, `gap-8`). No usar píxeles sueltos a menos que sea estrictamente necesario.
2.  **Tipografía Moderada**:
    *   Títulos: Fuentes Sans-serif modernas (Inter o Roboto), pesos `bold` (700) o `extrabold` (800).
    *   Cuerpo: Peso `medium` (500) para asegurar legibilidad sobre el blur.
3.  **Interactividad Obligatoria (Micro-animaciones)**:
    *   Todos los botones y tarjetas clicleables deben tener clases como: `transition-all duration-200 hover:scale-[1.02] active:scale-95`.
    *   Uso extendido de utilidades de animación como `animate-fade-in` o `animate-slide-up` para montar componentes.

## 🧠 Principios de UX "Plug & Play"
Para que una nueva app encaje perfectamente, su diseño debe:
*   **Tener un Sidebar / Layout Similar**: Si la app ocupa el 100% de la pantalla (fuera de iframe), debe replicar la navegación lateral o superior con colores oscuros/glass.
*   **Feedback Inmediato**: Las acciones CRUD deben gatillar notificaciones tipo "Toast" inmediatas.
*   **Carga Optimista / Esqueletos**: Mostrar "Skeleton Loaders" (barras parpadeantes simulando texto) en lugar de "Spinners" tradicionales o pantallas en blanco.
*   **Ausencia de Placeholders**: Si falta una imagen, debe crearse un gráfico estético o utilizarse un icono genérico de Lucide/React-Icons (`FaImage`, `FaBox`) dentro de una caja difuminada.

## 🛠️ Clases de Utilidad Clave (Referencia)
Todo componente tarjeta (Card), panel o modal debe construirse preferentemente con estas bases:

```css
/* Ejemplo Base de Cristal para Módulos Nuevos */
.module-glass-card {
    @apply bg-black/40 border border-white/10 backdrop-blur-xl rounded-2xl shadow-2xl;
}
```

---
> [!NOTE]
> Al inicializar un proyecto desde `BaseProyectos`, la mayoría de estos estilos ya estarán inyectados en `index.css` y en los componentes `_common/`. Su respeto garantiza una certificación visual automática.
