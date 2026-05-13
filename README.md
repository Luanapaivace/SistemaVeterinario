# 🐾 Sistema Veterinário - Microsserviços

<div align="center">

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![Spring Data JPA](https://img.shields.io/badge/Spring%20Data%20JPA-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Maven](https://img.shields.io/badge/Maven-C71A36?style=for-the-badge&logo=apachemaven&logoColor=white)
![Status](https://img.shields.io/badge/Status-Em%20Desenvolvimento-yellow?style=for-the-badge)

**Um sistema veterinário distribuído em microsserviços independentes para gerenciamento de pets, tutores e agendamentos.**

</div>

---

## 📋 Sobre o Projeto

Este projeto tem como objetivo o desenvolvimento de um **sistema veterinário** utilizando **arquitetura de microsserviços**, aplicando conceitos de separação de responsabilidades, modularização e comunicação entre serviços independentes.

A proposta é dividir as funcionalidades em serviços específicos, permitindo maior organização da aplicação e facilitando futuras manutenções e expansões.

O sistema é composto por **três microsserviços principais**, cada um com responsabilidade bem definida e comunicação via **APIs REST**.

---

## 🗂️ Estrutura dos Microsserviços

| Microsserviço | Responsabilidade |
|---|---|
| 🐶 **Pets** | Gerenciamento dos animais cadastrados |
| 👤 **Tutores** | Gerenciamento dos tutores dos animais |
| 📅 **Agendamentos** | Agendamento e controle de consultas veterinárias |

```text
Sistema Veterinário
│
├── 🐶 Serviço de Pets
├── 👤 Serviço de Tutores
└── 📅 Serviço de Agendamentos
```

---

## 🐶 Microsserviço de Pets

Responsável pelo gerenciamento das informações dos animais cadastrados no sistema.

### ✅ Funcionalidades

- Cadastro de pets
- Atualização de informações
- Remoção de pets
- Listagem de animais cadastrados
- Consulta de informações detalhadas

### 📦 Dados Principais

| Campo | Descrição |
|---|---|
| `id_animal` | Identificador único do animal (PK) |
| `nome` | Nome do animal |
| `especie` | Espécie do animal |
| `raca` | Raça do animal |
| `idade` | Idade do animal |
| `sexo` | Sexo do animal |
| `peso` | Peso do animal |
| `historico_medico` | Histórico médico do animal |
| `id_tutor` | Referência ao tutor (FK) |

---

## 👤 Microsserviço de Tutores

Responsável pelo gerenciamento dos tutores dos animais.

### ✅ Funcionalidades

- Cadastro de tutores
- Atualização cadastral
- Remoção de registros
- Listagem de tutores
- Consulta de informações específicas

### 📦 Dados Principais

| Campo | Descrição |
|---|---|
| `id_tutor` | Identificador único do tutor (PK) |
| `nome_completo_tutor` | Nome completo do tutor |
| `cpf` | CPF do tutor |
| `telefone` | Contato telefônico |
| `rua` | Rua do endereço |
| `numero` | Número do endereço |
| `bairro` | Bairro do endereço |

---

## 📅 Microsserviço de Agendamentos

Responsável pelo agendamento e gerenciamento das consultas veterinárias.

### ✅ Funcionalidades

- Agendamento de consultas
- Atualização de agendamentos
- Cancelamento de agendamentos
- Consulta de histórico
- Listagem de agendamentos

### 📦 Dados Principais

| Campo | Descrição |
|---|---|
| `id_agendamento` | Identificador único do agendamento (PK) |
| `data` | Data da consulta |
| `hora` | Horário da consulta |
| `motivo_consulta` | Motivo do atendimento |
| `id_tutor` | Referência ao tutor (FK) |
| `id_pet` | Referência ao animal (FK) |

---

## 🔗 Comunicação entre os Serviços

Os microsserviços se comunicam por meio de **APIs REST**.

O serviço de **Agendamentos**, por exemplo, realiza requisições ao serviço de **Pets** e ao serviço de **Tutores** para validar a existência do animal e do tutor antes de efetuar um agendamento, garantindo a integridade dos dados entre os serviços.

```
┌──────────────────┐     REST API     ┌────────────────┐
│   Agendamentos   │ ──────────────▶  │     Pets       │
│     Service      │                  │    Service     │
│                  │ ──────────────▶  ├────────────────┤
│                  │     REST API     │    Tutores     │
└──────────────────┘                  │    Service     │
                                      └────────────────┘
```

---

## 🛠️ Tecnologias Utilizadas

| Tecnologia | Finalidade |
|---|---|
| **Java** | Linguagem principal de desenvolvimento |
| **Spring Boot** | Framework para criação dos microsserviços |
| **Spring Data JPA** | Persistência e mapeamento de dados |
| **MySQL** | Banco de dados relacional |
| **Maven** | Gerenciamento de dependências |
| **GitHub** | Controle de versão e colaboração |

---

<div align="center">

✨ **Projeto acadêmico desenvolvido para estudo de Arquitetura de Microsserviços**


</div>
