# Prova-V1
repositório para Prova de Junior 


README.TXT

# RH_Empresa.API

# Esta aplicação é uma API REST para gerenciamento de funcionários, férias e histórico de RH,
# desenvolvida em ASP.NET Core com Entity Framework Core e SQL Server.

# ===========================
# PRÉ-REQUISITOS
# ===========================
# - .NET 6 SDK ou superior instalado
# - SQL Server instalado e em execução (pode ser o SQL Server Express)
# - VS Code ou outro editor de sua preferência
# - Extensão SQL Server (mssql) instalada no VS Code (opcional)

# ===========================
# CONFIGURAÇÃO DO BANCO DE DADOS
# ===========================
# 1. Crie um banco de dados chamado RH_Empresa no seu SQL Server.
# 2. Crie um usuário de acesso e defina a senha.
# 3. No arquivo appsettings.json, configure a string de conexão conforme seu ambiente, exemplo:

# "DefaultConnection": "Server=localhost\\SQLEXPRESS;Database=RH_Empresa;User Id=SEU_USUARIO;Password=SUA_SENHA;TrustServerCertificate=True;"

# ===========================
# INSTALAÇÃO DE DEPENDÊNCIAS
# ===========================
# Abra o terminal na pasta do projeto e execute:

dotnet restore   # Restaura as dependências do projeto

# ===========================
# MIGRAÇÕES DO BANCO DE DADOS
# ===========================
# 1. Instale a ferramenta do Entity Framework Core, se necessário:

dotnet tool install --global dotnet-ef   # Instala a ferramenta de migração do EF Core

# 2. Crie a primeira migração:

dotnet ef migrations add InitialCreate   # Cria a primeira migração com base nos modelos

# 3. Atualize o banco de dados:

dotnet ef database update   # Aplica a migração e cria as tabelas no banco

# ===========================
# EXECUTANDO A API
# ===========================
# No terminal, execute:

dotnet run   # Inicia a aplicação

# Aguarde a mensagem informando as URLs onde a API está rodando, por exemplo:
# - https://localhost:5001
# - http://localhost:5000

# ===========================
# TESTANDO A API
# ===========================
# Acesse a documentação Swagger pelo navegador:

# https://localhost:5001/swagger

# Você poderá testar todos os endpoints da API diretamente pelo Swagger.

# ===========================
# OBSERVAÇÕES
# ===========================
# - Se ocorrer erro de certificado SSL, garanta que o parâmetro TrustServerCertificate=True está na string de conexão.
# - Se aparecer erro de tabela já existente, exclua a tabela ou o banco de dados manualmente antes de rodar as migrações.
# - Para ambiente de produção, utilize um certificado válido e configure o acesso ao banco de dados de forma segura.

# Fim do README
