<p align="right">
  <img src="../media/utpllogo.png" alt="Logo UTPL" width="150"/>
</p>

# Modelo de Datos

El presente modelo de datos está diseñado para gestionar un sistema orientado a la administración de componentes, solicitudes, inventarios y órdenes de compra.Cada tabla representa una entidad principal o una relación clave entre entidades, con atributos que capturan los datos esenciales.

## Descripción General

El sistema permite a los usuarios del personal administrativo interactuar con componentes mediante operaciones como generar solicitudes, administrar inventarios, y procesar órdenes de compra. Adicionalmente, se registran los movimientos de los componentes, asegurando un historial detallado para su trazabilidad. La seguridad está garantizada a través de un sistema de credenciales asociado a cada usuario.

<p align="center">
  <img src="../media/Modelo de Datos.png" alt="Modelo de datos"/>
</p>

## Tablas y Propósitos

### UTPL
- **Propósito**: Administrar credenciales de acceso del sistema y mensajes de error para los usuarios.
- **Atributos**:
  - `sistema_credenciales`: Identificador de las credenciales del sistema.
  - `mensaje_error`: Mensaje que describe errores en la validación.

### PERSONAL_ADMINISTRATIVO
- **Propósito**: Representa a los usuarios administrativos que gestionan componentes y solicitudes.
- **Atributos**:
  - `usuario`: Identificador único del usuario.
  - `password`: Contraseña para acceder al sistema.

### SERVICIO_CHECKLIST
- **Propósito**: Manejar las solicitudes generadas y el estado de entrega de componentes.
- **Atributos**:
  - `id_servicio`: Identificador único del servicio.
  - `estado_entrega`: Estado actual del servicio.
  - `fecha_creacion`: Fecha en la que se creó el servicio.
  - `estado_servicio`: Estado general del servicio.

### SOLICITUD
- **Propósito**: Registro de solicitudes de componentes realizadas por el personal administrativo.
- **Atributos**:
  - `id_solicitud`: Identificador único de la solicitud.
  - `id_servicio`: Referencia al servicio asociado.
  - `id_personal`: Referencia al usuario que realiza la solicitud.
  - `estado_solicitud`: Estado actual de la solicitud.
  - `fecha_solicitud`: Fecha de creación de la solicitud.

### SOLICITUD_COMPONENTE
- **Propósito**: Relación entre solicitudes y los componentes solicitados.
- **Atributos**:
  - `id_solicitud`: Referencia a la solicitud asociada.
  - `id_componente`: Referencia al componente solicitado.
  - `estado_componente_solicitud`: Estado del componente en la solicitud.
  - `cantidad_solicitada`: Cantidad de componentes solicitados.

### INVENTARIO
- **Propósito**: Control y almacenamiento de los componentes disponibles.
- **Atributos**:
  - `id_inventario`: Identificador único del inventario.
  - `id_componente`: Referencia al componente almacenado.
  - `estado_componente`: Estado del componente en el inventario.

### HISTORIAL_MOVIMIENTOS
- **Propósito**: Registro histórico de los movimientos realizados sobre los componentes.
- **Atributos**:
  - `id_movimiento`: Identificador único del movimiento.
  - `id_componente`: Referencia al componente relacionado.
  - `detalle_movimiento`: Descripción del movimiento realizado.
  - `fecha_movimiento`: Fecha en la que ocurrió el movimiento.

### COMPONENTE
- **Propósito**: Representación de un componente físico gestionado en el sistema.
- **Atributos**:
  - `id_componente`: Identificador único del componente.
  - `nombre_componente`: Nombre del componente.
  - `estado_componente`: Estado actual del componente.
  - `categoria`: Categoría a la que pertenece el componente.
  - `detalles`: Detalles adicionales sobre el componente.

### ORDEN_COMPRA
- **Propósito**: Registro de órdenes de compra de componentes.
- **Atributos**:
  - `id_orden`: Identificador único de la orden.
  - `estado_orden`: Estado actual de la orden.
  - `fecha_creacion`: Fecha de creación de la orden.

### COMPONENTES_SOLICITADOS
- **Propósito**: Relación entre órdenes de compra y los componentes solicitados en cada una.
- **Atributos**:
  - `id_orden`: Referencia a la orden de compra asociada.
  - `id_componente`: Referencia al componente solicitado.
  - `cantidad`: Cantidad de componentes solicitados.

---

## Relaciones entre Tablas
- **UTPL - PERSONAL_ADMINISTRATIVO**: Relación para validar credenciales.
- **PERSONAL_ADMINISTRATIVO - SOLICITUD**: Cada usuario puede generar múltiples solicitudes.
- **SOLICITUD - SOLICITUD_COMPONENTE**: Cada solicitud puede incluir varios componentes.
- **COMPONENTE - INVENTARIO**: Los componentes son almacenados en un inventario.
- **HISTORIAL_MOVIMIENTOS - COMPONENTE**: Cada componente tiene un historial de movimientos.
- **ORDEN_COMPRA - COMPONENTES_SOLICITADOS**: Cada orden incluye varios componentes.

---

