# Distribución y actualizaciones públicas

## Canal oficial

Las descargas aprobadas aparecerán en [GitHub Releases](https://github.com/danielunibe/VoyagerOS-Public-testers/releases). El historial público está en [CHANGELOG.md](../CHANGELOG.md), y cada publicación debe seguir la estructura de [RELEASE_NOTES_TEMPLATE.md](RELEASE_NOTES_TEMPLATE.md).

Actualmente no hay instalador, tag ni release pública. La versión **0.2.1** que aparecía en un borrador anterior era una etiqueta de planificación; no se publicó y no queda aprobada como versión inicial. El número público se asignará desde una candidata verificable con canal `PUBLIC`.

## Gates de publicación

Cada paquete público debe corresponder a un corte de origen exacto y a una versión reservada para `PUBLIC`. Antes de habilitar la descarga se comprobarán:

- Instalador para la arquitectura y versión de Windows indicadas.
- Procedencia del paquete y correspondencia entre EXE, instalador y versión.
- Pruebas automatizadas asociadas al corte público.
- Instalación, inicio, desinstalación y recuperación documentados y verificados.
- Manifiesto e integridad SHA-256 de los archivos que se adjunten.
- Estado Authenticode real del instalador y del EXE; nunca se describirá como firmado si no tiene una firma válida.
- Requisitos, dependencias, limitaciones conocidas y material de soporte.

La candidata local 0.2.24 revisada durante la preparación está marcada `PRIVATE_ALPHA`, tiene firma `UNSIGNED` y no se generó desde un corte limpio apto para distribución pública. No se ofrece en este repositorio.

## Archivos permitidos

Adjunta únicamente materiales preparados para distribución pública:

- Instalador aprobado.
- Hashes SHA-256 y manifiesto de distribución.
- Notas de versión, requisitos e instrucciones.
- Material visual real que haya sido revisado para privacidad.

No publiques código fuente privado, registros internos, datos personales, saves, carpetas de build ni archivos de depuración.

## Actualizar VoyagerOS

Por ahora, las personas obtendrán las nuevas versiones manualmente desde la página **Releases** e instalarán el paquete publicado. La aplicación no consulta GitHub ni instala actualizaciones automáticamente.

## Estado actual

**Preparación; sin versión pública asignada.** La release permanecerá vacía hasta que haya una candidata `PUBLIC` con procedencia, instalación e integridad verificadas. Consulta el [informe de preflight](RELEASE_PREFLIGHT_2026-11-20.md) para el estado de esta revisión.
