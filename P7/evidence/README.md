# Evidencia de ejecución

Completar después del primer pipeline real; no se incluyen capturas simuladas.

| Evidencia | Valor real |
| --- | --- |
| URL de GitHub Actions | https://github.com/Carbonell-Castillo/Practicas-SA-B-202203069-P7/actions/runs/35400491476 |
| Commit/tag evaluado | `ee89e8797b7548e85d5c77c82da69d664a39b173` |
| Fecha | 18/09/2026 |

Evidencia disponible en el run:

1. Grafo completo de `P7 CI/CD · Kind efímero` en verde.
2. Matriz `3 · Docker` con sus ocho servicios exitosos.
3. Log de `Prueba de humo del clúster`, mostrando los pods `Ready`.
4. Matriz Docker con el login y push exitoso de las ocho imágenes a GHCR.
5. Página de Packages con las ocho imágenes y el tag SHA evaluado.

El clúster solo existe durante el job; por eso la evidencia se obtiene del log de Actions, no de una consola GCP.
