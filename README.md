# Fake Shop - CI/CD com GitHub Actions

Este repositório contém a aplicação Fake Shop com pipeline CI/CD automatizada usando GitHub Actions para deploy no Kubernetes.

## Pipeline CI/CD

A pipeline automatiza:
- Build da imagem Docker
- Push para o Docker Hub
- Deploy no cluster Kubernetes

## Pré-requisitos

- Conta no GitHub
- Conta no Docker Hub
- Cluster Kubernetes (ex: Digital Ocean Kubernetes)

## Configuração

1. Fork este repositório
2. Adicione os seguintes secrets no seu repositório:
   - `DOCKERHUB_USERNAME`: Seu nome de usuário do Docker Hub
   - `DOCKERHUB_TOKEN`: Token de acesso ao Docker Hub
   - `KUBE_CONFIG`: Arquivo kubeconfig - ex. comando: cat ~/.kube/config
3. A pipeline é executada automaticamente quando:
   - Um push é feito para a branch main
   - Um pull request é aberto para a branch main

## Estrutura do Projeto

- `.github/workflows/`: Contém o arquivo de configuração da pipeline CI/CD
- `k8s/`: Contém os manifestos Kubernetes para o deploy da aplicação