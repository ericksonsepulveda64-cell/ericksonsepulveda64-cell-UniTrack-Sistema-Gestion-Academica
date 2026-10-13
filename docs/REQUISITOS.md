# Requisitos del sistema UniTrack

## 1. Propósito

Este documento reúne los requisitos iniciales identificados para UniTrack – Sistema de Gestión Académica. Deben revisarse con los interesados antes de iniciar una implementación definitiva.

## 2. Actores principales

- **Estudiante:** consulta su información académica autorizada.
- **Personal académico:** registra o consulta información académica según sus permisos.
- **Administrador:** administra cuentas, roles y permisos.

## 3. Requisitos funcionales iniciales

- **RF-01 – Autenticación:** el sistema debe permitir que los usuarios autorizados inicien y cierren sesión.
- **RF-02 – Consulta de calificaciones:** el estudiante debe poder consultar las calificaciones que le corresponden.
- **RF-03 – Consulta de asignaturas inscritas:** el estudiante debe poder visualizar las asignaturas en las que está inscrito.
- **RF-04 – Consulta de horario:** el estudiante debe poder consultar su horario académico.
- **RF-05 – Gestión de estudiantes:** el personal autorizado debe poder registrar, consultar y actualizar datos de estudiantes.
- **RF-06 – Gestión de calificaciones:** el personal autorizado debe poder registrar o actualizar calificaciones, respetando los permisos definidos.

## 4. Requisitos no funcionales iniciales

- **RNF-01 – Seguridad:** el acceso a las funciones debe estar restringido según la identidad, el rol y los permisos del usuario.
- **RNF-02 – Privacidad:** cada usuario solo debe consultar información académica para la que tenga autorización.
- **RNF-03 – Usabilidad:** las pantallas deben presentar opciones y mensajes comprensibles.
- **RNF-04 – Integridad:** el sistema debe validar los datos para evitar registros incompletos o inconsistentes.
- **RNF-05 – Mantenibilidad:** el diseño debe separar la interfaz, la lógica de negocio y el acceso a datos.
- **RNF-06 – Trazabilidad:** los cambios relevantes deben relacionarse con tareas o Issues y documentarse en el repositorio.

## 5. Historias de usuario iniciales

1. **HU-01 – Consulta de calificaciones:** como estudiante, quiero consultar mis calificaciones para conocer mi rendimiento académico.
2. **HU-02 – Consulta de horario:** como estudiante, quiero ver mi horario para organizar mis clases.
3. **HU-03 – Consulta de asignaturas inscritas:** como estudiante, quiero visualizar mis asignaturas inscritas para confirmar mi carga académica.
4. **HU-04 – Registro de calificaciones:** como usuario académico autorizado, quiero registrar calificaciones para mantener actualizada la información académica.
5. **HU-05 – Gestión de estudiantes:** como administrador o personal autorizado, quiero gestionar los datos de estudiantes para mantener el registro académico organizado.

## 6. Criterios de aceptación generales

- El sistema solicita autenticación para las funciones restringidas.
- El usuario solo visualiza datos permitidos por su rol.
- Si no existen datos para una consulta, se muestra un mensaje claro.
- Los formularios validan los campos obligatorios antes de guardar.
- Las operaciones de registro o actualización muestran confirmación o un mensaje de error comprensible.

## 7. Estado y revisión

Estos requisitos constituyen una base inicial de análisis académico. Antes de implementarlos, deben validarse con el alcance acordado, completarse los criterios específicos de aceptación y relacionarse con los Issues correspondientes.