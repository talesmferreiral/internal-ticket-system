# 📊 Sistema de Gestão de Chamados Internos | Internal Ticket Management System

> 🇧🇷 Projeto desenvolvido na disciplina de **Prototipagem de Sistemas** — 1º semestre de Ciência da Computação.
> 🇺🇸 Project developed in the **Systems Prototyping** course — 1st semester of Computer Science.

---

## 🗺️ Progresso do Projeto | Project Progress

| Etapa | Descrição | Status |
|-------|-----------|--------|
| I | Análise do Processo e Modelagem BPMN (AS-IS) | ✅ Concluída |
| II | Modelagem UML — Casos de Uso e Especificação Textual | ✅ Concluída |
| III | Modelagem UML — Classes e Diagramas Comportamentais | 🔄 Em breve |
| IV | Síntese, Reflexão e Entrega Final | 🔄 Em breve |

---

# 🇧🇷 Português

## 📌 Sobre o Projeto

Este projeto foi desenvolvido como parte da disciplina de Prototipagem de Sistemas no 1º semestre de Ciência da Computação.

O objetivo foi analisar um processo organizacional com problemas reais e propor uma solução digital para melhorar a eficiência operacional, reduzindo retrabalho, atrasos e falta de controle nas solicitações internas.

---

## ⚠️ Problema Identificado

A organização analisada utilizava um processo manual e descentralizado para gerenciar solicitações internas, usando e-mails, mensagens e comunicação verbal. Isso gerava:

- Falta de controle das demandas
- Perda de informações
- Retrabalho
- Atrasos no atendimento
- Baixa rastreabilidade

---

## ✅ Etapa I — Modelagem do Processo Atual (AS-IS)

O processo atual foi modelado utilizando **BPMN**, com 6 raias representando cada stakeholder, evidenciando as falhas operacionais como ausência de sistema integrado, comunicação informal, falta de priorização e stakeholders estratégicos completamente sem visibilidade do processo.

### 👥 Stakeholders identificados

| Stakeholder | Papel | Influência |
|-------------|-------|------------|
| Colaborador | Usuário final — abre solicitações | Média |
| Equipe Suporte / TI | Atende e gerencia os chamados | Alta |
| Gestor de Departamento | Supervisiona e aprova chamados | Alta |
| Administrador do Sistema | Gerencia usuários e configurações | Alta |
| Diretoria | Tomada de decisões estratégicas | Muito Alta |
| RH / Qualidade | Análise de desempenho e melhoria contínua | Média |

### 📊 Diagrama BPMN — Processo AS-IS

![BPMN AS-IS](docs/diagrams/bpmn_as_is.png)

---

## ✅ Etapa II — Modelagem UML: Casos de Uso e Especificação Textual

Nesta etapa foi desenvolvido o **Diagrama de Casos de Uso UML** representando o sistema digital proposto, seguido da especificação textual detalhada dos principais casos de uso com fluxos principal, alternativo e de exceção.

### 🧩 Diagrama de Casos de Uso

![Casos de Uso UML](docs/diagrams/use_case_diagram.svg)

### 📋 Principais Casos de Uso

- Abrir solicitação / chamado interno
- Acompanhar status do chamado em tempo real
- Receber notificações automáticas
- Assumir e atualizar status do chamado
- Encaminhar chamado para outro setor
- Aprovar / rejeitar chamado
- Visualizar dashboard gerencial / KPIs
- Gerar e exportar relatórios
- Gerenciar usuários e permissões
- Configurar categorias e SLAs
- Registrar log de auditoria *(«include»)*
- Emitir alerta de SLA vencido *(«extend»)*

### 📝 Especificação Textual — UC1: Abrir Solicitação

| Campo | Descrição |
|-------|-----------|
| **Ator principal** | Colaborador |
| **Pré-condição** | Usuário autenticado no sistema |
| **Fluxo principal** | Preenche formulário → sistema valida → gera protocolo → notifica |
| **Fluxos alternativos** | Campo vazio, urgência alta, salvar como rascunho |
| **Fluxos de exceção** | Chamado duplicado, falha de conexão, sessão expirada |
| **Pós-condição** | Chamado registrado com protocolo único e notificação enviada |

### 📝 Especificação Textual — UC2: Assumir e Atualizar Status

| Campo | Descrição |
|-------|-----------|
| **Ator principal** | Equipe de Suporte / TI |
| **Pré-condição** | Atendente autenticado e chamado disponível na fila |
| **Fluxo principal** | Assume chamado → executa → registra solução → encerra |
| **Fluxos alternativos** | Encaminhar para outro setor, aguardar informações, solicitar aprovação |
| **Fluxos de exceção** | Chamado já assumido, encerramento sem solução, perda de conexão |
| **Pós-condição** | Chamado atribuído, histórico registrado e colaborador notificado |

---

## 🔄 Etapa III — Em breve: Modelagem UML Avançada

A próxima etapa irá aprofundar a modelagem técnica do sistema com:

- **Diagrama de Classes** — estrutura lógica e relacionamentos entre entidades
- **Diagramas Comportamentais** — sequência, atividades e estados
- **Interpretação integrada** dos modelos produzidos
- **Síntese e reflexão** sobre a arquitetura do sistema

---

## ⚙️ Requisitos do Sistema

### ✅ Funcionais
- Cadastro de chamados com protocolo automático
- Acompanhamento de status em tempo real
- Priorização automática por urgência
- Atribuição de responsáveis
- Registro de histórico completo
- Notificações automáticas
- Relatórios e KPIs gerenciais

### 🔒 Não Funcionais
- Desempenho (resposta < 2 segundos)
- Segurança e controle de acesso
- Usabilidade intuitiva
- Disponibilidade mínima de 99%
- Escalabilidade

---

## 🎯 Solução Proposta

Criação de um **sistema digital integrado** com foco em centralização das informações, automação de processos, melhoria da comunicação entre departamentos, geração de indicadores de desempenho e rastreabilidade completa dos chamados.

---

## 📁 Estrutura do Repositório

```
internal-ticket-system/
├── docs/
│   └── diagrams/
│       ├── bpmn_as_is.svg            # Diagrama BPMN — Processo AS-IS
│       ├── bpmn_as_is.png            # Versão PNG do BPMN
│       └── use_case_diagram.svg      # Diagrama de Casos de Uso UML
└── README.md
```

---

## 📚 Aprendizados

- Levantamento e análise de requisitos
- Modelagem de processos com BPMN
- Identificação e classificação de stakeholders
- Modelagem de sistemas com UML (Casos de Uso)
- Especificação textual de casos de uso com fluxos de exceção
- Pensamento crítico e sistemático antes de programar

---
---

# 🇺🇸 English

## 📌 About the Project

This project was developed as part of a Systems Prototyping course during the first semester of a Computer Science degree.

The goal was to analyze an organizational process with real problems and propose a digital solution to improve operational efficiency, reducing rework, delays, and lack of control over internal requests.

---

## ⚠️ Problem Identified

The analyzed organization managed internal requests through a manual and decentralized process, relying on emails, messages, and verbal communication. This caused:

- Lack of demand control
- Information loss
- Rework
- Service delays
- Low traceability

---

## ✅ Stage I — Current Process Modeling (AS-IS)

The current process was modeled using **BPMN**, with 6 swim lanes representing each stakeholder, highlighting operational failures such as no integrated system, informal communication, lack of prioritization, and strategic stakeholders with no process visibility.

### 👥 Identified Stakeholders

| Stakeholder | Role | Influence |
|-------------|------|-----------|
| Employee | End user — opens requests | Medium |
| Support / IT Team | Handles and manages tickets | High |
| Department Manager | Supervises and approves tickets | High |
| System Administrator | Manages users and settings | High |
| Board / Directors | Strategic decision-making | Very High |
| HR / Quality | Performance analysis and continuous improvement | Medium |

### 📊 BPMN Diagram — AS-IS Process

![BPMN AS-IS](docs/diagrams/bpmn_as_is.png)

---

## ✅ Stage II — UML Modeling: Use Cases and Textual Specification

In this stage, a **UML Use Case Diagram** was developed representing the proposed digital system, followed by a detailed textual specification of the main use cases including main, alternative, and exception flows.

### 🧩 Use Case Diagram

![Use Case Diagram](docs/diagrams/use_case_diagram.svg)

### 📋 Main Use Cases

- Open internal request / ticket
- Track ticket status in real time
- Receive automatic notifications
- Take ownership and update ticket status
- Forward ticket to another department
- Approve / reject ticket
- View management dashboard / KPIs
- Generate and export reports
- Manage users and permissions
- Configure categories and SLAs
- Record audit log *(«include»)*
- Issue SLA breach alert *(«extend»)*

### 📝 Textual Specification — UC1: Open Request

| Field | Description |
|-------|-------------|
| **Primary actor** | Employee |
| **Pre-condition** | User authenticated in the system |
| **Main flow** | Fill out form → system validates → generates protocol → sends notification |
| **Alternative flows** | Empty field, high urgency, save as draft |
| **Exception flows** | Duplicate ticket, connection failure, expired session |
| **Post-condition** | Ticket registered with unique protocol and confirmation sent |

### 📝 Textual Specification — UC2: Take Ownership and Update Status

| Field | Description |
|-------|-------------|
| **Primary actor** | Support / IT Team |
| **Pre-condition** | Attendant authenticated and ticket available in queue |
| **Main flow** | Take ticket → perform service → record solution → close |
| **Alternative flows** | Forward to another department, wait for info, request approval |
| **Exception flows** | Ticket already taken, closure without solution, connection loss |
| **Post-condition** | Ticket assigned, history recorded, employee notified |

---

## 🔄 Stage III — Coming Soon: Advanced UML Modeling

The next stage will deepen the technical modeling of the system with:

- **Class Diagram** — logical structure and relationships between entities
- **Behavioral Diagrams** — sequence, activity, and state diagrams
- **Integrated interpretation** of all produced models
- **Synthesis and reflection** on the system architecture

---

## ⚙️ System Requirements

### ✅ Functional
- Ticket registration with automatic protocol
- Real-time status tracking
- Automatic prioritization by urgency
- Assignee management
- Full history logging
- Automatic notifications
- Reports and management KPIs

### 🔒 Non-Functional
- Performance (response < 2 seconds)
- Security and access control
- Intuitive usability
- Minimum 99% availability
- Scalability

---

## 🎯 Proposed Solution

Creation of an **integrated digital system** focused on centralized information, process and notification automation, improved inter-department communication, performance indicator generation, and full ticket traceability.

---

## 📁 Repository Structure

```
internal-ticket-system/
├── docs/
│   └── diagrams/
│       ├── bpmn_as_is.svg            # BPMN Diagram — AS-IS Process
│       ├── bpmn_as_is.png            # PNG version of BPMN
│       └── use_case_diagram.svg      # UML Use Case Diagram
└── README.md
```

---

## 📚 Key Learnings

- Requirements gathering and analysis
- Process modeling with BPMN
- Stakeholder identification and classification
- System modeling with UML (Use Cases)
- Textual use case specification with exception flows
- Critical and systematic thinking before coding

---

👨‍💻 **Author:** Tales Manfredine Ferreira Lopes — Computer Science Student
