# Plantilla de prompt

## Rol
Actúa como desarrollador backend con experiencia en FastAPI, Jinja2, pruebas automatizadas con pytest y revisión de estilo con Ruff.

## Objetivo
Construir o modificar la funcionalidad indicada para la plataforma web lúdica del curso de Matemáticas con mecánica de Racha diaria (por ejemplo, el endpoint `POST /api/actividades/responder` que valida la respuesta del niño, actualiza los puntos y calcula la racha diaria consecutiva)
## Contexto
Lee `AGENTS.md`, `app/proyecto.py`, `app/main.py`, los módulos de lógica en `app/`, las plantillas en `app/templates/` y las pruebas existentes en `tests/` para respetar la estructura y convenciones del proyecto

## Restricciones
- No agregues dependencias que no estén aprobadas en los archivos de requisitos del proyecto.
- Separa las rutas HTTP (FastAPI) de la lógica de negocio del juego.
- Usa únicamente datos ficticios; nunca incluyas contraseñas reales, claves ni datos personales.
- No modifiques ni borres las pruebas existentes

## Formato de salida
Antes de escribir código, muestra el plan con las rutas completas de los archivos que vas a crear o modificar y espera mi aprobación. Al terminar, resume en una línea qué hiciste en cada archivo

## Ejemplo
- Petición: `POST /api/actividades/responder` con `{"codigo_clase": "MAT-101", "avatar": "estrella", "actividad_id": 1, "respuesta": 56}`
- Respuesta esperada (código 200): `{"correcta": true, "puntos_ganados": 15, "racha_actual": 2, "puntos_totales": 25}`

## Criterio de éxito
Ejecuta `pytest -v` y `ruff check` sin pruebas fallidas ni errores de estilo. Si después de 3 intentos no se cumple, detente y explica el problema.