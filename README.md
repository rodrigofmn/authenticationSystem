# 🔐 Authentication System with Permission - Clean Architecture (.NET)

This is an  authentication system developed in ASP.NET Core, utilizando os princípios de **DDD (Domain-Driven Design)** e **Clean Architecture**. O projeto simula um ambiente real de controle de usuários, autenticação JWT, e autorização por permissões de acesso (Admin/User), com código limpo, testável e escalável.

---

## 🧱 Tecnologias Utilizadas

- ASP.NET Core 8
- Entity Framework Core
- JWT (JSON Web Tokens)
- AutoMapper
- FluentValidation
- Swagger
- xUnit (testes)
- PostgreSQL ou SQL Server
- Docker (opcional)

---

## 🎯 Funcionalidades

- ✅ Cadastro de usuário com validação
- ✅ Login com autenticação JWT
- ✅ Geração de Refresh Token
- ✅ Autorização por perfil (Admin / Comum)
- ✅ Consulta de usuários (apenas Admin)
- ✅ Atualização de dados do usuário logado
- ✅ Proteção de rotas via middleware
- ✅ Arquitetura limpa e desacoplada
- ✅ Testes unitários nos casos de uso

---

## 🧠 Arquitetura
/src
/Domain → Entidades e contratos
/Application → Casos de uso, DTOs e serviços
/Infrastructure → Repositórios, banco de dados
/WebApi → Controllers e configuração da API
/tests
/UnitTests → Testes dos casos de uso e domínio


> O projeto segue os princípios de **SOLID**, com separação clara entre camadas, facilitando manutenção e testes.

---

## 🚀 Como Executar Localmente

### Pré-requisitos:
- [.NET 8 SDK](https://dotnet.microsoft.com/en-us/download)
- [PostgreSQL](https://www.postgresql.org/) ou [SQL Server](https://www.microsoft.com/en-us/sql-server/)
- (Opcional) [Docker](https://www.docker.com/)

### Passos:

```bash```
# Clone o repositório
git clone https://github.com/seu-usuario/nome-do-repo.git

# Navegue até o projeto
cd nome-do-repo/src/WebApi

# Execute as migrações (ou configure no appsettings.json)
dotnet ef database update

# Rode a aplicação
dotnet run

Acesse: https://localhost:5001/swagger

## 🔑 Exemplos de Endpoints (via Swagger)
Método	Rota	Acesso	Descrição
POST	/api/auth/register	Público	Cadastra um novo usuário
POST	/api/auth/login	Público	Realiza login e gera tokens
GET	/api/users	Admin	Lista todos os usuários
PUT	/api/users/me	Privado	Atualiza dados do usuário

## 🧪 Testes
Os testes unitários cobrem os principais casos de uso do sistema.

cd tests/UnitTests
dotnet test

## 📦 Próximos passos (Evoluções futuras)
Reset de senha com envio de e-mail

Confirmação de e-mail ao registrar

Painel administrativo com gerenciamento de permissões

Front-end com React e autenticação JWT

Deploy em nuvem (Azure ou Render)

## 👨‍💻 Autor
Rodrigo F. M. Nogueira
Desenvolvedor .NET | Clean Architecture | DDD | APIs

LinkedIn – (https://www.linkedin.com/in/rodrigo-nogueira-37276b1b5/)
GitHub
