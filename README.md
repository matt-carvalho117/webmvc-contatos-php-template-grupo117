Projeto didático desenvolvido para a disciplina **Fundamentos de Sistemas para Internet**.

---

# 📌 Descrição do Projeto

Esta aplicação tem como objetivo demonstrar a organização de uma aplicação PHP utilizando uma arquitetura baseada em camadas.

O projeto apresenta um sistema simples de cadastro de contatos, aplicando conceitos de separação de responsabilidades entre as partes da aplicação.

Fluxo da aplicação:
```text.
Navegador
   ↓
Controller
   ↓
Service
   ↓
Repository
   ↓
Banco de Dados
```

Cada camada possui uma responsabilidade específica:

- **Controller:** recebe as requisições e controla o fluxo da aplicação.
- **Service:** contém as regras de negócio e validações.
- **Repository:** realiza a comunicação com o banco de dados.
- **Database:** gerencia a conexão com o banco.

---

# 🎯 Objetivo

O projeto foi desenvolvido para apresentar na prática:

- organização de projetos PHP;
- separação de código em camadas;
- conexão com banco de dados;
- manipulação de formulários;
- validação de informações;
- utilização do Git e GitHub.

---

# 🚀 Funcionalidades disponíveis 👨‍💻

O sistema possui as seguintes funcionalidades:

- Cadastro de contatos;
- Validação de nome;
- Validação de e-mail;
- Validação de mensagem;
- Salvamento no banco de dados;
- Consulta dos contatos cadastrados;
- Exibição de mensagens de sucesso;
- Exibição de mensagens de erro;
- Comunicação segura com banco utilizando PDO;
- Uso de prepared statements.

---

# 🛠 Tecnologias utilizadas ⌨️

## Backend

- PHP 8+
- PDO
- Apache

## Banco de Dados

- MySQL
- MariaDB

## Frontend

- HTML5
- CSS3

## Ambiente

- XAMPP
- Git
- GitHub

---

# 📋 Requisitos para instalação

Antes de iniciar o projeto, certifique-se de possuir:

- PHP 8 ou superior;
- Apache;
- MySQL ou MariaDB;
- Navegador atualizado;
- XAMPP instalado.

Recomendado:

```text
XAMPP 8.x
PHP 8.x
MySQL 8.x
```

---

# 📂 Estrutura do Projeto

```text
webmvc-contatos-php-template/
│
├── app/
│   │
│   ├── Controllers/
│   │   └── ContatoController.php
│   │
│   ├── Repositories/
│   │   └── ContatoRepository.php
│   │
│   ├── Services/
│   │   └── ContatoService.php
│   │
│   └── Views/
│       └── contatos/
│           └── index.php
│
├── config/
│   │
│   ├── bootstrap.php
│   └── Database.php
│
├── database/
│   └── schema.sql
│
├── docs/
│   │
│   ├── ATIVIDADE_BRANCH_PULL_REQUEST.md
│   ├── GUIA_PROFESSOR_GITHUB.md
│   └── ROTEIRO_ALUNO_XAMPP.md
│
├── public/
│   │
│   ├── assets/
│   │   └── css/
│   │       └── style.css
│   │
│   ├── index.php
│   └── salvar_contato.php
│
├── .github/
│   └── PULL_REQUEST_TEMPLATE.md
│
├── .gitignore
├── LICENSE
└── README.md
```

---

# 📥 Instalação

## 1. Baixar o projeto

Clone o repositório:

```bash
git clone URL_DO_REPOSITORIO
```

ou faça o download do projeto em formato `.zip`.

---

# 2. Colocar no XAMPP

Após baixar o projeto, copie a pasta:

```text
webmvc-contatos-php-template
```

para:

```text
C:\xampp\htdocs\
```

O caminho final deve ficar:

```text
C:\xampp\htdocs\webmvc-contatos-php-template
```

---

# 3. Iniciar o XAMPP

Abra o painel do XAMPP.

Inicie:

```text
Apache
MySQL
```

Os dois serviços devem aparecer como ativos.

---

# 🗄 Configuração do Banco de Dados

Abra:

```text
http://localhost/phpmyadmin
```

---

## Criar o banco

No phpMyAdmin:

1. Clique em importar;
2. Escolha o arquivo:

```text
database/schema.sql
```

3. Execute o arquivo.

O sistema irá criar automaticamente:

- banco de dados;
- tabelas;
- estrutura necessária.

---

# 🔧 Configuração da conexão

Abra:

```text
config/Database.php
```

Configuração padrão:

```text
Servidor:
127.0.0.1

Porta:
3306

Banco:
aula_camadas

Usuário:
root

Senha:
vazia
```

Exemplo:

```php
host = 127.0.0.1
database = aula_camadas
username = root
password = ""
```

Caso seu MySQL tenha senha, altere o campo:

```php
password
```

---

# ▶️ Executando o Projeto

Após configurar o banco:

Acesse:

```text
http://localhost/webmvc-contatos-php-template/public/
```

A tela inicial será exibida.

---

# 🧪 Teste da Aplicação

Para testar:

1. Preencha o nome;
2. Informe um e-mail válido;
3. Digite uma mensagem;
4. Clique em cadastrar.

O sistema deve:

- validar os campos;
- salvar no banco;
- retornar mensagem de sucesso;
- exibir o contato cadastrado.

---

# ⚠️ Solução de Problemas

## Erro: Apache não inicia

Possíveis causas:

- porta 80 ocupada;
- outro servidor rodando.

Solução:

Altere a porta do Apache no XAMPP.

Exemplo:

```text
8080
```

Acesse:

```text
http://localhost:8080/
```

---

## Erro: conexão recusada com banco

Verifique:

Arquivo:

```text
config/Database.php
```

Confira:

- nome do banco;
- usuário;
- senha;
- porta.

---

## Erro: banco não encontrado

Entre no:

```text
phpMyAdmin
```

Execute novamente:

```text
database/schema.sql
```

---

## Erro: página em branco

Verifique:

- erros do PHP;
- versão do PHP;
- caminhos dos arquivos.

---

# 🔐 Segurança Aplicada

O projeto utiliza boas práticas:

## PDO

A conexão com banco é feita usando PDO.

## Prepared Statements

Evita comandos SQL maliciosos.

## Validação de dados

Antes de salvar:

- nome é verificado;
- e-mail é validado;
- mensagem é conferida.

---

# 🌱 Git e GitHub

O projeto utiliza controle de versão.

Comandos básicos:

Ver arquivos modificados:

```bash
git status
```

Adicionar arquivos:

```bash
git add .
```

Criar commit:

```bash
git commit -m "descrição"
```

Enviar alterações:

```bash
git push
```

Atualizar projeto:

```bash
git pull
```

---

# 🔀 Branch e Pull Request

Fluxo recomendado:

Criar uma branch:

```bash
git checkout -b minha-alteracao
```

Fazer alterações.

Enviar:

```bash
git push origin minha-alteracao
```

Depois criar um:

```text
Pull Request
```

no GitHub.

---

# 👨‍🎓 Para alunos

Leia:

```text
docs/ROTEIRO_ALUNO_XAMPP.md
```

e:

```text
docs/ATIVIDADE_BRANCH_PULL_REQUEST.md
```

Contém:

- instalação;
- execução;
- Git;
- branches;
- Pull Request.

---

# 👨‍🏫 Para professor

Consultar:

```text
docs/GUIA_PROFESSOR_GITHUB.md
```

e:

```text
docs/CRIAR_REPOSITORIO_GITHUB.md
```

Inclui:

- orientação do projeto;
- avaliação;
- organização do GitHub.

---

# 📚 Aprendizados

Ao concluir este projeto, é possível compreender:

- estrutura MVC;
- comunicação entre camadas;
- banco de dados com PHP;
- organização profissional de projetos;
- versionamento com Git.

---

**Fundamentos de Sistemas para Internet**