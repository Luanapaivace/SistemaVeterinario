# 🐾 Sistema Veterinário - Microsserviços

<div align="center">

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![Spring Data JPA](https://img.shields.io/badge/Spring%20Data%20JPA-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Maven](https://img.shields.io/badge/Maven-C71A36?style=for-the-badge&logo=apachemaven&logoColor=white)
![HTML](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![Status](https://img.shields.io/badge/Status-Em%20Desenvolvimento-yellow?style=for-the-badge)

**Um sistema veterinário distribuído em microsserviços independentes para gerenciamento de pets, tutores e agendamentos, com interface web funcional integrada ao backend via API REST.**

</div>

---

## 📋 Sobre o Projeto

Este projeto tem como objetivo o desenvolvimento de um **sistema veterinário** utilizando **arquitetura de microsserviços**, aplicando conceitos de separação de responsabilidades, modularização e comunicação entre serviços independentes.

A proposta é dividir as funcionalidades em serviços específicos, permitindo maior organização da aplicação e facilitando futuras manutenções e expansões.

O sistema conta com **três microsserviços principais**, cada um com responsabilidade bem definida e comunicação via **APIs REST**, além de uma **interface web em HTML/CSS** que permite realizar as operações de CRUD diretamente pelo navegador, consumindo as APIs do backend.

---

## 👥 Equipe e Responsabilidades

Cada microsserviço é desenvolvido e mantido por um(a) integrante responsável, que fica encarregado(a) tanto do **backend** (Spring Boot + JPA) quanto do **frontend** (HTML/CSS) do seu respectivo serviço.

| Integrante | Microsserviço | Responsabilidade |
|---|---|---|
| 👩‍💻 **Rayssa Fialho** | 🐶 Pets | Backend + Interface web do serviço de Pets |
| 👩‍💻 **Luana Oliveira** | 👤 Tutores | Backend + Interface web do serviço de Tutores |
| 👨‍💻 **Gabriel Rolim** | 📅 Agendamentos | Backend + Interface web do serviço de Agendamentos |

---

## 🗂️ Estrutura dos Microsserviços

```text
Sistema Veterinário
│
├── 🐶 Serviço de Pets          → Rayssa Fialho
├── 👤 Serviço de Tutores       → Luana Oliveira
└── 📅 Serviço de Agendamentos  → Gabriel Rolim
```

---

## 🐶 Microsserviço de Pets

> 👩‍💻 **Responsável:** Rayssa Fialho

Responsável pelo gerenciamento das informações dos animais cadastrados no sistema.

### ✅ Funcionalidades

- Cadastro de pets
- Atualização de informações
- Remoção de pets
- Listagem de animais cadastrados
- Consulta de informações detalhadas

### 📦 Modelo de Dados

| Campo | Tipo | Descrição |
|---|---|---|
| `id_animal` | PK | Identificador único do animal |
| `nome` | — | Nome do animal |
| `especie` | — | Espécie do animal |
| `raca` | — | Raça do animal |
| `idade` | — | Idade do animal |
| `sexo` | — | Sexo do animal |
| `peso` | — | Peso do animal |
| `historico_medico` | — | Histórico médico do animal |
| `id_tutor` | FK | Referência ao tutor responsável |

### 🌐 Interface Web

Página HTML/CSS desenvolvida por **Rayssa Fialho** para gerenciamento dos pets via navegador, com as seguintes operações:

| Operação | Descrição |
|---|---|
| ➕ **Create** | Cadastro de novo pet via formulário |
| 📋 **Read** | Listagem e visualização dos pets cadastrados |
| ✏️ **Update** | Edição das informações de um pet |
| 🗑️ **Delete** | Remoção de um pet do sistema |

---

## 👤 Microsserviço de Tutores

> 👩‍💻 **Responsável:** Luana Oliveira

Responsável pelo gerenciamento dos tutores dos animais.

### ✅ Funcionalidades

- Cadastro de tutores
- Atualização cadastral
- Remoção de registros
- Listagem de tutores
- Consulta de informações específicas

### 📦 Modelo de Dados

| Campo | Tipo | Descrição |
|---|---|---|
| `id_tutor` | PK | Identificador único do tutor |
| `nome_completo_tutor` | — | Nome completo do tutor |
| `cpf` | — | CPF do tutor |
| `telefone` | — | Contato telefônico |
| `rua` | — | Rua do endereço |
| `numero` | — | Número do endereço |
| `bairro` | — | Bairro do endereço |

### 🌐 Interface Web

Página HTML/CSS desenvolvida por **Luana Oliveira** para gerenciamento dos tutores via navegador, com as seguintes operações:

| Operação | Descrição |
|---|---|
| ➕ **Create** | Cadastro de novo tutor via formulário |
| 📋 **Read** | Listagem e visualização dos tutores cadastrados |
| ✏️ **Update** | Edição das informações de um tutor |
| 🗑️ **Delete** | Remoção de um tutor do sistema |

---

## 📅 Microsserviço de Agendamentos

> 👨‍💻 **Responsável:** Gabriel Rolim

Responsável pelo agendamento e gerenciamento das consultas veterinárias.

### ✅ Funcionalidades

- Agendamento de consultas
- Atualização de agendamentos
- Cancelamento de agendamentos
- Consulta de histórico
- Listagem de agendamentos

### 📦 Modelo de Dados

| Campo | Tipo | Descrição |
|---|---|---|
| `id_agendamento` | PK | Identificador único do agendamento |
| `data` | — | Data da consulta |
| `hora` | — | Horário da consulta |
| `motivo_consulta` | — | Motivo do atendimento |
| `id_tutor` | FK | Referência ao tutor responsável |
| `id_pet` | FK | Referência ao animal |

### 🌐 Interface Web

Página HTML/CSS desenvolvida por **Gabriel Rolim** para gerenciamento dos agendamentos via navegador, com as seguintes operações:

| Operação | Descrição |
|---|---|
| ➕ **Create** | Agendamento de nova consulta via formulário |
| 📋 **Read** | Listagem e visualização dos agendamentos |
| ✏️ **Update** | Edição de um agendamento existente |
| 🗑️ **Delete** | Cancelamento de um agendamento |

---

## 🔗 Comunicação entre os Serviços

Os microsserviços se comunicam por meio de **APIs REST**.

O serviço de **Agendamentos** realiza requisições ao serviço de **Pets** e ao serviço de **Tutores** para validar a existência do animal e do tutor antes de efetuar um agendamento, garantindo a integridade dos dados entre os serviços.

```
┌──────────────────┐     REST API     ┌────────────────┐
│   Agendamentos   │ ──────────────▶  │     Pets       │
│   (G. Rolim)     │                  │  (R. Fialho)   │
│                  │ ──────────────▶  ├────────────────┤
│                  │     REST API     │    Tutores     │
└──────────────────┘                  │  (L. Oliveira) │
                                      └────────────────┘
```

---

## 🛠️ Tecnologias Utilizadas

### Backend
| Tecnologia | Finalidade |
|---|---|
| **Java** | Linguagem principal de desenvolvimento |
| **Spring Boot** | Framework para criação dos microsserviços |
| **Spring Data JPA** | Persistência e mapeamento de dados |
| **MySQL** | Banco de dados relacional |
| **Maven** | Gerenciamento de dependências |

### Frontend
| Tecnologia | Finalidade |
|---|---|
| **HTML5** | Estrutura das páginas de CRUD |
| **CSS3** | Estilização das interfaces web |

### Outros
| Tecnologia | Finalidade |
|---|---|
| **GitHub** | Controle de versão e colaboração |

---

<div align="center">

✨ **Projeto acadêmico desenvolvido para estudo de Arquitetura de Microsserviços**


</div>
