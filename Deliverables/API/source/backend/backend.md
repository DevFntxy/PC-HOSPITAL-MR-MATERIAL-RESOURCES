# Hospital MR API - Backend Documentation

## 📋 Descripción General

Hospital MR API es una API REST desarrollada con FastAPI que implementa un sistema híbrido SQL y NoSQL para la gestión de información hospitalaria.

La API utiliza:

- MySQL para almacenamiento relacional y ejecución de procedimientos almacenados.
- MongoDB para almacenamiento flexible de especificaciones técnicas en formato JSON.

El proyecto está orientado a la automatización de registros hospitalarios y adquisición de recursos medicos.

---

# Arquitectura del Proyecto

```
/backend
│
├── /core
│   └── config.py
├── /crud
│   └── adquisicion.py
├── /db
│   └── init.py
├── /routes
│   ├── pacientes.py
│   └── recursos_materiales.py 
├── /schemas
│   └── adquisicion.py
└── /main
    └── main.py
```