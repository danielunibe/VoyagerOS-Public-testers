# Distribución y actualizaciones públicas

## Canal oficial

Las descargas se publican en [GitHub Releases](https://github.com/danielunibe/VoyagerOS-Public-testers/releases). El historial de cambios está en [CHANGELOG.md](../CHANGELOG.md) y cada release usa la estructura de [RELEASE_NOTES_TEMPLATE.md](RELEASE_NOTES_TEMPLATE.md).

La versión pública inicial es **0.2.1**. La página de releases permanece vacía hasta que exista un instalador verificable.

## Numeración

Usa números `MAJOR.MINOR.PATCH` en el nombre de la release y dentro del EXE. La primera publicación será `0.2.1`; los siguientes números avanzan después de validar la versión anterior. Los nombres visibles de versión no llevan etiquetas de alpha, beta o prueba.

## Contenido de una publicación

Adjunta únicamente materiales de distribución pública:

- Instalador de Windows x64.
- Archivo de sumas SHA-256.
- Manifiesto del paquete y requisitos de instalación.
- Notas con cambios integrados y comprobados, limitaciones confirmadas e instrucciones para actualizar.

El SHA-256 y el estado/editor de Authenticode deben corresponder al instalador adjunto. No publiques código privado, logs de QA, datos de usuario, saves, carpetas de build ni archivos de depuración.

## Actualizar VoyagerOS

Por ahora, las personas obtienen nuevas versiones desde la página **Releases** e instalan el instalador publicado. El EXE actual no consulta GitHub ni descarga actualizaciones automáticamente; la página Releases es el canal manual de actualización. No se anunciará actualización automática hasta que exista y se verifique esa función dentro de la aplicación.

## Estado 0.2.1

**En preparación.** No hay instalador ni release publicados todavía. Las notas de novedades se completarán cuando la candidata pública pase sus gates de procedencia, integridad, firma y aceptación.
