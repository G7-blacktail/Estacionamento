# Estacionamento

## Projeto para aplicação local
Este projeto é uma aplicação que gerencia vagas de estacionamento de estabelecimentos.

## Objetivo
Contabilizar quantidade de vagas, disponibilidade, tempo de permanência do usuário e gerar a cobrança do tempo de permanência.

## Tecnologias
- .NET
- Angular
- MariaDB

Obs.: Este projeto ainda está na fase de desenvolvimento, este repositório será o protótipo da aplicação.

## Status atual do projeto
Até o momento, a base do projeto já foi criada em duas partes principais:

- Backend em .NET com ASP.NET Core, dentro de [src/Estacionamento.API](src/Estacionamento.API)
- Frontend em Angular, dentro de [client-app](client-app)

### Backend
O projeto API já foi inicializado com:
- estrutura padrão do ASP.NET Core
- configuração de OpenAPI
- endpoint inicial `/weatherforecast` gerado pelo template padrão
- arquivo de configuração `Program.cs` com a pipeline básica da aplicação

### Frontend
O projeto Angular já foi inicializado com:
- estrutura padrão do Angular CLI
- módulo principal `AppModule`
- componente principal `AppComponent`
- arquivos de configuração do projeto e ambientes
- roteamento básico da aplicação

### Observação importante
Ainda não há implementação completa do sistema de estacionamento, como cadastro de vagas, controle de entrada/saída, persistência em banco de dados e regras de cobrança. O que existe hoje é a base inicial da aplicação para dar continuidade ao desenvolvimento.

## Como buildar e executar

### Pré-requisitos
- .NET SDK 9+
- Node.js e npm
- Angular CLI (opcional, mas útil para execução local)

### 1. Restaurar e compilar o backend
No diretório raiz do projeto:

```bash
dotnet restore
dotnet build
```

Para rodar a API:

```bash
dotnet run --project src/Estacionamento.API/Estacionamento.APi.csproj
```

A API ficará disponível em uma URL local conforme a configuração da aplicação, normalmente com HTTPS e porta do ASP.NET.

### 2. Instalar dependências do frontend
Acesse a pasta do cliente:

```bash
cd client-app
npm install
```

### 3. Build do frontend
Para compilar o Angular:

```bash
npm run build
```

### 4. Executar o frontend em modo desenvolvimento
```bash
npm start
```

O Angular normalmente será executado em:

```text
http://localhost:4200
```

## Próximos passos
- criar as entidades e regras de negócio do estacionamento
- implementar persistência com MariaDB
- conectar backend e frontend
- criar telas de gestão de vagas, entrada/saída e cobrança
- validar fluxos de uso em ambiente local
