````markdown
# Tutorial Básico — Criando um Repositório Git

Este tutorial mostra, passo a passo, como criar um **repositório Git local**, desde a criação da pasta do projeto até a criação do primeiro arquivo.

---

## Sumário

- [1. O que será feito](#1-o-que-será-feito)
- [2. O que é necessário](#2-o-que-é-necessário)
  - [2.1 Git instalado](#21-git-instalado)
  - [2.2 Configuração inicial do Git](#22-configuração-inicial-do-git)
  - [2.3 Terminal](#23-terminal)
- [3. Criando a pasta do projeto](#3-criando-a-pasta-do-projeto)
- [4. Entrando na pasta do projeto](#4-entrando-na-pasta-do-projeto)
- [5. Inicializando o repositório Git](#5-inicializando-o-repositório-git)
- [6. O que foi criado pelo `git init`](#6-o-que-foi-criado-pelo-git-init)
- [7. Criando o primeiro arquivo](#7-criando-o-primeiro-arquivo)

---

# 1. O que será feito

Ao final desta primeira etapa, teremos uma estrutura semelhante a:

```text
meu-projeto/
├── .git/
└── README.md
````

O processo será:

```text
Criar pasta
    ↓
Entrar na pasta
    ↓
Inicializar o Git
    ↓
Criar o primeiro arquivo
```

---

# 2. O que é necessário

Antes de criar o repositório, precisamos apenas de três coisas:

* Git instalado;
* Git configurado;
* Um terminal.

---

## 2.1 Git instalado

Verifique se o Git está instalado:

```bash
git --version
```

Exemplo:

```text
git version 2.x.x
```

Se uma versão for exibida, o Git está disponível.

---

## 2.2 Configuração inicial do Git

Configure seu nome:

```bash
git config --global user.name "Seu Nome"
```

Configure seu e-mail:

```bash
git config --global user.email "seu@email.com"
```

Verifique:

```bash
git config --global user.name
git config --global user.email
```

Essas informações serão utilizadas para identificar a autoria dos commits.

---

## 2.3 Terminal

O processo pode ser realizado em qualquer sistema operacional.

### Windows

* PowerShell
* Git Bash
* Prompt de Comando

### macOS

* Terminal
* iTerm

### Linux

* Terminal

Os comandos do Git utilizados neste tutorial são os mesmos:

```bash
git init
git status
git add
git commit
```

---

# 3. Criando a pasta do projeto

Primeiro, vamos criar uma pasta para representar o projeto:

```bash
mkdir meu-projeto
```

`mkdir` significa **make directory**, ou seja, criar um diretório.

O resultado será:

```text
meu-projeto/
```

---

# 4. Entrando na pasta do projeto

Agora precisamos entrar na pasta:

```bash
cd meu-projeto
```

`cd` significa **change directory**, ou seja, alterar o diretório atual.

Para confirmar a localização:

### macOS, Linux e Git Bash

```bash
pwd
```

### PowerShell

```powershell
Get-Location
```

---

# 5. Inicializando o repositório Git

Dentro da pasta do projeto, execute:

```bash
git init
```

O Git informará que um novo repositório vazio foi inicializado.

A partir desse momento, a pasta `meu-projeto` passa a ser um **repositório Git**.

---

# 6. O que foi criado pelo `git init`

Ao executar:

```bash
git init
```

o Git cria uma pasta chamada:

```text
.git/
```

A estrutura agora será:

```text
meu-projeto/
└── .git/
```

A pasta `.git` contém as informações internas necessárias para o Git controlar o projeto, incluindo seu histórico e configurações locais.

> **Importante:** não altere ou apague manualmente a pasta `.git`. Removê-la elimina as informações do repositório Git daquele diretório.

---

# 7. Criando o primeiro arquivo

Agora vamos criar o primeiro arquivo do projeto:

```text
README.md
```

O README será utilizado para documentar e apresentar o projeto.

### Windows — PowerShell

```powershell
Set-Content README.md "# Meu Projeto"
```

### Windows — CMD

```cmd
echo # Meu Projeto > README.md
```

### Git Bash, macOS e Linux

```bash
echo "# Meu Projeto" > README.md
```

A estrutura passa a ser:

```text
meu-projeto/
├── .git/
└── README.md
```

Neste ponto, temos um **repositório Git inicializado contendo o primeiro arquivo do projeto**.

```
```
