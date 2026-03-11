# ecoScan ♻️

Plataforma web para la gestión de recicladoras y clasificación de residuos, desarrollada como proyecto colaborativo. 
El sistema permite registrar recicladoras, administrar los materiales que aceptan, gestionar sus horarios y facilitar la consulta de información para promover el reciclaje.

🔗 **Repositorio original:**  
https://github.com/BenyiCordero/ecoScan

🌐 **Sitio web del proyecto:**  
https://smarttech.icu/index.htm

---

# 👩‍💻 Mi contribución (Backend)

Participé en el desarrollo del **backend del módulo de recicladoras**, implementando la lógica de negocio, acceso a datos y endpoints REST para la gestión de recicladoras, materiales y horarios.

---

# 🔧 Desarrollo de API REST

Se implementaron endpoints para administrar recicladoras, materiales aceptados y horarios.

## Recicladora

- **POST:** crear recicladora  
- **GET:** obtener todas las recicladoras  
- **GET:** obtener recicladoras activas  
- **GET:** obtener recicladoras inactivas  
- **GET:** obtener recicladora por ID  
- **PUT:** actualizar datos de recicladora  
- **DELETE:** eliminación lógica (desactivar recicladora)  
- **POST:** reactivar recicladora  

### Gestión de materiales

- **GET:** ver materiales aceptados por una recicladora  
- **POST:** agregar materiales aceptados por una recicladora  
- **DELETE:** eliminar material ligado a la recicladora  

### Gestión de horarios

- **GET:** ver horarios de la recicladora  
- **POST:** agregar horario  
- **PUT:** actualizar horario  
- **DELETE:** eliminar horario  

---

# 🗂 Capa de acceso a datos (DAO)

Se implementaron clases DAO para manejar la interacción con la base de datos de las siguientes entidades:

- **Material**
- **Recicladora**
- **RecicladoraDetails**
- **Horario**

### Funcionalidades principales implementadas

**Material**
- Alta de material  
- Consulta de todos los materiales  
- Consulta de material por ID  
- Actualización de material  
- Eliminación de material  

**Recicladora**
- Alta de recicladora  
- Consulta de recicladoras  
- Consulta por ID  
- Consulta de recicladoras activas e inactivas  
- Actualización de datos  
- Eliminación lógica de recicladora  

**RecicladoraDetails**
- Asociación de materiales aceptados por recicladora  
- Eliminación de materiales asociados  
- Validación para evitar materiales duplicados en una recicladora  

**Horario**
- Registro de horarios por día para cada recicladora  
- Consulta de horarios  
- Actualización de horarios  
- Eliminación de horarios  

---

# 📦 Implementación de DTO

Se diseñaron **DTO (Data Transfer Objects)** para estructurar la comunicación entre el backend y los endpoints de la API.

### DTO implementados

**Recicladora**
- RecicladoraRequest  
- RecicladoraUpdate  

**Horarios**
- HorarioUpdate  
- HorarioRequest  

**Material - Recicladora**
- MaterialRecicladoraRequest  

---

# 🧠 Lógica adicional implementada

- Validación para evitar **materiales duplicados** en una recicladora  
- Implementación de **eliminación lógica (soft delete)** para recicladoras  
- Manejo de relaciones entre **recicladoras, materiales y horarios**  
- Organización del backend mediante **arquitectura por capas**

---

# 🏗 Arquitectura utilizada

El backend se organizó utilizando una arquitectura por capas:
Controller → DTO → DAO → Base de Datos
Esto permite mantener una separación clara entre la lógica de negocio, la comunicación de datos y el acceso a la base de datos.

---

# ⚙️ Tecnologías utilizadas

- **Java**
- **REST API**
- **MySQL**
- **DAO Pattern**
- **DTO Pattern**
- **Arquitectura por capas**

---

# 👥 Proyecto colaborativo

Este proyecto fue desarrollado en colaboración con otros integrantes del equipo.
