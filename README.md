# Proyecto Final CI/CD

Proyecto práctico de Cloud/DevOps para implementar un flujo de integración continua y despliegue de una aplicación web Python.

## Tecnologías

- Python
- Flask
- Pytest
- Git y GitHub
- GitHub Actions
- Docker
- GitHub Container Registry (GHCR)
- Kubernetes
- Minikube

## Funcionamiento

El flujo del proyecto es:

1. Se desarrolla una aplicación web con Flask.
2. Pytest comprueba automáticamente que la aplicación responde correctamente.
3. El código se almacena en GitHub.
4. Cada push a `main` activa GitHub Actions.
5. GitHub Actions ejecuta los tests.
6. Si los tests pasan, se construye una imagen Docker.
7. La imagen se publica automáticamente en GHCR.
8. Kubernetes despliega la imagen mediante un Deployment.
9. La aplicación se ejecuta dentro de un Pod de Kubernetes.

## Pipeline

Git Push
→ GitHub Actions
→ Pytest
→ Docker Build
→ GHCR
→ Kubernetes
→ Aplicación Flask

## Ejecución en Kubernetes

Aplicar el Deployment:

```bash
kubectl apply -f deployment.yaml
