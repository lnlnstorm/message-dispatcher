# Disparador de Mensagens - SENAI

Aplicação desktop desenvolvida em **Java** para gerenciamento de contatos e disparo de mensagens para múltiplos destinatários.

O projeto utiliza **JavaFX** para a interface gráfica, **FXML** para definição das telas, **Maven** para gerenciamento da aplicação e **MySQL** para persistência dos dados.

> Projeto desenvolvido como parte da minha formação em desenvolvimento de software, com foco na aplicação prática de conceitos de programação orientada a objetos, desenvolvimento de interfaces desktop e integração com banco de dados.

---

## 📌 Sobre o projeto

O **Message Dispatcher** é uma aplicação desktop criada para simular um sistema de gerenciamento e envio de mensagens.

A aplicação permite realizar o cadastro e gerenciamento de usuários e contatos, selecionar múltiplos destinatários e enviar mensagens com diferentes informações, além de consultar o histórico de mensagens.

O projeto foi desenvolvido durante uma etapa inicial dos meus estudos em desenvolvimento de software, em um período de desenvolvimento relativamente curto. Por esse motivo, algumas decisões técnicas e aspectos de arquitetura podem ser aprimorados em versões futuras.

O projeto permanece como parte do meu portfólio por representar uma etapa importante da minha evolução prática com **Java, JavaFX, Maven e MySQL**.

---

## ✨ Funcionalidades

### 👤 Usuários

* Cadastro de usuários
* Login por e-mail e senha
* Validação dos dados de cadastro
* Gerenciamento do perfil do usuário
* Alteração da foto de perfil
* Controle da sessão do usuário

### 👥 Contatos

* Listagem de contatos
* Pesquisa de contatos
* Visualização do perfil dos contatos
* Seleção de múltiplos destinatários

### 💬 Mensagens

* Definição de assunto
* Composição do conteúdo da mensagem
* Definição de prioridade
* Seleção de múltiplos destinatários
* Disparo de mensagens
* Consulta do histórico de mensagens

### 🖥️ Interface

* Interface gráfica desenvolvida com JavaFX
* Telas construídas utilizando FXML
* Navegação entre diferentes telas
* Relógio digital na interface

---

## 🛠️ Tecnologias utilizadas

| Tecnologia             | Utilização                       |
| ---------------------- | -------------------------------- |
| **Java 21**            | Linguagem principal              |
| **JavaFX 21**          | Interface gráfica                |
| **FXML**               | Estrutura das telas              |
| **Maven**              | Gerenciamento e build do projeto |
| **MySQL**              | Banco de dados                   |
| **MySQL Connector/J**  | Comunicação com o banco          |
| **NetBeans / VS Code** | Ambiente de desenvolvimento      |

---

## 🏗️ Estrutura do projeto

```text
src/
├── main/
│   ├── java/
│   │   ├── com/mycompany/disparadordemensagens/
│   │   │   ├── controller/
│   │   │   │   ├── CadastroControle.java
│   │   │   │   ├── PerfilContatoController.java
│   │   │   │   ├── PerfilUsuarioControle.java
│   │   │   │   ├── Sessao.java
│   │   │   │   ├── TelaControle.java
│   │   │   │   └── UsuarioControle.java
│   │   │   │
│   │   │   ├── database/
│   │   │   │   └── Conexao.java
│   │   │   │
│   │   │   ├── models/
│   │   │   │   ├── Contato.java
│   │   │   │   └── Mensagem.java
│   │   │   │
│   │   │   └── App.java
│   │   │
│   │   └── module-info.java
│   │
│   └── resources/
│       └── com/mycompany/disparadordemensagens/
│           ├── ConfigUsuario.fxml
│           ├── PerfilContato.fxml
│           ├── Usuario.fxml
│           ├── cadastro.fxml
│           ├── tela.fxml
│           └── img/
│               └── avatar.jpg
│
├── pom.xml
└── .gitignore
```

---

## ⚙️ Pré-requisitos

Para executar o projeto localmente, é necessário ter instalado:

* **JDK 21**
* **Maven**
* **MySQL**
* Uma IDE compatível com projetos Maven, como:

  * NetBeans
  * IntelliJ IDEA
  * Visual Studio Code

---

## 🚀 Como executar

### 1. Clone o repositório

```bash
git clone https://github.com/lnlnstorm/message-dispatcher.git
```

Entre na pasta:

```bash
cd message-dispatcher
```

### 2. Configure o banco de dados

O projeto utiliza um banco de dados MySQL.

Antes de executar a aplicação, é necessário possuir uma instância do MySQL configurada localmente e ajustar as informações de conexão utilizadas pela aplicação.

A configuração da conexão encontra-se em:

```text
src/main/java/com/mycompany/disparadordemensagens/database/Conexao.java
```

Por utilizar uma configuração local, os parâmetros de conexão podem precisar ser adaptados ao ambiente de execução.

### 3. Execute o projeto

Utilizando Maven:

```bash
mvn clean javafx:run
```

Ou execute a classe principal:

```text
com.mycompany.disparadordemensagens.App
```

---

## 🗄️ Banco de dados

A aplicação utiliza **MySQL** para armazenar informações relacionadas aos usuários, contatos e mensagens.

A comunicação com o banco é centralizada na classe:

```text
database/Conexao.java
```

> **Observação:** a configuração atual foi desenvolvida para um ambiente local. Para utilização em um ambiente real, recomenda-se externalizar as credenciais e configurações de conexão por meio de variáveis de ambiente ou arquivos de configuração apropriados.

---

## 🔐 Considerações de segurança

Este projeto possui finalidade **educacional e de portfólio**.

A implementação original não foi projetada seguindo todos os requisitos necessários para um ambiente de produção. Entre os pontos que poderiam ser aprimorados estão:

* armazenamento seguro de senhas;
* utilização de variáveis de ambiente para configurações sensíveis;
* melhoria da arquitetura da aplicação;
* tratamento mais robusto de exceções;
* gerenciamento mais adequado dos arquivos de foto de perfil;
* separação das responsabilidades entre interface, regras de negócio e acesso a dados.

Esses pontos representam oportunidades de evolução técnica do projeto.

---

## 📚 Contexto do desenvolvimento

Este projeto foi desenvolvido durante uma etapa inicial dos meus estudos em desenvolvimento de software, em um período de desenvolvimento relativamente curto.

O principal objetivo foi colocar em prática conceitos de:

* Programação Orientada a Objetos;
* desenvolvimento de aplicações desktop;
* construção de interfaces gráficas;
* utilização de FXML;
* gerenciamento de dependências com Maven;
* integração com banco de dados;
* operações de persistência de dados.

Por ter sido desenvolvido em uma fase inicial da minha trajetória, algumas decisões de arquitetura e implementação podem ser aprimoradas.

Ainda assim, o projeto representa uma etapa importante da minha evolução prática e demonstra a aplicação dos conhecimentos adquiridos naquele período.

---

## 🎯 Objetivos de aprendizado

Durante o desenvolvimento, foram trabalhados conceitos relacionados a:

* Java;
* JavaFX;
* FXML;
* Maven;
* MySQL;
* JDBC;
* organização de projetos Java;
* manipulação de dados;
* validação de informações;
* desenvolvimento de interfaces;
* gerenciamento de eventos;
* controle de sessão;
* integração entre aplicação e banco de dados.

---


## 👨‍💻 Autor

**Iuri**

Projeto desenvolvido para fins de aprendizado, prática e portfólio profissional.

---


