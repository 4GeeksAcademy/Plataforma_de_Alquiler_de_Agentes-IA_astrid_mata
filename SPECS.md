# Especificación Técnica: Panel de Administración AgentHub

## 1. Descripción del Producto
AgentHub es una plataforma SaaS para alquilar agentes de IA preconfigurados. Este panel es la interfaz administrativa interna para gestionar usuarios, agentes, contratos y monitorear errores.
- **Usuario Administrador:** Perfil con acceso total para gestionar recursos, usuarios y configuraciones de seguridad.

## 2. Stack Tecnológico y Restricciones
- **HTML5:** Estructura semántica.
- **CSS:** Tailwind CSS (vía CDN exclusivamente). No usar archivos CSS externos ni estilos en línea.
- **JavaScript:** Vanilla JS únicamente. Prohibido frameworks o librerías externas (salvo Chart.js/SheetJS).
- **Diseño:** Mobile-first, responsive para desktop y tablet (usando unidades modernas `svh/dvh`).

## 3. Inventario de Componentes UI
- **Sidebar:** Navegación persistente (desktop) y off-canvas (mobile) con indicador activo.
- **Cards:** Contenedores con sombras sutiles, bordes redondeados y colores de acento.
- **Dropdowns:** Menú (⋮) funcional con cierre al hacer clic fuera (click-outside).
- **Modales:** Overlays centrados con cierre vía botón o clic en el backdrop.
- **Badges:** Etiquetas semánticas con código de color.
- **Listas:** Skills expandibles con transiciones CSS suaves (`transition-all`).
- **Theme Toggle:** Botón persistente en topbar para alternar modo light/dark.

## 4. Secciones y Especificaciones

### 4.1 Dashboard
1. **Métricas:** 4 tarjetas (Ingresos, Pérdidas, Activos, Fallos) en grid 2x2.
2. **Estilo:** Sombras suaves y colores de acento diferenciados por tipo de métrica.
3. **Gráfico:** Contenedor con borde discontinuo e integración Chart.js (diario/semanal/mensual).

### 4.2 Gestión de Usuarios
1. **Estructura:** Tabla de 5 filas con ID, Nombre, Email, Plan y Estado.
2. **Interacción:** Dropdown por fila (Ver detalle/Eliminar). Contenedor con `overflow-x-auto`.
3. **Modal:** Registro completo con botón de cierre y gestión de backdrop.

### 4.3 Gestión de Agentes
1. **Listado:** 4 agentes con nombre, propietario, estado y skills colapsadas por defecto.
2. **Transición:** Control expandible que revela habilidades mediante `transition-all`.
3. **Acciones:** Dropdown con "Configurar" que abre modal con `<textarea>` editable.

### 4.4 Skills
1. **Grid:** Tarjetas responsive con bordes redondeados para cada habilidad.
2. **Etiquetas:** Categorización visual con colores de fondo distintivos.
3. **Indicadores:** Badge de conteo ("Asignado a: X agentes") por cada card.

### 4.5 Contrataciones
1. **Registro:** Tabla (Cliente, Agente, Periodo, Total) con formato de moneda.
2. **Acciones:** Dropdown con "Ver detalle" para desplegar el resumen del contrato.
3. **Modal:** Visualización de desglose de skills y precios.

### 4.6 Log de Errores
1. **Tabla:** 6 entradas (Timestamp, Agente, Severidad, Descripción).
2. **Severidad:** Badges coloreados (rojo: crítico, amarillo: advertencia).
3. **Gestión:** Dropdown con "Ver detalle" y "Marcar resuelto".

## 5. Criterios de Aceptación
1. `SPECS.md` commiteado como primer paso.
2. Navegación persistente y funcional.
3. Modo oscuro operacional en toda la UI y persistente (localStorage).
4. Dropdowns operativos (abrir/cerrar/fuera).
5. Modales funcionales en secciones: Usuarios, Agentes, Contrataciones y Logs.
6. Listas de skills con animaciones suaves (`transition-all duration-300`).
7. Diseño mobile-first adaptado (usando `svh/dvh`).
8. Datos consistentes y hardcodeados en estructuras JS (arrays).