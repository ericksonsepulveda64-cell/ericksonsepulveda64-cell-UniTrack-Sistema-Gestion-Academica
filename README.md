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

## 5. Arquitectura seleccionada: frontend y backend

Para el diseño de UniTrack se propone una **arquitectura de tres capas**: presentación (frontend), lógica de aplicación (backend/API) y almacenamiento (base de datos). Esta separación permite distribuir las responsabilidades, facilitar el mantenimiento y reducir el acceso directo a información sensible.

### 5.1 Frontend: interfaz de usuario

El frontend será la parte visible del sistema, utilizada por estudiantes, personal académico y administradores. Su responsabilidad será presentar la información y permitir que los usuarios interactúen con las funciones disponibles.

Responsabilidades principales:

- Mostrar pantallas de inicio de sesión y navegación.
- Presentar calificaciones, asignaturas inscritas y horarios del estudiante.
- Ofrecer formularios para gestionar estudiantes y registrar calificaciones a los usuarios autorizados.
- Validar campos básicos antes de enviar formularios, por ejemplo, comprobar que no estén vacíos.
- Enviar solicitudes al backend y mostrar los resultados o mensajes de error que este devuelva.
- Mantener una interfaz clara y adaptada al tipo de usuario.

El frontend **no debe conectarse directamente a la base de datos** ni decidir por sí solo si un usuario tiene permiso para modificar información. Los controles de seguridad definitivos deben aplicarse en el backend.

### 5.2 Backend: API y lógica de negocio

El backend será la parte encargada de procesar las solicitudes recibidas desde el frontend y aplicar las reglas del sistema. La API servirá como punto de comunicación entre la interfaz y los servicios de datos.

Responsabilidades principales:

- Recibir y responder solicitudes del frontend mediante endpoints definidos.
- Autenticar usuarios y verificar permisos según sus roles.
- Validar la información recibida antes de procesarla.
- Aplicar las reglas de negocio para consultar o gestionar estudiantes, asignaturas, inscripciones, horarios y calificaciones.
- Consultar, registrar o actualizar datos a través de la capa de acceso a datos.
- Devolver respuestas estructuradas, con los datos solicitados o mensajes que indiquen errores.
- Evitar que usuarios no autorizados accedan a información académica o ejecuten operaciones restringidas.

### 5.3 Base de datos: almacenamiento

La base de datos almacenará de forma organizada la información que necesita el sistema, incluyendo usuarios y roles, estudiantes, asignaturas, inscripciones, horarios y calificaciones. El backend será el responsable de realizar las operaciones de lectura y escritura, aplicando las validaciones y permisos correspondientes.

### 5.4 ¿Cómo se comunicarán las partes?

La comunicación propuesta entre frontend y backend se realizará mediante una **API HTTP**, utilizando solicitudes y respuestas en formato JSON. Los endpoints concretos se definirán durante la implementación.

Flujo general de una operación:

1. El usuario inicia una acción en el frontend, por ejemplo, consultar sus calificaciones.
2. El frontend envía una solicitud HTTP al endpoint correspondiente del backend, incluyendo la información necesaria y las credenciales o token de sesión cuando aplique.
3. El backend verifica la autenticación, los permisos y la validez de la solicitud.
4. Si la operación está permitida, el backend consulta la base de datos y procesa los resultados.
5. El backend devuelve una respuesta HTTP con los datos en JSON o con un mensaje de error apropiado.
6. El frontend interpreta la respuesta y presenta la información al usuario.

**Ejemplo:** cuando un estudiante solicita sus calificaciones, el frontend envía una petición al backend; el backend verifica que el estudiante tenga acceso únicamente a sus propios resultados, consulta los datos y devuelve la respuesta para mostrarla en pantalla.

Esta comunicación deberá utilizar HTTPS en un entorno desplegado y proteger los datos personales mediante controles de acceso. El uso de HTTP/JSON y los endpoints descritos corresponde al diseño propuesto; su implementación debe confirmarse durante el desarrollo.

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
