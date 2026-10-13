# Modelado UML de UniTrack

## 1. Objetivo

Documentar los modelos UML utilizados o previstos para describir los requisitos, la estructura y los flujos principales de UniTrack. Los archivos gráficos exportados desde Visual Paradigm Online deben conservarse en esta carpeta o en una subcarpeta como `docs/diagramas/` cuando estén disponibles.

## 2. Diagrama de casos de uso

**Actores identificados:**
- Estudiante.
- Personal académico.
- Administrador.

**Casos de uso principales:**
- Iniciar sesión.
- Consultar calificaciones.
- Consultar asignaturas inscritas.
- Consultar horario académico.
- Gestionar estudiantes.
- Registrar o actualizar calificaciones.
- Administrar usuarios, roles y permisos.

El diagrama debe mostrar las asociaciones entre cada actor y los casos de uso autorizados. Las operaciones administrativas no deben asignarse al estudiante.

## 3. Diagrama de componentes / arquitectura

Componentes previstos:
- Frontend.
- Backend / API.
- Autenticación.
- Lógica de negocio.
- Base de datos.

La comunicación debe reflejar que el frontend se comunica con el backend, mientras que el backend coordina la autenticación, la lógica de negocio y el acceso a la base de datos. El frontend no debe acceder directamente a la base de datos.

## 4. Modelo de datos conceptual

Entidades iniciales que conviene representar y validar:
- **Estudiante:** datos de identificación académica.
- **Asignatura:** información de las materias.
- **Inscripción:** relación entre estudiantes y asignaturas.
- **Horario:** programación de las asignaturas o secciones.
- **Calificación:** resultado académico asociado a una inscripción o evaluación.
- **Usuario:** credenciales o referencia de acceso.
- **Rol / Permiso:** autorización para usar funciones del sistema.

Las relaciones y cardinalidades definitivas deben confirmarse en el modelo entidad-relación antes de implementar la base de datos.

## 5. Flujo principal sugerido

Para una consulta de calificaciones: el estudiante inicia sesión, solicita sus calificaciones, el backend valida su autorización, consulta la información correspondiente y devuelve el resultado para mostrarlo en pantalla.

## 6. Evidencia gráfica

Añadir aquí los diagramas exportados desde Visual Paradigm Online, preferiblemente en PNG, SVG o PDF, con nombres descriptivos, por ejemplo:
- `docs/diagramas/casos-de-uso.png`
- `docs/diagramas/componentes-arquitectura.png`
- `docs/diagramas/modelo-datos.png`

**Nota:** las descripciones de este archivo documentan los modelos propuestos; no sustituyen las capturas o exportaciones gráficas originales. No se deben marcar los diagramas como entregados hasta que los archivos reales estén incorporados.