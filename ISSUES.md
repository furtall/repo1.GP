# ISSUES – Proyecto OpenFounds

> Sistema que permite a los ciudadanos proponer, visualizar y votar proyectos para la asignación de recursos públicos.

---

## 📋 Historias de Usuario

| ID | Actor | Quiero | Para |
|----|-------|--------|------|
| HU-01 | Ciudadano | Registrarme en la plataforma | Poder participar en las decisiones de mi barrio |
| HU-02 | Ciudadano | Ver el listado de propuestas presentadas | Conocer en qué se quiere invertir el presupuesto |
| HU-03 | Ciudadano | Votar por una propuesta específica | Apoyar las mejoras que considero prioritarias |
| HU-04 | Administrador | Validar propuestas | Asegurar su viabilidad |
| HU-05 | Jefe de barrio | Subir propuesta | Proponer mejoras |
| HU-06 | Jefe de barrio | Editar propuestas | Corregirlas |
| HU-07 | Jefe de barrio | Asignar presupuesto al proyecto creado | Estimar costos |
| HU-08 | Administrador | Gestionar usuarios | Mantener el sistema |
| HU-09 | Administrador | Seleccionar propuestas | Asignar el presupuesto |

---

## ✅ Criterios de Aceptación

### HU-01 – Registro de ciudadano

- **Escenario 1:** Dado que el ciudadano accede al formulario de registro, cuando completa todos los campos obligatorios correctamente, entonces el sistema crea su cuenta y confirma el registro.
- **Escenario 2:** Dado que el ciudadano intenta registrarse, cuando ingresa un email ya existente, entonces el sistema muestra un mensaje de error indicando que el usuario ya está registrado.
- **Escenario 3:** Dado que el ciudadano completa el formulario, cuando deja campos obligatorios vacíos, entonces el sistema no permite avanzar y muestra los campos a completar.

### HU-02 – Ver listado de propuestas

- **Escenario 1:** Dado que el ciudadano está autenticado, cuando accede a la sección de propuestas, entonces el sistema muestra el listado de propuestas disponibles.
- **Escenario 2:** Dado que el ciudadano visualiza el listado, cuando selecciona una propuesta, entonces el sistema muestra el detalle de la misma.

### HU-03 – Votar propuesta

- **Escenario 1:** Dado que el ciudadano está autenticado, cuando selecciona una propuesta y emite su voto, entonces el sistema registra el voto correctamente.
- **Escenario 2:** Dado que el ciudadano ya votó una propuesta, cuando intenta votar nuevamente la misma propuesta, entonces el sistema impide el voto duplicado y muestra un mensaje.

### HU-04 – Validar propuestas (Administrador)

- **Escenario 1:** Dado que el administrador accede al panel de propuestas pendientes, cuando revisa una propuesta, entonces puede aprobarla o rechazarla.
- **Escenario 2:** Dado que el administrador valida una propuesta, cuando la aprueba, entonces la propuesta queda disponible para votación.
- **Escenario 3:** Dado que el administrador rechaza una propuesta, cuando confirma la acción, entonces la propuesta queda marcada como rechazada.

### HU-05 – Subir propuesta (Jefe de barrio)

- **Escenario 1:** Dado que el jefe de barrio está autenticado, cuando completa el formulario de propuesta, entonces el sistema guarda la propuesta correctamente.
- **Escenario 2:** Dado que el jefe de barrio intenta enviar una propuesta, cuando faltan datos obligatorios, entonces el sistema muestra errores y no permite enviarla.

### HU-06 – Editar propuestas (Jefe de barrio)

- **Escenario 1:** Dado que el jefe de barrio tiene una propuesta creada, cuando accede a editarla, entonces puede modificar sus datos.
- **Escenario 2:** Dado que el jefe de barrio guarda los cambios, cuando la edición es válida, entonces el sistema actualiza la propuesta correctamente.

### HU-07 – Asignar presupuesto (Jefe de barrio)

- **Escenario 1:** Dado que el jefe de barrio está creando o editando una propuesta, cuando asigna un presupuesto válido, entonces el sistema guarda el monto asociado.
- **Escenario 2:** Dado que el jefe de barrio ingresa un monto inválido, cuando intenta guardarlo, entonces el sistema muestra un error y no lo permite.

### HU-08 – Gestionar usuarios (Administrador)

- **Escenario 1:** Dado que el administrador accede al módulo de usuarios, cuando visualiza el listado, entonces el sistema muestra todos los usuarios registrados.
- **Escenario 2:** Dado que el administrador selecciona un usuario, cuando realiza una acción (editar, bloquear o eliminar), entonces el sistema aplica el cambio correctamente.

### HU-09 – Seleccionar propuestas (Administrador)

- **Escenario 1:** Dado que el administrador visualiza propuestas votadas, cuando selecciona una propuesta, entonces el sistema la marca como elegida.
- **Escenario 2:** Dado que el administrador selecciona propuestas, cuando confirma la asignación de presupuesto, entonces el sistema registra la decisión final.

---

## 🏁 Milestones y Tareas por Sprint

> Duración de cada sprint: **2 semanas**
> Equipo: **Alvaro** · **Alejo** · **Mateo** · **Alexis** · **Dahy**

---

### 🟢 Milestone 1 – SPRINT 1: Base del Sistema (Autenticación)

**🎯 Objetivo:** Que un usuario pueda registrarse e iniciar sesión.
**📅 HU relacionadas:** HU-01

**✅ Entregables:**
- Usuario puede registrarse
- Usuario puede loguearse
- Sistema reconoce roles

| Tarea | Descripción | Asignado a |
|-------|-------------|------------|
| TK-01 | Base de datos usuarios | **Alvaro** |
| TK-02 | Registro de usuario (frontend + backend) | **Alejo** |
| TK-03 | Login (backend + lógica) | **Mateo** |
| TK-04 | Validación email único | **Alvaro** |
| TK-05 | Roles + middleware de autorización | **Alexis** |
| TK-31 | Seguridad (hash contraseñas, protección endpoints) | **Dahy** |

---

### 🟡 Milestone 2 – SPRINT 2: Propuestas (Core del Sistema)

**🎯 Objetivo:** Permitir crear y visualizar propuestas.
**📅 HU relacionadas:** HU-02, HU-05, HU-06, HU-07

**✅ Entregables:**
- Jefe de barrio puede crear propuestas
- Usuarios pueden verlas

| Tarea | Descripción | Asignado a |
|-------|-------------|------------|
| TK-07 | Base de datos propuestas | **Alvaro** |
| TK-08 | Crear propuesta (frontend) | **Alejo** |
| TK-09 | Editar propuesta (backend) | **Mateo** |
| TK-10 | Listar propuestas | **Alexis** |
| TK-11 | Ver detalle de propuesta | **Dahy** |
| TK-12 | Validaciones de propuesta | **Dahy** |

---

### 🔵 Milestone 3 – SPRINT 3: Votación

**🎯 Objetivo:** Implementar el sistema de votación.
**📅 HU relacionadas:** HU-03

**✅ Entregables:**
- Usuarios pueden votar
- No pueden votar dos veces
- Se ven resultados

| Tarea | Descripción | Asignado a |
|-------|-------------|------------|
| TK-13 | Base de datos votos | **Alvaro** |
| TK-14 | Registrar voto (frontend) | **Alejo** |
| TK-15 | Validación voto único | **Mateo** |
| TK-16 | Mostrar resultados de votación | **Alexis** |
| —     | Testing + integración de votación | **Dahy** |

---

### 🟣 Milestone 4 – SPRINT 4: Administración

**🎯 Objetivo:** Permitir control del sistema por administrador.
**📅 HU relacionadas:** HU-04, HU-08, HU-09

**✅ Entregables:**
- Admin controla qué propuestas se publican
- Puede elegir ganadores

| Tarea | Descripción | Asignado a |
|-------|-------------|------------|
| TK-17 | Panel propuestas pendientes | **Alvaro** |
| TK-18 | Aprobar/rechazar propuesta (frontend) | **Alejo** |
| TK-19 | Estados de propuesta | **Mateo** |
| TK-20 | Selección de propuestas | **Alexis** |
| TK-21 | Asignación final + testing | **Dahy** |

---

### 🟠 Milestone 5 – SPRINT 5: Presupuesto y Reglas

**🎯 Objetivo:** Controlar dinero y restricciones.
**📅 HU relacionadas:** HU-07, HU-09

**✅ Entregables:**
- Sistema maneja presupuesto correctamente
- Evita errores de negocio

| Tarea | Descripción | Asignado a |
|-------|-------------|------------|
| TK-22 | Validación de presupuesto | **Alvaro** |
| TK-23 | Visualización de presupuesto total | **Alejo** |
| TK-24 | Control de asignación | **Mateo** |
| TK-27 | Límite de propuestas por jefe de barrio | **Alexis** |
| —     | Testing + validación de reglas de negocio | **Dahy** |

---

### 🔴 Milestone 6 – SPRINT 6: UX + Mejoras + Final

**🎯 Objetivo:** Mejorar la experiencia de usuario y completar requisitos.
**📅 HU relacionadas:** Todas (cierre y pulido)

**✅ Entregables:**
- Sistema completo
- Interfaz usable
- Funciona en celular

| Tarea | Descripción | Asignado a |
|-------|-------------|------------|
| TK-25 | Estados visuales de propuestas | **Alvaro** |
| TK-29 | Maquetado frontend | **Alejo** |
| TK-28 | Control de acceso por rol | **Mateo** |
| TK-30 | Integración frontend-backend | **Alexis** |
| TK-26 | UI de estados de propuesta | **Dahy** |
| TK-32 | Responsive (mobile + desktop) | **Dahy** |
| TK-33 | Performance | **Dahy** |

---

## 👥 Resumen de Asignaciones por Integrante

| Integrante | Rol principal | Tareas |
|------------|--------------|--------|
| **Alvaro** | Backend / Base de datos | TK-01, TK-04, TK-07, TK-13, TK-17, TK-22, TK-25 |
| **Alejo** | Frontend | TK-02, TK-08, TK-14, TK-18, TK-23, TK-29 |
| **Mateo** | Lógica backend | TK-03, TK-09, TK-15, TK-19, TK-24, TK-28 |
| **Alexis** | Integración / Funcionalidades | TK-05, TK-10, TK-16, TK-20, TK-27, TK-30 |
| **Dahy** | Testing + UX + Validaciones | TK-31, TK-11, TK-12, TK-21, TK-26, TK-32, TK-33 |

---

## 📊 Resumen General de Sprints

| Sprint | Nombre | HU Relacionadas | Resultado esperado |
|--------|--------|-----------------|-------------------|
| 1 | Autenticación | HU-01 | Login y registro funcionando |
| 2 | Propuestas | HU-02, HU-05, HU-06, HU-07 | Crear y ver propuestas |
| 3 | Votación | HU-03 | Sistema de votos operativo |
| 4 | Administración | HU-04, HU-08, HU-09 | Validación y selección de propuestas |
| 5 | Presupuesto | HU-07, HU-09 | Control financiero y reglas de negocio |
| 6 | UI / Final | Todas | Sistema completo y responsive |
