# Distribución y actualizaciones públicas

## Canal oficial

Las descargas aprobadas aparecerán en [GitHub Releases](https://github.com/danielunibe/VoyagerOS-Public-testers/releases). El historial público está en [CHANGELOG.md](../CHANGELOG.md), y las notas futuras seguirán la [plantilla de release](RELEASE_NOTES_TEMPLATE.md).

Actualmente no hay versión, tag ni release pública. La versión 0.2.1 mencionada en un borrador anterior nunca se publicó y no está aprobada como versión inicial.

## Estado de las candidatas locales

- La compilación instalada 0.2.24 está marcada PRIVATE_ALPHA, no está firmada y tiene un fallo confirmado de selección rectangular. No distribuir.
- Existe una candidata local 0.2.25 para Windows x64, con instalador y ejecutable que coinciden en versión. El ejecutable coincide con la identidad de compilación y con la huella del worktree actual, pero el worktree está modificado y el canal continúa como PRIVATE_ALPHA.
- Los archivos 0.2.25 no están firmados. La identidad no registra el hash del instalador; por ello no hay una cadena de integridad completa desde el corte de origen hasta el paquete descargable.
- CMake declara el proyecto como 0.2.0 mientras el paquete, ejecutable e identidad reportan 0.2.25. La correspondencia no está documentada y no existe versión pública asignada.
- La instalación, lanzamiento, desinstalación y QA física/visual de esa candidata no se han aceptado. Tampoco están confirmados los términos de redistribución.

Por esas razones, no se ofrece la candidata 0.2.25 en este repositorio.

## Gates de publicación

Cada paquete público debe corresponder a un corte de origen aprobado y a una versión reservada para el canal público. Antes de habilitar la descarga se comprobarán:

- Instalador para una versión de Windows y arquitectura expresamente documentadas.
- Correspondencia de versión y hash entre instalador, ejecutable, módulos de runtime y manifiesto.
- Procedencia del paquete y pruebas asociadas al corte exacto.
- Instalación, primer inicio, actualización manual, desinstalación y recuperación.
- Hash SHA-256 para cada artefacto publicado.
- Estado Authenticode real del instalador y el ejecutable.
- Requisitos, dependencias, limitaciones conocidas y material de soporte.
- Términos de distribución confirmados por el propietario.

## Archivos permitidos

Adjunta únicamente materiales preparados para distribución pública:

- Instalador aprobado.
- Hashes SHA-256 y manifiesto del paquete.
- Notas de versión, requisitos e instrucciones.
- Material visual auténtico revisado para privacidad.

No publiques código fuente privado, registros internos, datos personales, saves, carpetas de build ni archivos de depuración.

## Actualizar VoyagerOS

La aplicación no tiene un actualizador automático verificado. Cuando exista una versión pública, las personas obtendrán los cambios manualmente desde Releases e instalarán el paquete publicado.

## Estado actual

**Preparación; sin versión pública asignada.** Consulta el [preflight público](RELEASE_PREFLIGHT_2026-11-20.md) y las [limitaciones conocidas](KNOWN_LIMITATIONS.md). No descargues ni distribuyas candidatas privadas.
