<div align="center">

<img src="https://cdn-icons-png.flaticon.com/512/2920/2920277.png" alt="Logo do Projeto" width="120" />

# 🚀 Workshop Spring Boot 3 & JPA

**Um projeto de workshop prático focado na construção de uma API RESTful utilizando**
**Spring Boot 3, Spring Data JPA e banco de dados H2 in-memory.**

<br>

![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Gradle](https://img.shields.io/badge/Gradle-02303A?style=for-the-badge&logo=gradle&logoColor=white)
![H2 Database](https://img.shields.io/badge/H2%20Database-FF0000?style=for-the-badge&logo=h2&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)

</div>

---

## 📚 Tabela de Conteúdos

> Navegue rapidamente pelas seções do projeto.

| # | Seção |
|:-:|:------|
| 1 | [📖 Sobre o Projeto](#-sobre-o-projeto) |
| 2 | [✨ Funcionalidades Principais](#-funcionalidades-principais) |
| 3 | [🛠️ Pilha de Tecnologias](#️-pilha-de-tecnologias-tech-stack) |
| 4 | [🔑 Destaques da Arquitetura](#-destaques-da-arquitetura) |
| 5 | [🚀 Começando (Getting Started)](#-começando-getting-started) |
| 6 | [📂 Estrutura de Arquivos](#-estrutura-de-arquivos) |
| 7 | [🤝 Como Contribuir](#-como-contribuir) |
| 8 | [👨‍💻 Autor](#-autor) |
| 9 | [📄 Licença](#-licença) |

---

## 📖 Sobre o Projeto

> Este projeto é um **workshop prático** desenvolvido para demonstrar a configuração de uma aplicação Java do zero.
>
> O objetivo central é cobrir os conceitos essenciais do **Spring Data JPA** para mapeamento objeto-relacional (ORM) e do **Spring Web** na criação de endpoints RESTful.
>
> A aplicação expõe uma API simples para gerenciar **"Usuários"**, rodando sobre um banco **H2 in-memory**, garantindo facilidade nos testes e desenvolvimento contínuo sem a necessidade de configurar bancos externos.

---

## ✨ Funcionalidades Principais

| Ícone | Recurso | Descrição |
|:-----:|:--------|:----------|
| 🌐 | **API RESTful** | Expõe endpoints HTTP (ex: `GET /users`) para operações básicas de consulta. |
| 🗃️ | **Mapeamento JPA** | Usa Spring Data JPA para mapear a classe `User` diretamente na tabela `tb_user`. |
| ⚡ | **Banco H2 Integrado** | Banco em memória configurado para execução e testes instantâneos. |
| 🖥️ | **Console H2 Web** | Interface gráfica ativada para depuração direta em `/h2-console`. |
| 🛠️ | **Automação Gradle** | Gerenciamento completo de dependências e build via wrappers nativos do Gradle. |

---

## 🛠️ Pilha de Tecnologias (Tech Stack)

| Tecnologia | Versão | Função no Projeto |
|:-----------|:------:|:------------------|
| **Java** | 17+ | Linguagem de programação base. |
| **Spring Boot** | 3.x | Framework principal que orquestra a aplicação. |
| **Spring Web** | — | Responsável pela camada de Controllers e endpoints REST. |
| **Spring Data JPA** | — | Interface de persistência de dados e ORM. |
| **H2 Database** | — | Banco de dados relacional leve executado em runtime. |
| **Gradle** | — | Ferramenta de build e gestão de bibliotecas. |
| **Spring Boot Test** | — | Ambiente para testes unitários e de integração. |

---

## 🔑 Destaques da Arquitetura

> O projeto adota o **padrão de camadas clássico** do Spring Boot, isolando responsabilidades de forma clara e escalável.

| Camada | Arquivo | Responsabilidade |
|:-------|:--------|:----------------|
| 🏛️ **Entidade** | `User.java` | Classe de modelo anotada com `@Entity`. Representa os dados persistidos no banco. |
| 🎛️ **Controller** | `UserResource.java` | Recebe as requisições HTTP e retorna as respostas da API REST. |
| ⚙️ **Configuração** | `application.properties` | Centraliza os parâmetros de inicialização e credenciais do banco de dados. |

<details>
<summary><strong>⚙️ Visualizar conteúdo do <code>application.properties</code></strong></summary>

<br>

```properties
# ──────────────────────────────────────────
# Configuração do H2 Database (in-memory)
# ──────────────────────────────────────────
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.username=sa
spring.datasource.password=

# ──────────────────────────────────────────
# Configurações do Console Web H2
# ──────────────────────────────────────────
spring.h2.console.enabled=true

# ──────────────────────────────────────────
# Configurações Gerais da Aplicação
# ──────────────────────────────────────────
spring.application.name=course
```

</details>

---

## 🚀 Começando (Getting Started)

### 📋 Pré-requisitos

| Requisito | Detalhe |
|:----------|:--------|
| **Java (JDK)** | Versão **17 ou superior** instalada e configurada no `PATH`. |
| **IDE** | Recomenda-se **IntelliJ IDEA**, Eclipse ou VS Code com extensões Java. |
| **Gradle** | **Não requer instalação global.** O projeto utiliza o `gradlew` embutido. |

---

### 🔧 Instalação e Execução

**1. Clone o repositório:**

```bash
git clone https://github.com/victorhjsantiago/workshop-springboot3-jpa.git
cd workshop-springboot3-jpa
```

**2. Inicie o servidor Spring Boot:**

```bash
# Linux / macOS
./gradlew bootRun

# Windows
.\gradlew.bat bootRun
```

---

### 🛰️ Acesso aos Endpoints

> Com a aplicação em execução, os seguintes endereços estarão disponíveis:

| Serviço | URL |
|:--------|:----|
| 👤 **Consulta de Usuários** | `http://localhost:8080/users` |
| 🖥️ **Interface do Console H2** | `http://localhost:8080/h2-console` |

**Credenciais de acesso ao Console H2:**

| Campo | Valor |
|:------|:------|
| **JDBC URL** | `jdbc:h2:mem:testdb` |
| **Username** | `sa` |
| **Password** | *(deixe em branco)* |

---

## 📂 Estrutura de Arquivos

```plaintext
workshop-springboot3-jpa/
│
├── 📄 build.gradle                        # Dependências e configuração do Gradle
├── 📄 gradlew                             # Script de inicialização (Linux/macOS)
├── 📄 gradlew.bat                         # Script de inicialização (Windows)
│
├── 📁 gradle/
│   └── 📁 wrapper/                        # Arquivos base do Gradle Wrapper
│
└── 📁 src/
    ├── 📁 main/
    │   ├── 📁 java/com/course/course/
    │   │   ├── 📄 CourseApplication.java        # ▶ Ponto de entrada (main)
    │   │   ├── 📁 entities/
    │   │   │   └── 📄 User.java                 # 🏛 Entidade JPA
    │   │   └── 📁 resources/
    │   │       └── 📄 UserResource.java          # 🎛 Controller REST
    │   └── 📁 resources/
    │       └── 📄 application.properties         # ⚙ Configurações da aplicação
    │
    └── 📁 test/
        └── 📁 java/com/course/course/
            └── 📄 CourseApplicationTests.java    # 🧪 Testes de integração
```

---

## 🤝 Como Contribuir

> Contribuições tornam a comunidade open-source um lugar incrível para aprender e crescer. Qualquer melhoria será muito apreciada!

| Passo | Ação | Comando |
|:-----:|:-----|:--------|
| 1️⃣ | **Fork** | Crie um fork do repositório para a sua conta. |
| 2️⃣ | **Branch** | Crie sua feature branch. | `git checkout -b feature/NovaFeature` |
| 3️⃣ | **Commit** | Salve suas alterações com uma mensagem clara. | `git commit -m 'feat: Adiciona NovaFeature'` |
| 4️⃣ | **Push** | Envie sua branch para o repositório remoto. | `git push origin feature/NovaFeature` |
| 5️⃣ | **Pull Request** | Abra um PR detalhando as mudanças realizadas. | — |

<div align="center">

<br>

**Se este projeto foi útil para os seus estudos, deixe uma estrela ⭐️ no repositório!**

</div>

---

## 👨‍💻 Autor

<div align="center">

<br>

**Victor H. J. Santiago**

<br>

[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/VictorHJesusSantiago)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/victor-henrique-de-jesus-santiago/)

</div>

---

## 📄 Licença

<div align="center">

Este projeto está distribuído sob a **Licença MIT**.
Consulte o arquivo [`LICENSE`](./LICENSE) no repositório para mais informações.

![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)

</div>

---

<div align="center">

*Feito com ☕ e Spring Boot por **Victor H. J. Santiago***

</div>
