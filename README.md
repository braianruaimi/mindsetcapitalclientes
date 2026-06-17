# 🏦 Solicitud de Préstamo Express - Mind Set Capital

## 🔗 Acceso Rápido
**[🌐 Abrir Formulario](./index.html)** - Click aquí para acceder al formulario de solicitud

---

## 📋 Descripción del Proyecto

Plataforma moderna de solicitud de préstamos express con diseño glassmorphic responsivo, optimizado para desktop, tablet y móvil (iOS y Android). Integrada con FormSubmit.co para entrega de solicitudes por correo electrónico.

### ✨ Características Principales

- 💰 **4 Planes de Cuotas Flexibles**: 1, 2, 3 y 6 cuotas con montos variables
- 📱 **100% Responsive**: Optimizado para iOS, Android, tablet y desktop
- 🎨 **Diseño Glassmorphic Moderno**: Efecto de cristal con gradientes y blur
- ✅ **Validación en Tiempo Real**: Campos requeridos y formato de datos
- 🔐 **Seguridad Anti-spam**: Honeypot field + reCAPTCHA habilitado
- 📧 **Integración con FormSubmit.co**: Envío automático de solicitudes por email
- ♿ **Accesibilidad WCAG**: ARIA labels, navegación por teclado, contraste adecuado
- 🎭 **Animaciones Suaves**: Transiciones, cascadas y efectos de entrada
- 📍 **Geolocalización**: Campos para dirección completa
- 🏦 **Datos Bancarios**: Campo para ALIAS/CBU/CVU

---

## 📁 Estructura del Proyecto

```
mindsetcapitalclientes/
├── index.html              # Formulario principal con toda la lógica
├── styles.css              # Sistema de diseño y animaciones
├── gracias.html            # Página de éxito tras envío
├── README.md               # Este archivo
└── ...
```

### Archivos Clave

#### **index.html**
- Formulario de solicitud con 4 planes de cuotas
- JavaScript vanilla para accordion dinámico
- Sincronización de selección de planes
- Auto-llenado de montos desde lista de planes
- Dropdown personalizado con animaciones en cascada
- FormSubmit.co integration

#### **styles.css**
- Sistema de variables CSS
- Diseño glassmorphic con backdrop-filter
- Animaciones personalizadas (float-orb, rise-in, option-cascade)
- Responsive breakpoints (700px para móvil)
- Optimizaciones para iOS (safe-area-inset) y Android
- Scrollbar personalizado

#### **gracias.html**
- Página de éxito con confirmación
- Botón para volver al formulario
- Mismo tema de diseño

---

## 🚀 Características Técnicas

### Frontend Stack
- **HTML5**: Semántica, ARIA labels, meta tags de viewport
- **CSS3**: Gradientes, backdrop-filter, flexbox, grid, animaciones
- **JavaScript ES6+**: Vanilla JS, sin dependencias externas
- **Google Fonts**: Manrope (body) + Space Grotesk (headers)

### Formulario
- **Campos de Contacto**: Nombre, Apellido, DNI, Email, Teléfono
- **Dirección**: Calle, Línea 2, Ciudad, Provincia, Código Postal
- **Préstamo**: Monto solicitado, Plan elegido
- **Datos Bancarios**: ALIAS/CBU/CVU, Fecha de pago
- **Términos**: Checkbox aceptación de contrato

### Planes de Cuotas Disponibles

| Plan | Montos Disponibles |
|------|-------------------|
| **1 Cuota** | $50K, $100K, $200K, $300K |
| **2 Cuotas** | $100K, $200K, $300K, $500K |
| **3 Cuotas** | $200K, $300K, $500K |
| **6 Cuotas** | $200K, $300K, $500K, $1M, $2M |

---

## 📱 Optimizaciones por Dispositivo

### iOS (iPhone)
- ✅ Safe area inset para notch
- ✅ Scroll momentum nativo (-webkit-overflow-scrolling)
- ✅ Meta tags para app web (apple-mobile-web-app-capable)
- ✅ Font size 16px para evitar zoom automático
- ✅ Estatus bar translúcido (black-translucent)

### Android
- ✅ Font size 16px en inputs
- ✅ Altura mínima 44px en botones (toque cómodo)
- ✅ Sin estilos nativos (-webkit-appearance: none)
- ✅ Theme color para barra de dirección
- ✅ Meta mobile-web-app-capable

### Desktop
- ✅ Max-width 860px para lectura óptima
- ✅ Hover effects en botones
- ✅ Teclado accesible (Tab, Enter, Space)

---

## 🎨 Paleta de Colores

```css
--primary-color: #caa64a       /* Oro */
--primary-strong: #e4bd5e     /* Oro fuerte */
--bg-1: #050b15               /* Negro azulado */
--bg-2: #0a1322               /* Azul oscuro */
--bg-3: #111f36               /* Azul más oscuro */
--text-main: #eef5ff          /* Blanco frío */
--text-soft: #a6b7cd          /* Gris azulado */
```

---

## 🔐 Seguridad

- **Honeypot Field**: Campo oculto `_honey` para detectar bots
- **reCAPTCHA**: `_captcha=true` en FormSubmit
- **Validación HTML5**: `required`, `type="email"`, etc.
- **Email Destinatario**: mind.set.capital.pres@gmail.com
- **Página de Éxito**: Redirige a gracias.html tras envío

---

## ⚙️ Configuración

### FormSubmit.co
```
action: https://formsubmit.co/mind.set.capital.pres@gmail.com
_template: "table"
_captcha: "true"
_next: gracias.html
```

### Viewport (iOS/Android)
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0, 
  viewport-fit=cover, maximum-scale=5.0, user-scalable=yes">
```

---

## 📊 Interactividad

### Accordion Dinámico
- Click en "Planes Disponibles" expande/contrae
- Al abrir un plan, los otros se cierran automáticamente
- Recalculación automática de altura de paneles padre
- Transiciones suaves con maxHeight CSS

### Plan Picker
- Dropdown personalizado con 4 opciones
- Selección abre automáticamente el plan en la lista
- Animación en cascada de opciones (stagger 0.02s-0.2s)
- Click fuera cierra el dropdown

### Auto-llenado
- Click en monto de plan rellena "Monto Solicitado"
- Resalta el monto seleccionado con color dorado
- Scroll automático en móvil al campo rellenado

---

## 🎬 Animaciones

| Animación | Duración | Uso |
|-----------|----------|-----|
| `rise-in` | 0.8s | Entrada del formulario |
| `float-orb` | 10s | Orbas de fondo flotantes |
| `option-cascade` | 0.35s | Aparición de opciones del dropdown |
| `max-height` | 0.35s | Expansión/contracción de accordions |

---

## ♿ Accesibilidad

- ✅ ARIA labels en todos los botones interactivos
- ✅ `aria-expanded` para accordions
- ✅ `aria-live` para mensajes de error
- ✅ Navegación por teclado (Enter, Space, Tab)
- ✅ Contraste WCAG AA
- ✅ Font size mínimo 16px
- ✅ Min-height 44px en elementos táctiles
- ✅ `role="button"` en elementos clicables

---

## 📝 Notas de Desarrollo

### JavaScript (Vanilla)
- Sin frameworks ni jQuery
- Vanilla ES6+: arrow functions, template literals, destructuring
- RequestAnimationFrame para sincronización de layout
- Event delegation con `addEventListener`
- TransitionEnd event para recálculos

### CSS
- Variables CSS para temas
- Clamp() para responsive typography
- Backdrop-filter para glassmorphism
- CSS Grid y Flexbox
- Media queries para breakpoints

### Performance
- Archivo CSS minificado recomendado
- JavaScript inline en HTML (pequeño)
- Google Fonts optimizado
- Sin imágenes (gradientes CSS)
- Load time estimado: <2s

---

## 🔧 Personalización

### Cambiar Email Destinatario
En `index.html`, línea del action del form:
```html
<form action="https://formsubmit.co/TU_EMAIL@example.com" method="POST">
```

### Cambiar Página de Éxito
En `index.html`, cambiar el valor de `_next`:
```html
<input type="hidden" name="_next" id="next-url" value="tu-pagina.html">
```

### Modificar Planes
Editar en `index.html` en la sección "Planes Disponibles":
```html
<li>$MONTO abona $RESULTADO</li>
```

---

## 📞 Contacto

**Mind Set Capital**
- Email: mind.set.capital.pres@gmail.com
- Documentación: Confidencial

---

## 📄 Licencia

Proyecto propietario de Mind Set Capital. Todos los derechos reservados.

---

## 🚀 Roadmap Futuro

- [ ] Base de datos de solicitudes
- [ ] Panel de administración
- [ ] Notificaciones push
- [ ] WhatsApp integration
- [ ] Sistema de puntaje crediticio
- [ ] Multi-idioma (EN/PT)
- [ ] PWA (descargable)

---

**Última actualización**: 17 de Junio, 2026

**Versión**: 1.0.0 - Producción
