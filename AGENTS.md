# Contexto del proyecto para agentes

## Proyecto
Plataforma web lúdica para niños, desarrollada con FastAPI.
Curso: Matemáticas. Mecánica: racha diaria.
Roles previstos: docente y niño; el niño entra con código de clase y avatar, sin correo.
El prototipo actual ofrece página de inicio, API básica y soporte PWA; no asumir que los flujos de curso ya existen.

## Stack 
- Python 3.11+, FastAPI y plantillas Jinja2; SQLModel está en dependencias, pero aún no hay modelos implementados.
## Comandos
- Instalar dependencias de desarrollo: `pip install -r requirements-dev.txt`.
- Ejecutar localmente: `uvicorn app.main:app --reload`.
- Probar: `pytest -v`. Revisar estilo: `ruff check .`.

## Estructura y arquitectura
- `app/rutas/`: endpoints y páginas; reciben solicitudes y delegan la lógica de negocio.
- `app/servicios/`: reglas de negocio; `app/modelos/`: modelos de datos. Aún son espacios preparados para crecer.
- `app/templates/`: HTML Jinja2; `app/static/`: CSS, JavaScript, manifiesto, iconos y service worker.
- `tests/`: pruebas automatizadas; `tests/aceptacion/`: pruebas de criterios de aceptación.
- `specs/`: especificación, flujo, plan, tareas y decisiones; consulta estos documentos antes de implementar funcionalidades.

## Convenciones 
- Usa nombres claros en español y sigue los patrones existentes.
- Al iniciar cada sesión, leer STATE.md.
- Mantén las rutas sin reglas de negocio; coloca la lógica en servicios y cúbrela con pruebas.
## Que no hacer
- No inventes requisitos ni presentes funciones planeadas como implementadas; señala dudas antes de tomar decisiones de comportamiento.
- No elimines ni debilites pruebas para hacerlas pasar; añade o actualiza pruebas para cambios de comportamiento.
- No guardes secretos ni uses datos personales reales; usa variables de entorno para secretos.
- Conserva `/sw.js` en la raíz: permite que el service worker controle todo el sitio.
- No hacer commit ni push: los hace el desarrollador.
## Validación y documentación
- Ejecuta las pruebas relacionadas y `ruff check .` después de cambios de código; informa fallos que no puedas resolver.
- Actualiza la documentación directamente relacionada cuando cambie el comportamiento o la forma de ejecutar el proyecto.
- No registres credenciales ni datos personales en código, pruebas o documentación.
## lecciones aprendidas
