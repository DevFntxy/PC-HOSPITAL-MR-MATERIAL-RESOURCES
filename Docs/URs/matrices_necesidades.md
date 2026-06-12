# Matriz de Necesidades y Requisitos de Usuario (URs)

## Módulo: Material Resources (MR)

A continuación, se detallan los requisitos de usuario basados en la documentación del proyecto y la funcionalidad de los endpoints expuestos por la API híbrida (MySQL + MongoDB).

### 1. Gestión de Adquisiciones e Inventario
| ID | Perfil de Usuario | Necesidad (Requisito) | Origen / Contexto |
|---|---|---|---|
| **UR-01** | Administrador de Compras | Necesito poder registrar la adquisición de nuevo equipamiento médico de forma centralizada, capturando proveedor, finanzas y especificaciones en un solo proceso. | Endpoint `/adquisicion-equipamiento` |
| **UR-02** | Jefe de Inventarios | Requiero asociar cada equipo médico a un espacio o área física específica del hospital para conocer su ubicación exacta. | Relación `espacio_id` en equipamiento |
| **UR-03** | Ingeniero Biomédico / Técnico | Necesito almacenar atributos técnicos muy variados y específicos para cada equipo (voltaje, peso, canales ECG, tamaño de pantalla, etc.) sin limitarme a una estructura rígida. | Uso de MongoDB (`specs_extra`) |

### 2. Gestión de Proveedores
| ID | Perfil de Usuario | Necesidad (Requisito) | Origen / Contexto |
|---|---|---|---|
| **UR-04** | Administrador de Compras | Requiero un directorio centralizado de proveedores (Personas Morales) con sus datos de contacto y especialidad para facilitar futuras compras. | Colecciones/Tablas de Proveedores y Personas Morales |

### 3. Control Financiero
| ID | Perfil de Usuario | Necesidad (Requisito) | Origen / Contexto |
|---|---|---|---|
| **UR-05** | Administrador Financiero | Necesito registrar y categorizar cada movimiento económico (Compra, Pago, Devolución, Ajuste) con su respectiva referencia y fecha de transacción para trazabilidad contable. | Parámetros de `transaccion` en la API |

### 4. Arquitectura y Rendimiento (NFR/UR Técnico)
| ID | Perfil de Usuario | Necesidad (Requisito) | Origen / Contexto |
|---|---|---|---|
| **UR-06** | Administrador de Sistemas | El sistema debe ser capaz de procesar inserciones de hasta 1000 registros por transacción asegurando la consistencia entre MySQL y MongoDB. | Restricciones del SP / API Híbrida |
| **UR-07** | Administrador de Sistemas | La comunicación con el módulo debe realizarse mediante una API REST documentada en Swagger (`/docs`) para facilitar la integración de clientes frontend. | Manual de Despliegue de la API |
