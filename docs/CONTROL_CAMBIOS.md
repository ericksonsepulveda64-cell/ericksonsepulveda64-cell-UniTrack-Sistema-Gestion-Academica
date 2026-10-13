# Control de cambios de UniTrack

## 1. Objetivo

Establecer una práctica sencilla para mantener trazabilidad entre las necesidades académicas, los Issues, los archivos modificados y los commits del repositorio.

## 2. Procedimiento para cambios

1. Identificar la necesidad, corrección o mejora.
2. Registrar o actualizar un Issue con descripción y criterios de aceptación.
3. Modificar únicamente los archivos relacionados con el cambio.
4. Revisar que el contenido sea coherente con los requisitos y la arquitectura.
5. Crear un commit con un mensaje breve y descriptivo.
6. Actualizar el estado del Issue o del tablero según el trabajo realmente realizado.
7. Cuando corresponda, adjuntar evidencia o pruebas verificables.

## 3. Convención sugerida para commits

Usar mensajes que expliquen la acción y el alcance, por ejemplo:
- `docs: documentar requisitos iniciales`
- `docs: describir arquitectura propuesta`
- `docs: agregar referencia a modelos UML`
- `docs: actualizar seguimiento de tareas`
- `fix: corregir validación de datos`

Los ejemplos son convenciones sugeridas, no un historial de commits ya ejecutados.

## 4. Registro de cambios de esta documentación

| Cambio documental | Evidencia esperada |
|---|---|
| README principal | Commit que añade o actualiza `README.md`. |
| Requisitos | Commit que añade o actualiza `docs/REQUISITOS.md`. |
| Arquitectura | Commit que añade o actualiza `docs/ARQUITECTURA.md`. |
| Modelado UML | Commit que añade o actualiza `docs/UML.md` y, cuando existan, los archivos gráficos. |
| Seguimiento y versión | Commits de `docs/SEGUIMIENTO.md` y `docs/NOTA_VERSION_0.1.md`. |

## 5. Regla de trazabilidad

No se debe afirmar que una tarea está terminada únicamente porque existe documentación. El estado debe basarse en el trabajo realizado y en la evidencia disponible.