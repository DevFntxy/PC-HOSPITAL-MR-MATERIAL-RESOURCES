# 🗄️ Repositorio de Bases de Datos

Este directorio contiene la arquitectura, el diseño y los respaldos de la persistencia de datos del sistema. Está organizado según el paradigma de base de datos utilizado.

---

## 📂 Estructura de la Carpeta

### 🔵 1. SQL (Relacional)
En esta sección se gestionan los datos estructurados (PostgreSQL).
* `Backups/`: Scripts `.sql` autogenerados para la restauración completa de la BD.
* `DD/`: **Diccionario de Datos** con la descripción de tablas, columnas, tipos de datos y restricciones (PK/FK).
* `ERD/`: Diagramas Entidad-Relación visuales (formatos `.png` o `.pdf`).
* `RM/`: Documentación del Modelo Relacional.

### 🟢 2. NoSQL (No Relacional)
Gestión de documentos y datos no estructurados (MongoDB).
* `Backups/`: Archivos JSON o BSON de las colecciones principales.
* `DD/`: Descripción de la estructura esperada de los documentos.
* `Schemas/`: Definición de esquemas para validación (ej. Mongoose o JSON Schema).

---

## 📊 Resumen de la Arquitectura

| Paradigma | Motor | Uso Principal |
| :--- | :--- | :--- |
| **SQL** | PostgreSQL | Gestión de usuarios, sesiones y transacciones. |
| **NoSQL** | MongoDB | Almacenamiento de series temporales de sensores (Wearables). |

---



## Equipo de Desarrollo

| Integrante                   | Matrícula | Rol en el Equipo                     | Contacto                                                   |Observaciones |
|------------------------------|------------|--------------------------------------|-----------------------------------------------------------|--------------|
| Derek Sesni Carreño          | `230892`   | Lider, Desarrollo Backend           | [@DevFntxy](https://github.com/DevFntxy)                   | ⚠️ Pendiente |
| Diego Miguel Rivera Chavez   | `230260`   | Frontend, Diseño y Estructura de BD | [@DiegoMiguel04](https://github.com/DiegoMiguel04)         | ⚠️ Pendiente |
| José Arturo Garcia Gonzalez  | `230629`   | Diseño y Estructura de BD           | [@ppyo1234](https://github.com/ppyo1234)                   | ⚠️ Pendiente |
| Mauricio Rosales Gabriel     | `220859`   | Desarrollo Backend                  | [@elmau0834x](https://github.com/elmau0834x)               | ⚠️ Pendiente |
| Erick Matias Granillo Mejia  | `220045`   | Desarrollo Backend                  | [@EMATIAS](https://github.com/EMATIAS230045)               | ✔️ Validado |



# Estructura General

```text
DataBases/
│
├── SQL/
│   └── Readme.md
│
├── NoSQL/
│   │
│   ├── Backups/
│   │   └── Readme.md
│   │
│   ├── DD/
│   │    └── Readme.md
│   │
│   └── Schemas/
│       └── Readme.md
│
└── README.md