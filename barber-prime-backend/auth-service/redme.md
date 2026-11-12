# BarberPrime — Auth Service

## 1. Sobre o projeto

O `auth-service` é o microsserviço responsável pela autenticação e pelo controle de acesso dos usuários da aplicação BarberPrime.

Sua função é garantir que os usuários possam acessar o sistema de maneira segura, respeitando as permissões definidas.

### Responsabilidades

- Autenticação de usuários.
- Controle de acesso à aplicação.
- Validação das credenciais.
- Gerenciamento de informações relacionadas à identidade e segurança.

---

## 2. Tecnologias utilizadas

- Java
- Spring Boot
- Spring Security
- Spring Data JPA
- Gradle
- PostgreSQL
- Docker

As tecnologias serão configuradas progressivamente durante o desenvolvimento.

---

## 3. Pré-requisitos

Antes de executar o projeto, é necessário ter instalado:

- JDK compatível com a versão configurada no projeto.
- Visual Studio Code ou outra IDE Java.
- Docker Desktop, quando a aplicação utilizar containers.
- PostgreSQL, caso o banco seja executado localmente.

Também é necessário possuir acesso ao terminal do sistema operacional.

---

## 4. Configuração do ambiente

As configurações de ambiente devem ser realizadas antes de iniciar a aplicação.

### Variáveis de ambiente

As credenciais e informações de conexão com o banco de dados devem ser configuradas por meio de variáveis de ambiente.

Exemplo de variáveis:

| Variável | Descrição |
|---|---|
| `DB_URL` | Endereço de conexão com o banco |
| `DB_USERNAME` | Usuário do banco de dados |
| `DB_PASSWORD` | Senha do banco de dados |


As variáveis acima deverão ser utilizadas na configuração do Spring Boot quando a conexão com o banco for implementada.

---

## 5. Executando o projeto

Abra o terminal na pasta raiz do `auth-service`.

### Verificar o Gradle Wrapper

No Windows:

```powershell
.\gradlew.bat --version
```

No Linux ou macOS:

```bash
./gradlew --version
```

### Executar os testes

Windows:

```powershell
.\gradlew.bat test
```

Linux ou macOS:

```bash
./gradlew test
```

### Compilar o projeto

Windows:

```powershell
.\gradlew.bat build
```

Linux ou macOS:

```bash
./gradlew build
```

O comando `build` compila o projeto e executa as verificações configuradas, incluindo os testes.

### Iniciar a aplicação

Windows:

```powershell
.\gradlew.bat bootRun
```

Linux ou macOS:

```bash
./gradlew bootRun
```

A aplicação será iniciada utilizando as configurações definidas no projeto.

---

## 6. Banco de dados

O `auth-service` utilizará PostgreSQL para armazenar os dados necessários à autenticação.

A configuração do banco deverá ser realizada conforme o ambiente de desenvolvimento.

Quando o PostgreSQL estiver configurado, será necessário:

1. Criar o banco de dados do serviço.
2. Configurar as variáveis de conexão.
3. Configurar o Spring Data JPA.
4. Verificar se a aplicação consegue estabelecer conexão.

O banco de dados será configurado de forma independente dos demais microsserviços.

---

## 7. Docker

O serviço poderá ser executado em um container Docker.

A configuração dos containers será centralizada no diretório `infrastructure` do BarberPrime.

O Docker Compose será utilizado para facilitar a inicialização dos serviços e suas dependências.

Os comandos de inicialização e gerenciamento dos containers serão documentados após a implementação da configuração Docker.

---

## 8. Verificação da aplicação

Após iniciar o serviço, verifique:

- Se a aplicação iniciou sem erros.
- Se a conexão com o banco de dados foi estabelecida, quando configurada.
- Se os testes estão sendo executados corretamente.
- Se os endpoints implementados estão respondendo conforme esperado.

Os endpoints disponíveis serão documentados conforme forem desenvolvidos.

---

## 9. Estrutura do projeto

```text
auth-service/
├── gradlew
├── gradlew.bat
├── build.gradle
├── settings.gradle
└── src/
    ├── main/
    │   ├── java/
    │   └── resources/
    └── test/
        └── java/
```

A estrutura poderá ser expandida conforme a implementação das funcionalidades de autenticação.

---

## 10. Segurança

- Não armazenar senhas em texto puro.
- Não publicar credenciais no repositório.
- Utilizar variáveis de ambiente para configurações sensíveis.
- Implementar autenticação e autorização utilizando Spring Security.
- Validar os dados recebidos pela aplicação.

---

## 11. Status do projeto

**Status:** Em desenvolvimento.

O `auth-service` faz parte da arquitetura de microsserviços do BarberPrime.
