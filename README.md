# UniTrack – Sistema de Gestión Académica

## 1. Nombre del sistema

**UniTrack – Sistema de Gestión Académica**

UniTrack es un proyecto académico orientado al diseño de un sistema que facilite la organización y consulta de información académica de los estudiantes.

## 2. Problema que resuelve

Cuando la información académica se encuentra dispersa entre documentos, hojas de cálculo o procesos manuales, puede resultar difícil consultarla, mantenerla actualizada y controlar quién tiene permiso para modificarla. Esto puede ocasionar pérdida de tiempo, duplicación de datos y errores en el manejo de la información.

UniTrack propone centralizar la información académica en una solución organizada, con acceso según el rol del usuario y una estructura que facilite su consulta y administración.

## 3. Objetivo general

Diseñar un sistema de gestión académica que permita organizar y consultar información de estudiantes, asignaturas inscritas, horarios y calificaciones, aplicando principios de análisis de requisitos, modelado UML, arquitectura de software, planificación y control de cambios.

## 4. Funcionalidades principales

El alcance funcional propuesto contempla:

- **Autenticación de usuarios:** acceso al sistema mediante una cuenta.
- **Consulta de calificaciones:** permitir que el estudiante revise sus resultados académicos.
- **Consulta de asignaturas inscritas:** mostrar las asignaturas registradas para el estudiante.
- **Consulta de horario académico:** facilitar la revisión del horario de clases.
- **Gestión de estudiantes:** organizar y mantener los datos de los estudiantes.
- **Registro y gestión de calificaciones:** permitir al personal autorizado registrar o actualizar resultados.
- **Control de roles y permisos:** limitar las operaciones disponibles según el tipo de usuario.

Estas funcionalidades describen el alcance previsto; su disponibilidad real dependerá de la implementación y las pruebas posteriores.

## 5. Arquitectura seleccionada

Para el diseño de UniTrack se adopta una **arquitectura por capas de tres niveles**, que separa la interfaz, el procesamiento de las solicitudes y el almacenamiento de datos.

- **Frontend (presentación):** interfaz con la que interactúan estudiantes, personal académico y administradores.
- **Backend / API (lógica de aplicación):** recibe solicitudes, valida datos, aplica reglas de negocio y controla el acceso a las operaciones.
- **Base de datos (persistencia):** almacena la información académica, como estudiantes, asignaturas, inscripciones, horarios, calificaciones y usuarios.

**Flujo general:** el usuario interactúa con el frontend; este envía solicitudes al backend; el backend procesa las reglas y consulta o actualiza la base de datos; finalmente, devuelve una respuesta al frontend. El frontend no accede directamente a la base de datos.

## 6. Herramientas utilizadas y de apoyo

- **GitHub:** alojamiento del repositorio y registro de cambios mediante commits.
- **GitHub Issues:** registro y seguimiento de tareas, problemas y mejoras.
- **GitHub Projects:** organización y visualización del avance en un tablero de trabajo.
- **Visual Paradigm Online:** elaboración y documentación de modelos y diagramas UML.
- **Markdown:** formato empleado para mantener la documentación técnica dentro del repositorio.

## 7. Documentación del proyecto

Los documentos técnicos se encuentran en la carpeta [docs/](docs/):

| Archivo | Descripción |
|---|---|
| [REQUISITOS.md](docs/REQUISITOS.md) | Requisitos funcionales y no funcionales e historias de usuario. |
| [ARQUITECTURA.md](docs/ARQUITECTURA.md) | Capas, responsabilidades y comunicación entre componentes. |
| [UML.md](docs/UML.md) | Descripción de los modelos UML contemplados. |
| [SEGUIMIENTO.md](docs/SEGUIMIENTO.md) | Organización y seguimiento de tareas. |
| [CONTROL_CAMBIOS.md](docs/CONTROL_CAMBIOS.md) | Criterios para registrar y revisar cambios. |
| [NOTA_VERSION_0.1.md](docs/NOTA_VERSION_0.1.md) | Alcance de la línea base documental y próximos pasos. |

## 8. Estado actual del proyecto

**Estado: análisis, diseño, arquitectura y documentación académica.**

El repositorio cuenta con un README principal y documentos iniciales de requisitos, arquitectura, UML, seguimiento, control de cambios y nota de versión. El proyecto continúa en desarrollo académico; la documentación no significa que las funcionalidades estén implementadas ni que hayan superado pruebas.

Los estados concretos de las tareas deben verificarse en GitHub Issues y GitHub Projects. También queda pendiente incorporar y verificar los archivos gráficos finales de los diagramas UML, si aún no se han agregado.

## 9. Próximos pasos

1. Revisar los requisitos y sus criterios de aceptación.
2. Completar y agregar los diagramas UML finales.
3. Verificar que las tareas estén registradas y actualizadas en Issues y Projects.
4. Priorizar los módulos para una futura implementación.
5. Documentar los cambios y las pruebas conforme avance el desarrollo.

## 10. Repositorio

[Consultar UniTrack en GitHub](https://github.com/ericksonsepulveda64-cell/ericksonsepulveda64-cell-UniTrack-Sistema-Gestion-Academica)
