# 📦 Repositorio de Charts de Helm ☸️

Este repositorio contiene los **charts de Helm** utilizados para definir, instalar y actualizar una **aplicación node** 

Estos charts son una parte fundamental de nuestra estrategia de despliegue en **Kubernetes**, facilitando la automatización del despliegue continuo a través de **ArgoCD** y la validación mediante **GitHub Actions**.

---

## 🚀 Tecnologías Clave de Despliegue

Este repositorio está directamente relacionado con las siguientes tecnologías vistas durante el diplomado de arquitectura de software:

- Kubernetes
- Helm
- ArgoCD (para Despliegue Continuo)
- GitHub Actions (para CI de los charts, como linting y testing)
- Docker/DockerHub (Los charts despliegan imágenes de Docker)

---

## 📂 Estructura del Repositorio

Los charts de Helm para cada microservicio se encuentran organizados dentro del directorio `charts/`.

## Loguearse
`helm registry login ghcr.io`

## Como empaquetar en tgz
`helm package charts/vehicles-svc`

## Como pushear con ArgoCD
`helm push vehicles-svc-0.1.0.tgz oci://ghcr.io/edosgn/helm-charts`

## Como instalar el chart manualmente
`helm install <name> charts/vehicles-svc`

!> [!NOTE]

> El name puede ser el nombre del ambiente

## Como desinstalar el chart manualmente
`helm uninstall <name>`
