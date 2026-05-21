# Directorio: Esquemas de Colecciones NoSQL (Módulo MR)

## 📁 Propósito de la Carpeta
Este espacio almacena las definiciones estructurales, esquemas de validación y modelos de datos no relacionales (NoSQL) utilizados por el Módulo de Recursos Materiales (MR). Al estar dentro del motor NoSQL, esta carpeta organiza los planos técnicos para almacenar datos de alta velocidad, logs inmutables y payloads dinámicos que no encajan en el modelo relacional puro.

## 📄 Estructura de Archivos Esperada (Índice de Contenido)

El equipo de Backend y Base de Datos debe organizar los esquemas en los siguientes subdirectorios dentro de esta carpeta:

### 1. `security_logs/` (Control de Seguridad y Accesos)
*Documentos orientados al registro inmutable de accesos a áreas restringidas de suministros.*
- **`access_log_schema.json`**: Esquema de validación estricta (JSON Schema) para auditoría. Debe exigir de forma obligatoria: `timestamp`, `user_id`, `biometric_token`, `access_point_id` y `status_result` (Exitoso/Denegado).

### 2. `inventory_telemetry/` (Trazabilidad y Wearables)
*Esquemas para el flujo de datos rápidos provenientes de la WebApp y la WearableApp.*
- **`asset_location_history.json`**: Modelo para guardar el histórico de geolocalización o asignación de dispositivos médicos móviles dentro del hospital.
- **`stock_alerts_stream.json`**: Estructura de las notificaciones y alertas de stock crítico enviadas en tiempo real a los dispositivos vestibles del personal de almacén.

### 3. `provider_metadata/` (Información Flexible de Proveedores)
*Esquemas para almacenar datos no estructurados de las Personas Morales.*
- **`ext_catalog_cache.json`**: Estructura para almacenar las respuestas temporales (caché) de las APIs de proveedores externos para agilizar las cotizaciones financieras.

---

## 🛠️ Tecnologías Sugeridas para estos Esquemas
Dependiendo del stack del equipo de desarrollo, los archivos aquí depositados deben usar extensiones estándar:
- **`.json` / `.ts`**: Si usan esquemas de validación pura como *JSON Schema*, *Zod* o *Joi*.
- **`.js` / `.ts`**: Si definen modelos ODM directos (ej. Schemas de *Mongoose* para MongoDB).

## ⚠️ Reglas de Integración con `DD/` (Diccionario de Datos)
Toda colección definida en este directorio de esquemas NoSQL debe contar con su correspondiente hoja explicativa en la carpeta hermana **`../DD/` (Diccionario de Datos)**, detallando el propósito de cada llave (`key`) y los índices de rendimiento creados para las consultas de emergencia del hospital.

## Equipo de Desarrollo

| Integrante                   | Matrícula | Rol en el Equipo                     | Contacto                                                   |Observaciones |
|------------------------------|------------|--------------------------------------|-----------------------------------------------------------|--------------|
| Derek Sesni Carreño          | `230892`   | Lider, Desarrollo Backend           | [@DevFntxy](https://github.com/DevFntxy)                   | ✔️ Validado |
| Diego Miguel Rivera Chavez   | `230260`   | Frontend, Diseño y Estructura de BD | [@DiegoMiguel04](https://github.com/DiegoMiguel04)         | ✔️ Validado |
| José Arturo Garcia Gonzalez  | `230629`   | Diseño y Estructura de BD           | [@ppyo1234](https://github.com/ppyo1234)                   | ✔️ Validado |
| Mauricio Rosales Gabriel     | `220859`   | Desarrollo Backend                  | [@elmau0834x](https://github.com/elmau0834x)               | ✔️ Validado |
| Erick Matias Granillo Mejia  | `220045`   | Desarrollo Backend                  | [@EMATIAS](https://github.com/EMATIAS230045)               | ✔️ Validado |