# Product Backlog Maestro - Historias de Usuario (UHs)

## Módulo: Material Resources (MR)

El siguiente backlog desglosa las Historias de Usuario estructuradas en Épicas, basadas en el alcance del módulo MR y los requisitos de la API de Adquisición de Equipamiento.

### Épica 1: Gestión de Proveedores
| ID | Título | Descripción (Como... quiero... para...) | Criterios de Aceptación |
|---|---|---|---|
| **UH-1.1** | Alta de Proveedor | **Como** administrador de compras,<br>**quiero** registrar los datos de un nuevo proveedor (nombre, contacto, especialidad),<br>**para** asociarlo a futuras transacciones de equipo. | 1. Permite crear el registro generando automáticamente un `id_persona` si no existe.<br>2. Se guarda la especialidad del equipamiento que maneja.<br>3. Los datos obligatorios faltantes asumen valores predeterminados seguros. |
| **UH-1.2** | Directorio de Proveedores | **Como** personal administrativo,<br>**quiero** consultar la lista de proveedores (Personas Morales),<br>**para** encontrar contactos de mantenimiento o nuevas compras. | 1. Se debe mostrar nombre, contacto y especialidad. |

### Épica 2: Control Financiero y Transacciones
| ID | Título | Descripción (Como... quiero... para...) | Criterios de Aceptación |
|---|---|---|---|
| **UH-2.1** | Registro de Transacciones | **Como** administrador financiero,<br>**quiero** capturar la transacción (Compra, Pago, Devolución, Ajuste) de un recurso,<br>**para** llevar control del gasto presupuestal. | 1. Se valida que el tipo de transacción sea válido (Compra, Pago, etc.).<br>2. Se registra la fecha y un folio/referencia.<br>3. En caso de ausencia de fecha, se asume una de los últimos 365 días (comportamiento API). |

### Épica 3: Catálogo y Trazabilidad de Equipamiento
| ID | Título | Descripción (Como... quiero... para...) | Criterios de Aceptación |
|---|---|---|---|
| **UH-3.1** | Alta de Equipamiento Básico | **Como** jefe de inventarios,<br>**quiero** registrar un nuevo equipo (nombre, marca, espacio_id),<br>**para** identificar su existencia y ubicación física en el hospital. | 1. Se vincula obligatoriamente a un `espacio_id` válido.<br>2. Genera un ID único para el equipo en la base relacional MySQL. |
| **UH-3.2** | Registro de Especificaciones Técnicas (NoSQL) | **Como** ingeniero biomédico,<br>**quiero** guardar las especificaciones extendidas (fabricante, modelo, garantía, peso, voltaje, etc.) de un equipo,<br>**para** consultar detalles operativos y de mantenimiento. | 1. Se guarda la información en una colección MongoDB (`equipamientos_specs`).<br>2. Se soportan campos JSON libres en la llave `specs_extra`.<br>3. Los campos peso_kg y garantia_meses se validan como `>= 0`. |

### Épica 4: Integración y Consistencia Híbrida (Técnica)
| ID | Título | Descripción (Como... quiero... para...) | Criterios de Aceptación |
|---|---|---|---|
| **UH-4.1** | Endpoint de Adquisición Completa | **Como** sistema cliente (frontend u otro módulo),<br>**quiero** consumir el endpoint `/adquisicion-equipamiento`,<br>**para** persistir de manera atómica todos los datos de una adquisición. | 1. Acepta un JSON estructurado con `proveedor`, `transaccion`, `equipamiento` y `specs`.<br>2. Ejecuta inserciones en bloque en MySQL (SP) y en MongoDB.<br>3. Retorna un resumen con los IDs generados (`mysql`, `mongodb`) o un error claro en caso de fallo. |
| **UH-4.2** | Poblar Datos de Prueba (Pacientes/Mock) | **Como** desarrollador/tester,<br>**quiero** usar el endpoint `/poblar-pacientes`,<br>**para** generar volúmenes de datos ficticios para pruebas de carga o demostración. | 1. Permite especificar `cantidad`, `genero`, `edad`, y `estatus`.<br>2. Genera el número exacto de registros solicitados. |
