# Práctica 7 — CI/CD con Kind efímero

Repositorio independiente del carnet **202203069** para conservar y ejecutar la Práctica 7 sin interferir con el flujo GitOps de la Práctica 8.

El workflow construye y prueba los microservicios, valida Helm, crea un clúster Kubernetes Kind dentro del runner de GitHub Actions, carga las imágenes, despliega la plataforma con Helm y ejecuta pruebas de humo. El clúster se elimina con el runner al finalizar.

## Características

- No utiliza GCP.
- No requiere kubeconfig ni secretos cloud.
- No publica imágenes en registros externos.
- No deja infraestructura ni costos activos.
- El despliegue existe únicamente dentro del runner efímero.

## Ejecución

El workflow `P7 CI/CD · Kind efímero` se ejecuta automáticamente ante cambios en `P5/apps`, `P7` o su propio archivo sobre `main`. También puede iniciarse manualmente desde la pestaña **Actions** mediante **Run workflow**.

La implementación, arquitectura y criterios de éxito se encuentran en [P7/README.md](P7/README.md) y [P7/DOCUMENTACION.md](P7/DOCUMENTACION.md).

## Estructura

```text
.github/workflows/p7-ci-cd.yml  # pipeline activo
P5/apps/                         # ocho workloads
P7/charts/                       # chart umbrella y subcharts
P7/scripts/                      # build, tests, Helm y despliegue
P7/evidence/                     # evidencia histórica
```

