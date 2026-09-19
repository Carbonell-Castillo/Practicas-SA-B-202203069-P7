# Evidencia de ejecución

Las evidencias corresponden a ejecuciones reales y exitosas del pipeline. Las capturas se encuentran en [la documentación técnica](../DOCUMENTACION.md#evidencia).

| Evidencia | Valor real |
| --- | --- |
| URL de GitHub Actions | https://github.com/Carbonell-Castillo/Practicas-SA-B-202203069-P7/actions/runs/35408246400 |
| Commit/tag evaluado | `e55c9f466dc1d75b319772bab9baaafde558b564` |
| Fecha | 19/09/2026 |
| Imágenes publicadas | [Listado y verificación GHCR](ghcr-images.md) |

Evidencia disponible en el run:

1. Grafo completo de `P7 CI/CD · Kind efímero` en verde.
2. Matriz `3 · Docker` con sus ocho servicios exitosos.
3. Log de `Prueba de humo del clúster`, mostrando los pods `Ready`.
4. Matriz Docker con el login y push exitoso de las ocho imágenes a GHCR.
5. Página de Packages con las ocho imágenes y el tag SHA evaluado.

El clúster solo existe durante el job; por eso la evidencia se obtiene del log de Actions, no de una consola GCP.
