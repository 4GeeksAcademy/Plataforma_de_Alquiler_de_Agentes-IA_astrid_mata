# Especificación Técnica: Panel de Administración AgentHub

## 1. Descripción del Producto
AgentHub es una plataforma SaaS para alquilar agentes de IA preconfigurados. Este panel es la interfaz administrativa interna para gestionar usuarios, agentes, contratos y monitorear errores.
- **Usuario Administrador:** Perfil con acceso total para gestionar recursos, usuarios y configuraciones de seguridad.

## 2. Stack Tecnológico y Restricciones
- **HTML5:** Estructura semántica.
- **CSS:** Tailwind CSS (vía CDN exclusivamente). No usar archivos CSS externos ni estilos en línea.
- **JavaScript:** Vanilla JS únicamente. Prohibido el uso de frameworks (React, Vue, etc.) o librerías como jQuery.
- **Diseño:** Responsive para desktop y tablet.

## 3. Inventario de Componentes UI
- **Sidebar:** Navegación persistente con indicador de sección activa.
- **Cards:** Contenedores con sombras sutiles, bordes redondeados y colores de acento.
- **Dropdowns:** Menú vertical (⋮) que abre opciones al hacer clic y se cierra al hacer clic fuera.
- **Modales:** Overlays centrados con botón de cierre y cierre al hacer clic en el backdrop.
- **Badges:** Etiquetas con códigos de color para estados (Activo, Fallando, etc.).
- **Lists (Collapsable):** Secciones expandibles con transición CSS suave.
- **Theme Toggle:** Botón en top-bar para cambiar entre clases `light` y `dark`.

## 4. Secciones y Especificaciones
*(Aquí debes detallar las 6 secciones como pide el reto)*

### 4.1 Dashboard
1. **Métricas:** 4 tarjetas en grid 2x2. Icono, etiqueta y valor hardcodeado.
2. **Estilo:** Colores de acento distintos por métrica, sombra sutil.
3. **Gráfico:** Un `div` contenedor con borde discontinuo y etiqueta centrada para representar actividad semanal.

### 4.2 Gestión de Usuarios
*(Aplica el mismo nivel de detalle para cada sección: 1. Estructura, 2. Interacción, 3. Componentes usados)*
...

## 5. Criterios de Aceptación
1. `SPECS.md` commiteado antes de cualquier archivo HTML.
2. Navegación lateral funcional y persistente.
3. Toggle de modo oscuro operacional en toda la interfaz.
4. Todos los dropdowns funcionan (abrir/cerrar).
5. Modales funcionales en las 4 secciones requeridas (cerrar con botón y backdrop).
6. Listas de skills expandibles/colapsables con transición suave.