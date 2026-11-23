# Cadastro de Veículos — Dart e Supabase

## Sobre o projeto

Este projeto consiste em uma aplicação desenvolvida em Dart, integrada ao Supabase, com o objetivo de gerenciar o cadastro de veículos de uma concessionária.

O sistema permite realizar operações CRUD (Create, Read, Update e Delete) diretamente pelo terminal, mantendo os dados armazenados em um banco de dados PostgreSQL.

## Funcionalidades

- **Cadastrar veículos:** registra novos veículos no banco de dados.
- **Listar veículos:** exibe todos os veículos cadastrados.
- **Atualizar veículos:** permite modificar as informações de um veículo utilizando seu ID.
- **Excluir veículos:** remove um veículo específico mediante confirmação.
- **Validação de dados:** verifica as informações inseridas pelo usuário.

## Tecnologias utilizadas

- Dart
- Supabase
- PostgreSQL
- Biblioteca Supabase para Dart
- Dotenv

## Estrutura do projeto

```text
CadastroVeiculosDART/
│
├── bin/
│   └── main.dart
│
├── lib/
│   ├── conexao.dart
│   └── veiculos.dart
│
├── .env.example
├── .gitignore
├── pubspec.yaml
├── supabase_setup.sql
└── README.md
```

## Banco de dados

O projeto utiliza uma tabela chamada `veiculos`, criada no Supabase, com os seguintes campos:

| Campo | Tipo |
|---|---|
| id | BIGINT |
| marca | VARCHAR(50) |
| modelo | VARCHAR(100) |
| ano | INTEGER |
| valor | DECIMAL(12,2) |
| quilometragem | INTEGER |

O ID é gerado automaticamente pelo banco de dados.

## Configuração da conexão

1. Crie um projeto no Supabase.
2. Execute o script `supabase_setup.sql` no SQL Editor.
3. Crie um arquivo `.env` na raiz do projeto.
4. Configure as seguintes variáveis:

```env
SUPABASE_URL=sua_url_do_supabase
SUPABASE_PUBLISHABLE_KEY=sua_chave_publicavel
```

**Importante:** não compartilhe o arquivo `.env` nem suas credenciais. O arquivo está protegido pelo `.gitignore`.

## Como executar

Com o Dart SDK instalado, abra o terminal na pasta principal do projeto.

Instale as dependências:

```bash
dart pub get
```

Execute a aplicação:

```bash
dart run bin/main.dart
```

## Menu do sistema

```text
CADASTRO DE VEÍCULOS

1 - Cadastrar veículo
2 - Listar veículos
3 - Atualizar veículo
4 - Excluir veículo
0 - Sair
```

Todas as operações podem ser realizadas durante uma única execução do programa.

## Objetivo acadêmico

Projeto desenvolvido como atividade acadêmica da disciplina de desenvolvimento de software, com foco na utilização da linguagem Dart, integração com banco de dados, operações CRUD e organização do código em diferentes arquivos.

---

**Desenvolvido por:** Marcus Vinicius da Silva Martins
