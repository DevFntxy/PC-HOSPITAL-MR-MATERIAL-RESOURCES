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

## 🚀 Instrucciones de Configuración

### Restauración de SQL
Para restaurar la base de datos relacional, ejecuta el siguiente comando en tu terminal:
```bash
psql -U usuario -d nombre_bd < SQL/Backups/ultimo_backup.sql