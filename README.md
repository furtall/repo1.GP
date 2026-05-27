# OpenFounds

**Sistema de Presupuesto Participativo — Río Tercero, Córdoba**

---

## HOME

OpenFounds es un sistema web orientado a gestionar procesos de presupuesto participativo, permitiendo a los ciudadanos de Río Tercero proponer, votar y hacer seguimiento de proyectos para su comunidad.

Es una plataforma digital diseñada para mejorar la participación ciudadana en la toma de decisiones sobre el uso de recursos públicos. A través del sistema, los ciudadanos podrán registrarse, presentar propuestas de mejora para su comunidad, participar mediante votaciones y consultar el estado de ejecución de los proyectos seleccionados.

El sistema también permitirá a los administradores y evaluadores gestionar propuestas, validar su viabilidad y supervisar el proceso completo, promoviendo transparencia, organización y participación democrática.

---

### Roles

| Rol | Descripción |
|-----|-------------|
| **Ciudadano** | Se registra, visualiza propuestas, vota y consulta el estado de los proyectos. Solo puede emitir un voto. |
| **Presidente de barrio** | Crea, edita y elimina propuestas propias. Tiene un límite en la cantidad de proyectos que puede presentar. El administrador le asigna este rol. |
| **Administrador** | Aprueba o rechaza propuestas, asigna el rol de presidente de barrio y supervisa todo el proceso. |

---

### Requerimientos funcionales

- Registro e inicio de sesión de ciudadanos.
- Creación, edición y eliminación de propuestas por el presidente de barrio.
- Visualización de propuestas y su detalle.
- Sistema de votación con límite de un voto por usuario.
- Visualización de resultados de votación.
- Aprobación / rechazo de propuestas por el administrador.
- Visualización del presupuesto total disponible.
- Límite de proyectos presentados por presidente de barrio.
- Estado del proyecto: en espera, en curso, finalizado.
- Asignación del rol de presidente de barrio por el administrador.

### Requerimientos no funcionales

- Fácil de usar (usabilidad).
- Accesible desde celular y PC.
- Tiempo de respuesta menor a X segundos.
- Protección de datos de los usuarios.
- Disponibilidad 24/7.

---

## CEREMONIAS

### Sprints

El proyecto OpenFounds se desarrolla en 6 sprints de 2 semanas cada uno.

| Sprint | Nombre | Resultado |
|--------|--------|-----------|
| 1 | Autenticación | Login funcionando |
| 2 | Propuestas | Crear y ver propuestas |
| 3 | Votación | Sistema de votos |
| 4 | Admin | Validación y selección |
| 5 | Presupuesto | Control financiero |
| 6 | UI / Final | Sistema completo |

---

### Ceremonias del equipo

| Ceremonia | Descripción |
|-----------|-------------|
| **Sprint Planning** | Al inicio de cada sprint de 2 semanas. El equipo selecciona las tareas del backlog y define el objetivo del sprint. |
| **Daily Scrum** | Todos los días hábiles, 15 minutos. El equipo sincroniza su trabajo y detecta impedimentos. |
| **Sprint Review** | Al final de cada sprint. Se demuestra el incremento funcional entregado. |
| **Retrospectiva** | Al final de cada sprint. El equipo reflexiona sobre el proceso y define mejoras para el siguiente sprint. |

---

### Daily Scrum

Reunión diaria de 15 minutos. Cada integrante responde:

| Pregunta | Foco |
|----------|------|
| ¿Qué hice ayer? | Avances realizados sobre las tareas del sprint en curso. |
| ¿Qué haré hoy? | Tareas a completar durante el día para acercarse al objetivo del sprint. |
| ¿Tengo impedimentos? | Bloqueos que impiden avanzar con el desarrollo del sistema. |

#### Impedimentos frecuentes identificados

- Dependencias entre módulos: el módulo de votación (Sprint 3) depende de que usuarios y propuestas (Sprints 1 y 2) estén finalizados.
- Dudas sobre requerimientos: criterios de validación de propuestas o límites de proyectos por barrio (Sprint 5).
- Criterios de aceptación incompletos antes de comenzar a codificar una tarea.
- Problemas de integración entre el frontend y el backend (Sprint 6 – TK-30).

---

### Sprint Review

Al final de cada sprint el equipo demuestra el incremento funcional completado. Se presenta únicamente lo que cumple la Definición de Hecho del equipo.

| Sprint | Objetivo | Entregables |
|--------|----------|-------------|
| **Sprint 1 — Autenticación** | Que un usuario pueda registrarse e iniciar sesión. | Usuario puede registrarse · Usuario puede loguearse · Sistema reconoce roles |
| **Sprint 2 — Propuestas** | Permitir crear y visualizar propuestas. | Presidente de barrio puede crear propuestas · Usuarios pueden visualizarlas |
| **Sprint 3 — Votación** | Implementar el sistema de votación. | Usuarios pueden votar proyectos · No pueden votar dos veces · Se visualizan los resultados |
| **Sprint 4 — Administración** | Permitir el control del sistema por parte del administrador. | Administrador controla qué propuestas se publican · Puede elegir las propuestas ganadoras |
| **Sprint 5 — Presupuesto y Reglas** | Controlar el dinero y las restricciones del sistema. | El sistema maneja el presupuesto correctamente · Evita errores de negocio en la asignación |
| **Sprint 6 — UX / Cierre** | Mejorar la experiencia de usuario y completar los requisitos restantes. | Sistema completo y funcional · Interfaz usable · Funciona correctamente en celular |

---

### Retrospectiva

#### Empezar

- Definir los criterios de aceptación de cada tarea antes de comenzar a codificar.
- Hacer refinement del backlog antes del Planning para llegar con las historias más claras.
- Documentar las decisiones técnicas del proyecto en la wiki.
- Verificar dependencias entre sprints antes de comenzar cada uno (ej.: votación depende de usuarios y propuestas).

#### Dejar de hacer

- Comenzar a codificar sin tener claros los criterios de aceptación de la tarea.
- Posponer la actualización del tablero de tareas hasta el final del día.
- Resolver impedimentos técnicos sin comunicarlos al equipo en el Daily.
- Dejar la integración de frontend y backend para el último sprint sin haberla probado antes.

#### Continuar

- Revisar el código entre compañeros (code review) antes de hacer merge.
- Pedir ayuda al equipo cuando hay un bloqueo en lugar de trabajar en silencio.
- Mantener el Daily breve y enfocado en el objetivo del sprint.
- Respetar la duración de 2 semanas por sprint para mantener el ritmo de entrega.

---

*OpenFounds — Wiki del Proyecto | Río Tercero, Córdoba*
