# Práctica 7 — CI/CD con GitHub Actions y Kind

Pipeline completamente autocontenido: compila, prueba, valida los ocho Dockerfiles y despliega la plataforma en un clúster Kubernetes **Kind efímero dentro del runner de GitHub Actions**. No usa GCP, no necesita credenciales y no deja infraestructura ni costos al finalizar.

Este repositorio es exclusivo para P7, por lo que el workflow está activo en `.github/workflows/p7-ci-cd.yml`. El clúster Kind existe solamente dentro del runner y no utiliza GCP.

## Ejecución

```bash
git add P5/apps P7 .github/workflows/p7-ci-cd.yml
git commit -m "test: ejecutar pipeline de practica 7"
git push origin main
```

También puede iniciarse desde **GitHub > Actions > P7 CI/CD · Kind efímero > Run workflow**. No hay variables ni secrets que configurar.

La ejecución muestra las fases separadas como en la referencia:

1. preparación/versionamiento;
2. matrices de build Node y Python;
3. matriz de pruebas y validación Helm;
4. matriz de ocho builds Docker;
5. despliegue y smoke test sobre Kind.

La guía técnica, diagrama, criterios de éxito y respuestas teóricas están en [DOCUMENTACION.md](DOCUMENTACION.md).
