# UniTrack – Sistema de Gestión Académica

## 1. Descripción del proyecto

UniTrack es una propuesta académica de sistema de gestión que busca organizar y facilitar la consulta de información relacionada con la vida académica de los estudiantes. El proyecto contempla funciones para consultar calificaciones, revisar asignaturas inscritas, visualizar horarios y gestionar información académica según los permisos de cada usuario.

## 2. Problema que busca resolver

La información académica puede resultar difícil de consultar cuando está distribuida en diferentes medios o procesos manuales. UniTrack propone centralizar esa información en un sistema organizado, con acceso controlado y una estructura que facilite su consulta y mantenimiento.

## 3. Objetivo general

Diseñar una solución de gestión académica que permita organizar la información de estudiantes, asignaturas, horarios y calificaciones, aplicando principios de análisis de requisitos, modelado, arquitectura de software y planificación del desarrollo.

## 4. Usuarios principales

- **Estudiantes:** consultar sus calificaciones, asignaturas inscritas y horario académico.
- **Personal académico o administrativo:** gestionar y revisar la información académica de acuerdo con los permisos asignados.
- **Administradores:** gestionar usuarios, roles y permisos del sistema.

Estos perfiles representan el alcance funcional propuesto; su implementación debe verificarse durante una futura etapa de desarrollo.

## 5. Funcionalidades principales propuestas

- Consulta de calificaciones.
- Consulta de asignaturas inscritas.
- Consulta de horario académico.
- Gestión de estudiantes.
- Registro y administración de información académica.
- Autenticación de usuarios y control de acceso por roles.

## 6. Arquitectura propuesta

Se propone una arquitectura por capas con separación de responsabilidades:

- **Frontend:** interfaz para que los usuarios naveguen, consulten información y completen formularios.
- **Backend / API:** recibe solicitudes, valida los datos, aplica las reglas de negocio y coordina las operaciones.
- **Base de datos:** almacena la información de estudiantes, asignaturas, inscripciones, horarios, calificaciones y usuarios.

La interfaz se comunica con el backend mediante solicitudes definidas por la aplicación. El backend es responsable de acceder a la base de datos; el frontend no debe conectarse directamente a ella.

## 7. Organización de la documentación

La documentación técnica del proyecto se encuentra organizada en la carpeta `docs/`:

| Archivo | Contenido |
|---|---|
| [REQUISITOS.md](docs/REQUISITOS.md) | Requisitos funcionales y no funcionales e historias de usuario. |
| [ARQUITECTURA.md](docs/ARQUITECTURA.md) | Capas, responsabilidades y comunicación entre componentes. |
| [UML.md](docs/UML.md) | Descripción de los modelos UML y sus elementos principales. |
| [SEGUIMIENTO.md](docs/SEGUIMIENTO.md) | Organización del trabajo y seguimiento de tareas. |
| [CONTROL_CAMBIOS.md](docs/CONTROL_CAMBIOS.md) | Criterios para registrar y revisar cambios. |
| [NOTA_VERSION_0.1.md](docs/NOTA_VERSION_0.1.md) | Alcance de la línea base académica y próximos pasos. |

## 8. Herramientas de apoyo

- **GitHub:** alojamiento del repositorio, control de cambios y colaboración.
- **GitHub Issues:** registro y seguimiento de tareas, riesgos y mejoras.
- **GitHub Projects:** organización visual del avance mediante un tablero Kanban.
- **Visual Paradigm Online:** elaboración de diagramas y modelos de diseño.

## 9. Estado actual del proyecto

UniTrack se documenta como un proyecto académico en las etapas de análisis, diseño, arquitectura y planificación. La inclusión de requisitos, modelos y documentos no significa que las funcionalidades estén implementadas ni probadas. El estado de cada tarea debe contrastarse con los Issues y el tablero de GitHub Projects.

## 10. Próximos pasos

1. Revisar los requisitos y criterios de aceptación.
2. Verificar y completar los modelos UML.
3. Confirmar las tareas y sus estados en GitHub Issues y Projects.
4. Iniciar la implementación de los módulos priorizados cuando la etapa de diseño esté validada.
5. Relacionar los cambios de código con Issues y pruebas verificables.

## 11. Repositorio

[Ver el repositorio de UniTrack en GitHub](https://github.com/ericksonsepulveda64-cell/ericksonsepulveda64-cell-UniTrack-Sistema-Gestion-Academica)
