# MyERP 🧩

Este repositório é um projeto de estudos que simula a evolução de um ERP real, com foco em arquitetura de software moderna, boas práticas de backend/frontend e decisões técnicas que surgem ao longo do crescimento de um sistema.

⚠️ Importante: Este projeto não tem como objetivo ser um ERP pronto para produção, mas sim servir como laboratório para experimentação, aprendizado e validação de conceitos arquiteturais.

## 🎯 Objetivos do Projeto

Simular a construção evolutiva de um ERP real

Explorar padrões de arquitetura utilizados em sistemas corporativos

Entender na prática os desafios de:

- Escalabilidade

- Autenticação e autorização

- Separação de responsabilidades

- Comunicação entre serviços

## 🧠 Principais Conceitos Estudados

Este projeto foca principalmente nos seguintes tópicos:

### 🔐 Autenticação e Autorização

- JWT (JSON Web Token)

- Uso de JWT armazenado em cookies de sessão

Separação entre:

- API de autenticação (Auth API)

- APIs de domínio (API Principal)

- Emissor central de tokens (JWT Issuer)

### 🌐 API Gateway

- Centralização das requisições HTTP

- Validação de autenticação

- Redirecionamento de chamadas por tenant

- Roteamento baseado em paths (/api, /auth, etc.)

- Ponto único de entrada para o frontend

### ⚖️ Load Balancing

- Balanceamento de carga entre instâncias

- Integração com Service Discovery

### 🔍 Service Discovery

- Uso de Eureka para descoberta de serviços

- Comunicação desacoplada entre gateway e APIs

### 🧱 Arquitetura Evolutiva

Estrutura pensada para crescer com o tempo

Possibilidade de:

- Adição de novos módulos

- Extração de novos microsserviços

- Ajustes arquiteturais conforme novas necessidades surgem

### 🖥️ Frontend

Aplicação Next.js

Pode ser utilizada como:

- Web App

- Desktop App

- Distribuição de assets via CDN

- Comunicação exclusiva via API Gateway

### 🗄️ Backend

Atualmente, o backend é composto por:

#### API Gateway

- Autenticação

- Roteamento

- Load balancing

- API Auth

- Cadastro de usuários

- Emissão de JWT

### API Principal

- Regras de negócio