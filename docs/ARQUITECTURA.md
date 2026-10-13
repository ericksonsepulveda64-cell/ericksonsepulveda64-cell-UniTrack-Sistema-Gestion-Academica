# Arquitectura propuesta de UniTrack

## 1. Enfoque

Se propone una arquitectura por capas que separa la presentación, la autenticación, la lógica de negocio y la persistencia de datos. Esta separación facilita el mantenimiento, las pruebas y la evolución del sistema.

## 2. Componentes y responsabilidades

| Componente | Responsabilidad | Comunicación |
|---|---|---|
| Frontend | Presentar pantallas, formularios, navegación y resultados de consulta. | Envía solicitudes al backend y presenta las respuestas. |
| Backend / API | Recibir solicitudes, validar entradas y coordinar operaciones. | Expone operaciones mediante HTTP/API y procesa las respuestas. |
| Autenticación y autorización | Verificar la identidad y aplicar roles y permisos. | Es utilizada por las operaciones protegidas del backend. |
| Lógica de negocio | Aplicar reglas para estudiantes, asignaturas, inscripciones, horarios y calificaciones. | Recibe solicitudes del backend y coordina las operaciones necesarias. |
| Base de datos | Persistir usuarios y datos académicos. | El acceso se realiza desde el backend, no directamente desde el frontend. |

## 3. Flujo general de una solicitud

1. El usuario realiza una acción en el frontend.
2. El frontend envía la solicitud al backend.
3. El backend verifica la sesión, el rol y los permisos cuando corresponda.
4. La lógica de negocio valida la operación y sus reglas.
5. El backend consulta o modifica los datos mediante la capa de acceso a datos.
6. El backend devuelve una respuesta y el frontend presenta el resultado.

## 4. Principios de diseño

- Separación de responsabilidades.
- Acceso a la base de datos únicamente a través del backend.
- Validación de datos en el servidor, además de las validaciones de interfaz.
- Control de acceso por roles y permisos.
- Registro y trazabilidad de cambios relevantes.
- Pruebas de las reglas de negocio y de la comunicación entre capas.

## 5. Riesgos arquitectónicos iniciales

| Riesgo | Consecuencia posible | Medida de control |
|---|---|---|
| Permisos mal configurados | Acceso no autorizado a información académica. | Definir roles, aplicar autorización en el backend y probar accesos. |
| Validaciones insuficientes | Datos incompletos o inconsistentes. | Establecer reglas de validación y pruebas. |
| Acoplamiento entre interfaz y datos | Mantenimiento más difícil. | Mantener la comunicación mediante la API. |
| Requisitos ambiguos | Retrabajo durante la implementación. | Validar requisitos e historias antes de desarrollar. |

## 6. Estado

Este documento describe la arquitectura propuesta para el proyecto académico. No afirma que los componentes estén implementados. La tecnología concreta y los diagramas finales deben confirmarse con las decisiones y evidencias del proyecto.