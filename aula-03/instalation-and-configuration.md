````markdown
# Git — Instalação, Configuração e Comandos Essenciais do Terminal

> Guia completo para instalar, configurar, verificar e começar a utilizar o Git em Windows, macOS e Linux.
>
> **Objetivo:** preparar uma máquina para trabalhar com Git de forma correta, desde a instalação até a criação do primeiro repositório.
>
> **Escopo:** instalação, configuração, autenticação, comandos básicos do Git e comandos básicos de terminal.

---

## Sumário

- [1. Antes de instalar](#1-antes-de-instalar)
- [2. Instalação no Windows](#2-instalação-no-windows)
- [3. Instalação no macOS](#3-instalação-no-macos)
- [4. Instalação no Linux](#4-instalação-no-linux)
- [5. Verificação da instalação](#5-verificação-da-instalação)
- [6. Configuração inicial do Git](#6-configuração-inicial-do-git)
- [7. Configuração por projeto](#7-configuração-por-projeto)
- [8. Configuração de autenticação com GitHub](#8-configuração-de-autenticação-com-github)
- [9. Primeiro repositório](#9-primeiro-repositório)
- [10. Fluxo básico do Git](#10-fluxo-básico-do-git)
- [11. Comandos básicos do Git](#11-comandos-básicos-do-git)
- [12. Comandos básicos de terminal — Windows](#12-comandos-básicos-de-terminal--windows)
- [13. Comandos básicos de terminal — macOS](#13-comandos-básicos-de-terminal--macos)
- [14. Comandos básicos de terminal — Linux](#14-comandos-básicos-de-terminal--linux)
- [15. Tabela de equivalência de comandos](#15-tabela-de-equivalência-de-comandos)
- [16. Diagnóstico de problemas](#16-diagnóstico-de-problemas)
- [17. Compatibilidade e sistemas antigos](#17-compatibilidade-e-sistemas-antigos)
- [18. Checklist final](#18-checklist-final)
- [19. Referências oficiais](#19-referências-oficiais)

---

# 1. Antes de instalar

Antes de instalar o Git, é importante identificar algumas características da máquina.

### Verifique:

1. Qual é o sistema operacional.
2. Qual é a versão do sistema operacional.
3. Qual é a arquitetura do processador.
4. Qual terminal será utilizado.
5. Se existem versões anteriores do Git instaladas.

### Sistemas mais comuns

```text
Windows
macOS
Linux
````

### Arquiteturas comuns

```text
x64 / AMD64
ARM64
ARM
x86 / 32-bit
```

> **Importante:** "qualquer sistema operacional" não significa que a versão mais recente do Git será compatível com qualquer versão histórica de um sistema. Sistemas antigos podem exigir versões específicas do Git.

A página oficial do Git mantém instruções atualizadas para cada plataforma:

* https://git-scm.com/install/windows
* https://git-scm.com/install/mac
* https://git-scm.com/install/linux

---

# 2. Instalação no Windows

## 2.1 Identificar a arquitetura do Windows

No Windows, abra:

```text
Configurações
→ Sistema
→ Sobre
```

Procure por:

```text
Tipo de sistema
```

Você poderá encontrar algo semelhante a:

```text
Sistema operacional de 64 bits, processador baseado em x64
```

ou:

```text
Sistema operacional de 64 bits, processador baseado em ARM
```

---

## 2.2 Instalação pelo instalador gráfico

A forma mais simples para a maioria dos usuários é utilizar o **Git for Windows**.

Acesse:

https://git-scm.com/install/windows

Baixe o instalador correspondente à arquitetura da máquina.

Depois:

1. Execute o instalador.
2. Aceite a licença.
3. Escolha o diretório de instalação.
4. Continue pelas opções do instalador.
5. Mantenha as configurações padrão caso não exista uma necessidade específica de alterá-las.
6. Finalize a instalação.

Após a instalação, abra um novo terminal.

Você pode utilizar:

```text
Git Bash
PowerShell
Prompt de Comando
```

Verifique:

```bash
git --version
```

Exemplo:

```text
git version 2.x.x
```

---

## 2.3 Git Bash

O Git for Windows disponibiliza o **Git Bash**.

O Git Bash fornece um ambiente de terminal baseado em ferramentas Unix-like dentro do Windows.

Exemplo:

```bash
pwd
ls
cd
mkdir
touch
rm
```

Isso facilita a utilização de comandos semelhantes aos encontrados em macOS e Linux.

Site oficial:

https://gitforwindows.org/

---

## 2.4 Instalação utilizando Winget

Em versões do Windows com o Windows Package Manager instalado:

```powershell
winget install --id Git.Git -e --source winget
```

Depois:

```powershell
git --version
```

---

## 2.5 Windows ARM64

Em máquinas Windows com arquitetura ARM64, utilize o instalador ARM64 quando disponível.

A página oficial mantém as versões correspondentes:

https://git-scm.com/install/windows

---

## 2.6 Sistemas Windows antigos

Nem todas as versões atuais do Git for Windows são compatíveis com versões antigas do Windows.

Antes de instalar uma versão antiga, consulte:

https://gitforwindows.org/requirements.html

A regra deve ser:

```text
Identificar o Windows
        ↓
Verificar compatibilidade
        ↓
Escolher uma versão compatível
        ↓
Instalar
        ↓
Verificar
```

Não é recomendado instalar uma versão antiga simplesmente porque ela "parece funcionar".

---

# 3. Instalação no macOS

Existem diferentes maneiras de instalar o Git no macOS.

As opções mais comuns são:

```text
Xcode Command Line Tools
Homebrew
MacPorts
```

---

## 3.1 Xcode Command Line Tools

Abra o Terminal e execute:

```bash
xcode-select --install
```

O macOS exibirá uma janela para instalação das ferramentas.

Depois:

```bash
git --version
```

Caso o Git esteja disponível, uma versão será exibida.

---

## 3.2 Homebrew

Caso o Homebrew esteja instalado:

```bash
brew install git
```

Depois:

```bash
git --version
```

Para verificar onde o Git está instalado:

```bash
which git
```

Também é possível verificar todas as ocorrências encontradas:

```bash
type -a git
```

---

## 3.3 MacPorts

Caso utilize MacPorts:

```bash
sudo port install git
```

Depois:

```bash
git --version
```

---

## 3.4 Verificar o shell

O macOS moderno utiliza normalmente o `zsh`.

Verifique:

```bash
echo $SHELL
```

Exemplo:

```text
/bin/zsh
```

Isso não altera o funcionamento básico do Git. O objetivo é apenas identificar qual shell está sendo utilizado.

---

# 4. Instalação no Linux

No Linux, a instalação normalmente é realizada pelo gerenciador de pacotes da própria distribuição.

---

## 4.1 Debian e Ubuntu

Atualize os índices:

```bash
sudo apt update
```

Instale o Git:

```bash
sudo apt install git
```

Verifique:

```bash
git --version
```

---

## 4.2 Ubuntu com pacote upstream

Quando houver necessidade de utilizar uma versão mais recente disponibilizada por um repositório específico, consulte a documentação oficial do Git:

https://git-scm.com/install/linux

Uma alternativa conhecida para Ubuntu é o PPA do Git Core:

```bash
sudo add-apt-repository ppa:git-core/ppa
sudo apt update
sudo apt install git
```

Não utilize repositórios adicionais sem entender de onde os pacotes estão vindo.

---

## 4.3 Fedora

```bash
sudo dnf install git
```

Depois:

```bash
git --version
```

---

## 4.4 RHEL e derivados

Em sistemas modernos:

```bash
sudo dnf install git
```

Em sistemas antigos:

```bash
sudo yum install git
```

A disponibilidade e a versão podem depender da versão da distribuição e dos repositórios habilitados.

---

## 4.5 Arch Linux

```bash
sudo pacman -S git
```

---

## 4.6 openSUSE

```bash
sudo zypper install git
```

---

## 4.7 Alpine Linux

```bash
apk add git
```

Em ambientes que exigem privilégios administrativos:

```bash
sudo apk add git
```

---

## 4.8 Outras distribuições

Outras distribuições podem utilizar gerenciadores diferentes.

O princípio permanece:

```text
Identificar distribuição
        ↓
Identificar gerenciador de pacotes
        ↓
Instalar git
        ↓
Verificar versão
```

Consulte:

https://git-scm.com/install/linux

---

# 5. Verificação da instalação

Depois da instalação, o primeiro comando deve ser:

```bash
git --version
```

Exemplo:

```text
git version 2.x.x
```

---

## 5.1 Windows — CMD

Descobrir onde o executável está:

```cmd
where git
```

---

## 5.2 Windows — PowerShell

```powershell
Get-Command git
```

Para localizar todas as versões encontradas:

```powershell
Get-Command git -All
```

---

## 5.3 Git Bash

```bash
which git
```

---

## 5.4 macOS e Linux

```bash
which git
```

ou:

```bash
type -a git
```

---

## 5.5 Confirmar a versão

```bash
git --version
```

A sequência recomendada é:

```text
git --version
        ↓
localizar o executável
        ↓
confirmar que o terminal reconhece o Git
```

---

# 6. Configuração inicial do Git

Depois da instalação, o Git precisa ser configurado.

A configuração mais importante é a identidade utilizada nos commits.

---

## 6.1 Configurar nome

```bash
git config --global user.name "Seu Nome"
```

Exemplo:

```bash
git config --global user.name "Gabriel Oliveira"
```

---

## 6.2 Configurar e-mail

```bash
git config --global user.email "seu-email@example.com"
```

Utilize o endereço que deverá aparecer associado aos seus commits.

---

## 6.3 Verificar nome e e-mail

```bash
git config --global user.name
```

```bash
git config --global user.email
```

---

## 6.4 O que significa `--global`?

O parâmetro:

```bash
--global
```

faz com que a configuração seja aplicada ao usuário atual da máquina.

Exemplo:

```bash
git config --global user.name "Seu Nome"
```

Essa configuração será utilizada por padrão nos repositórios desse usuário.

---

## 6.5 Configuração local do projeto

Dentro de um repositório:

```bash
git config user.name "Nome específico"
```

Essa configuração será válida apenas naquele repositório.

---

## 6.6 Configurar o branch inicial

Atualmente, `main` é um nome amplamente utilizado para o branch principal.

Para configurar o Git para utilizar `main` ao criar novos repositórios:

```bash
git config --global init.defaultBranch main
```

Verifique:

```bash
git config --global init.defaultBranch
```

---

## 6.7 Configurar editor

O Git pode precisar abrir um editor de texto durante determinadas operações.

### VS Code

```bash
git config --global core.editor "code --wait"
```

### Vim

```bash
git config --global core.editor "vim"
```

### Nano

```bash
git config --global core.editor "nano"
```

---

## 6.8 Configuração de finais de linha

Uma configuração importante, principalmente em projetos multiplataforma, é:

```text
core.autocrlf
```

### Windows

Uma configuração frequentemente utilizada:

```bash
git config --global core.autocrlf true
```

### macOS/Linux

Uma configuração comum:

```bash
git config --global core.autocrlf input
```

Essa configuração deve ser adotada conscientemente em equipes que trabalham em diferentes sistemas operacionais.

---

## 6.9 Cores no terminal

Para habilitar cores:

```bash
git config --global color.ui auto
```

---

## 6.10 Visualizar configurações

```bash
git config --list
```

Para saber de qual arquivo cada configuração veio:

```bash
git config --list --show-origin
```

Essa segunda opção é extremamente útil para diagnosticar conflitos de configuração.

---

# 7. Configuração por projeto

O Git possui diferentes níveis de configuração.

De forma simplificada:

```text
System
   ↓
Global
   ↓
Local
```

A configuração mais específica normalmente prevalece.

---

## 7.1 Configuração global

```bash
git config --global user.name "Seu Nome"
```

Aplica-se ao usuário.

---

## 7.2 Configuração local

Dentro do repositório:

```bash
git config user.name "Nome do Projeto"
```

Aplica-se apenas ao repositório atual.

---

## 7.3 Ver configurações

```bash
git config --list --show-origin
```

---

# 8. Configuração de autenticação com GitHub

Git e GitHub são ferramentas diferentes.

O Git executa operações de versionamento.

O GitHub hospeda e disponibiliza repositórios e funcionalidades colaborativas.

Para enviar código ao GitHub, é necessário autenticar a máquina.

Existem dois métodos principais:

```text
SSH
HTTPS
```

---

## 8.1 SSH

Verifique se já existe uma chave:

```bash
ls ~/.ssh
```

Procure arquivos como:

```text
id_ed25519
id_ed25519.pub
```

---

## 8.2 Criar chave SSH

Utilize:

```bash
ssh-keygen -t ed25519 -C "seu-email@example.com"
```

Pressione `Enter` para aceitar o caminho padrão ou informe outro.

---

## 8.3 Iniciar o ssh-agent

macOS/Linux/Git Bash:

```bash
eval "$(ssh-agent -s)"
```

Depois:

```bash
ssh-add ~/.ssh/id_ed25519
```

---

## 8.4 Copiar a chave pública

A chave pública normalmente está em:

```text
~/.ssh/id_ed25519.pub
```

Exibir:

```bash
cat ~/.ssh/id_ed25519.pub
```

Copie o conteúdo inteiro.

Nunca compartilhe a chave privada:

```text
id_ed25519
```

A chave que pode ser adicionada ao GitHub é:

```text
id_ed25519.pub
```

---

## 8.5 Adicionar a chave ao GitHub

No GitHub:

```text
Settings
→ SSH and GPG keys
→ New SSH key
```

Cole sua chave pública.

---

## 8.6 Testar SSH

```bash
ssh -T git@github.com
```

Uma autenticação bem-sucedida retornará uma mensagem indicando que o GitHub reconheceu a chave.

---

## 8.7 HTTPS

Também é possível utilizar URLs HTTPS:

```text
https://github.com/usuario/repositorio.git
```

Para autenticação, o GitHub não utiliza mais senha comum da conta para operações Git sobre HTTPS.

Pode ser necessário utilizar:

```text
Personal Access Token
```

ou um gerenciador de credenciais.

Consulte:

https://docs.github.com/

---

# 9. Primeiro repositório

Agora que o Git está instalado e configurado, podemos criar um repositório.

---

## 9.1 Criar uma pasta

```bash
mkdir meu-projeto
```

---

## 9.2 Entrar na pasta

```bash
cd meu-projeto
```

---

## 9.3 Inicializar o Git

```bash
git init
```

O Git criará uma estrutura interna:

```text
.git/
```

A pasta `.git` contém os dados necessários para o controle de versão.

---

## 9.4 Verificar o estado

```bash
git status
```

---

## 9.5 Criar um README

macOS/Linux/Git Bash:

```bash
echo "# Meu Projeto" > README.md
```

PowerShell:

```powershell
Set-Content README.md "# Meu Projeto"
```

---

## 9.6 Adicionar o arquivo

```bash
git add README.md
```

---

## 9.7 Criar o commit

```bash
git commit -m "docs: add README"
```

---

## 9.8 Ver histórico

```bash
git log --oneline
```

---

# 10. Fluxo básico do Git

O fluxo mais importante para quem está começando é:

```text
Arquivo
   ↓
Working Tree
   ↓
git add
   ↓
Staging Area
   ↓
git commit
   ↓
Repository
```

Quando o GitHub entra no processo:

```text
Repository local
       ↓
git push
       ↓
GitHub
```

Para receber alterações:

```text
GitHub
   ↓
git fetch / git pull
   ↓
Repository local
```

---

# 11. Comandos básicos do Git

## `git --version`

Verifica a versão instalada:

```bash
git --version
```

---

## `git config`

Gerencia configurações:

```bash
git config --list
```

---

## `git init`

Cria um novo repositório:

```bash
git init
```

---

## `git clone`

Clona um repositório existente:

```bash
git clone URL
```

Exemplo:

```bash
git clone https://github.com/usuario/projeto.git
```

---

## `git status`

Mostra o estado atual do repositório:

```bash
git status
```

---

## `git add`

Adiciona alterações à staging area.

Um arquivo:

```bash
git add arquivo.txt
```

Todos os arquivos:

```bash
git add .
```

---

## `git commit`

Cria um commit:

```bash
git commit -m "mensagem"
```

Exemplo:

```bash
git commit -m "feat: add login"
```

---

## `git log`

Exibe o histórico:

```bash
git log
```

Versão resumida:

```bash
git log --oneline
```

---

## `git diff`

Mostra alterações ainda não adicionadas à staging area:

```bash
git diff
```

---

## `git branch`

Lista branches:

```bash
git branch
```

Criar branch:

```bash
git branch feature/login
```

---

## `git switch`

Trocar de branch:

```bash
git switch feature/login
```

Criar e entrar diretamente:

```bash
git switch -c feature/login
```

---

## `git merge`

Integra alterações de um branch em outro:

```bash
git merge feature/login
```

---

## `git remote`

Lista repositórios remotos:

```bash
git remote -v
```

---

## `git fetch`

Busca informações do remoto sem integrar automaticamente as alterações:

```bash
git fetch
```

---

## `git pull`

Busca alterações e tenta integrá-las:

```bash
git pull
```

---

## `git push`

Envia commits para um repositório remoto:

```bash
git push
```

Na primeira publicação de um branch:

```bash
git push -u origin main
```

---

# 12. Comandos básicos de terminal — Windows

O Windows possui diferentes ambientes de terminal.

Os principais são:

```text
Prompt de Comando (CMD)
PowerShell
Git Bash
```

---

## 12.1 Ver diretório atual

### CMD

```cmd
cd
```

### PowerShell

```powershell
Get-Location
```

### Git Bash

```bash
pwd
```

---

## 12.2 Listar arquivos

### CMD

```cmd
dir
```

### PowerShell

```powershell
Get-ChildItem
```

Também:

```powershell
ls
```

### Git Bash

```bash
ls
```

Arquivos ocultos:

```bash
ls -la
```

---

## 12.3 Entrar em uma pasta

```text
cd nome-da-pasta
```

Exemplo:

```bash
cd projetos
```

---

## 12.4 Voltar

```bash
cd ..
```

---

## 12.5 Ir para a pasta do usuário

PowerShell:

```powershell
cd ~
```

Git Bash:

```bash
cd ~
```

---

## 12.6 Criar pasta

### CMD / PowerShell

```cmd
mkdir projetos
```

### Git Bash

```bash
mkdir projetos
```

---

## 12.7 Criar arquivo

### PowerShell

```powershell
New-Item arquivo.txt
```

### CMD

```cmd
type nul > arquivo.txt
```

### Git Bash

```bash
touch arquivo.txt
```

---

## 12.8 Copiar

### PowerShell

```powershell
Copy-Item arquivo.txt copia.txt
```

### CMD

```cmd
copy arquivo.txt copia.txt
```

### Git Bash

```bash
cp arquivo.txt copia.txt
```

---

## 12.9 Mover ou renomear

### PowerShell

```powershell
Move-Item arquivo.txt novo.txt
```

### CMD

```cmd
move arquivo.txt novo.txt
```

### Git Bash

```bash
mv arquivo.txt novo.txt
```

---

## 12.10 Excluir

### PowerShell

```powershell
Remove-Item arquivo.txt
```

### CMD

```cmd
del arquivo.txt
```

### Git Bash

```bash
rm arquivo.txt
```

> Tenha cuidado com comandos de remoção executados pelo terminal.

---

## 12.11 Limpar terminal

### CMD

```cmd
cls
```

### PowerShell

```powershell
Clear-Host
```

Também:

```powershell
cls
```

### Git Bash

```bash
clear
```

---

## 12.12 Ler arquivo

### PowerShell

```powershell
Get-Content arquivo.txt
```

### CMD

```cmd
type arquivo.txt
```

### Git Bash

```bash
cat arquivo.txt
```

---

## 12.13 Localizar executável

### CMD

```cmd
where git
```

### PowerShell

```powershell
Get-Command git
```

### Git Bash

```bash
which git
```

---

# 13. Comandos básicos de terminal — macOS

O terminal do macOS utiliza uma estrutura Unix-like.

Em versões modernas, o shell padrão é normalmente o `zsh`.

---

## 13.1 Diretório atual

```bash
pwd
```

---

## 13.2 Listar arquivos

```bash
ls
```

Detalhado:

```bash
ls -l
```

Com arquivos ocultos:

```bash
ls -la
```

---

## 13.3 Entrar em pasta

```bash
cd projetos
```

---

## 13.4 Voltar

```bash
cd ..
```

---

## 13.5 Ir para a Home

```bash
cd ~
```

---

## 13.6 Criar pasta

```bash
mkdir projetos
```

Criar estrutura completa:

```bash
mkdir -p projetos/web/src
```

---

## 13.7 Criar arquivo

```bash
touch arquivo.txt
```

---

## 13.8 Copiar

```bash
cp arquivo.txt copia.txt
```

Diretório:

```bash
cp -R pasta destino
```

---

## 13.9 Mover ou renomear

```bash
mv arquivo.txt novo.txt
```

---

## 13.10 Excluir

```bash
rm arquivo.txt
```

Diretório:

```bash
rm -r pasta
```

---

## 13.11 Ler arquivo

```bash
cat arquivo.txt
```

Para arquivos grandes:

```bash
less arquivo.txt
```

---

## 13.12 Limpar terminal

```bash
clear
```

---

## 13.13 Encontrar executável

```bash
which git
```

Todas as ocorrências:

```bash
type -a git
```

---

# 14. Comandos básicos de terminal — Linux

Os comandos abaixo são comuns na maioria dos ambientes Linux.

---

## 14.1 Diretório atual

```bash
pwd
```

---

## 14.2 Listar arquivos

```bash
ls
```

Detalhado:

```bash
ls -l
```

Ocultos:

```bash
ls -la
```

---

## 14.3 Navegar

```bash
cd projetos
```

Voltar:

```bash
cd ..
```

Home:

```bash
cd ~
```

---

## 14.4 Criar diretório

```bash
mkdir projetos
```

Estrutura completa:

```bash
mkdir -p projetos/web/src
```

---

## 14.5 Criar arquivo

```bash
touch arquivo.txt
```

---

## 14.6 Copiar

```bash
cp arquivo.txt copia.txt
```

Diretório:

```bash
cp -r pasta destino
```

---

## 14.7 Mover ou renomear

```bash
mv arquivo.txt novo.txt
```

---

## 14.8 Remover

```bash
rm arquivo.txt
```

Diretório:

```bash
rm -r pasta
```

---

## 14.9 Exibir conteúdo

```bash
cat arquivo.txt
```

Ou:

```bash
less arquivo.txt
```

---

## 14.10 Limpar terminal

```bash
clear
```

---

## 14.11 Localizar comandos

```bash
which git
```

Ou:

```bash
type -a git
```

---

# 15. Tabela de equivalência de comandos

| Ação            | Windows CMD          | PowerShell        | Git Bash    | macOS/Linux |
| --------------- | -------------------- | ----------------- | ----------- | ----------- |
| Diretório atual | `cd`                 | `Get-Location`    | `pwd`       | `pwd`       |
| Listar arquivos | `dir`                | `Get-ChildItem`   | `ls`        | `ls`        |
| Entrar em pasta | `cd pasta`           | `cd pasta`        | `cd pasta`  | `cd pasta`  |
| Voltar          | `cd ..`              | `cd ..`           | `cd ..`     | `cd ..`     |
| Pasta Home      | `%USERPROFILE%`      | `~`               | `~`         | `~`         |
| Criar pasta     | `mkdir`              | `mkdir`           | `mkdir`     | `mkdir`     |
| Criar arquivo   | `type nul > arquivo` | `New-Item`        | `touch`     | `touch`     |
| Copiar          | `copy`               | `Copy-Item`       | `cp`        | `cp`        |
| Mover           | `move`               | `Move-Item`       | `mv`        | `mv`        |
| Excluir         | `del`                | `Remove-Item`     | `rm`        | `rm`        |
| Limpar terminal | `cls`                | `Clear-Host`      | `clear`     | `clear`     |
| Ler arquivo     | `type`               | `Get-Content`     | `cat`       | `cat`       |
| Localizar Git   | `where git`          | `Get-Command git` | `which git` | `which git` |

> Os comandos possuem funções equivalentes, mas não necessariamente o mesmo comportamento ou as mesmas opções.

---

# 16. Diagnóstico de problemas

## 16.1 `git` não é reconhecido

### Windows

Mensagem comum:

```text
'git' is not recognized as an internal or external command
```

### macOS/Linux

Mensagem comum:

```text
git: command not found
```

---

## 16.2 Verificar se o Git existe

### CMD

```cmd
where git
```

### PowerShell

```powershell
Get-Command git
```

### Git Bash/macOS/Linux

```bash
which git
```

Depois:

```bash
git --version
```

---

## 16.3 Possíveis causas

```text
Git não instalado
        ↓
PATH incorreto
        ↓
Terminal aberto antes da instalação
        ↓
Mais de uma instalação do Git
        ↓
Versão incorreta
```

Feche e abra novamente o terminal após instalar o Git.

---

## 16.4 Existem várias instalações

### Windows CMD

```cmd
where git
```

### PowerShell

```powershell
Get-Command git -All
```

### macOS/Linux

```bash
type -a git
```

Isso permite identificar se mais de uma instalação está disponível.

---

## 16.5 Verificar a configuração

```bash
git config --list --show-origin
```

---

## 16.6 Verificar identidade

```bash
git config user.name
git config user.email
```

Global:

```bash
git config --global user.name
git config --global user.email
```

---

## 16.7 `git push` solicita autenticação

Primeiro verifique o remoto:

```bash
git remote -v
```

Se estiver usando SSH:

```bash
ssh -T git@github.com
```

Se estiver usando HTTPS, verifique o gerenciador de credenciais e as credenciais utilizadas.

---

## 16.8 Editor não abre

Verifique:

```bash
git config --global core.editor
```

Exemplo com VS Code:

```bash
git config --global core.editor "code --wait"
```

---

# 17. Compatibilidade e sistemas antigos

O Git funciona em diferentes sistemas operacionais, mas isso não significa que a versão atual será compatível com todas as versões históricas.

A relação correta é:

```text
Sistema operacional
        +
Versão do sistema
        +
Arquitetura
        ↓
Versão compatível do Git
```

---

## 17.1 Windows

Consulte:

https://gitforwindows.org/requirements.html

---

## 17.2 macOS

Consulte:

https://git-scm.com/install/mac

Dependendo da versão do macOS, pode ser necessário utilizar:

```text
Command Line Tools
Homebrew
MacPorts
versão específica
compilação manual
```

---

## 17.3 Linux

A versão disponível pode depender de:

```text
Distribuição
Versão da distribuição
Repositórios habilitados
Gerenciador de pacotes
```

---

## 17.4 Compilação manual

O Git também pode ser compilado a partir do código-fonte.

Documentação oficial:

https://git-scm.com/install/source

A compilação manual normalmente é utilizada quando:

```text
A versão necessária não está disponível
        OU
O sistema não possui pacote adequado
        OU
Existe uma necessidade específica de compilação
```

---

# 18. Checklist final

Utilize este checklist depois de configurar uma nova máquina.

## 18.1 Git instalado

```bash
git --version
```

---

## 18.2 Git encontrado pelo sistema

### Windows CMD

```cmd
where git
```

### PowerShell

```powershell
Get-Command git
```

### macOS/Linux/Git Bash

```bash
which git
```

---

## 18.3 Nome configurado

```bash
git config --global user.name
```

---

## 18.4 E-mail configurado

```bash
git config --global user.email
```

---

## 18.5 Branch inicial configurado

```bash
git config --global init.defaultBranch
```

Resultado esperado:

```text
main
```

---

## 18.6 Configurações verificáveis

```bash
git config --list --show-origin
```

---

## 18.7 Repositório criado

```bash
mkdir teste-git
cd teste-git
git init
```

---

## 18.8 Status funcionando

```bash
git status
```

---

## 18.9 Primeiro arquivo criado

```text
README.md
```

---

## 18.10 Primeiro arquivo adicionado

```bash
git add README.md
```

---

## 18.11 Primeiro commit realizado

```bash
git commit -m "docs: add README"
```

---

## 18.12 Histórico funcionando

```bash
git log --oneline
```

---

## 18.13 Autenticação com GitHub testada

SSH:

```bash
ssh -T git@github.com
```

---

# 19. Referências oficiais

## Git

* Site oficial: https://git-scm.com/
* Instalação no Windows: https://git-scm.com/install/windows
* Instalação no macOS: https://git-scm.com/install/mac
* Instalação no Linux: https://git-scm.com/install/linux
* Instalação a partir do código-fonte: https://git-scm.com/install/source
* Documentação de configuração: https://git-scm.com/docs/git-config
* Documentação do `git init`: https://git-scm.com/docs/git-init
* Documentação do `git clone`: https://git-scm.com/docs/git-clone
* Documentação do `git status`: https://git-scm.com/docs/git-status
* Documentação do `git add`: https://git-scm.com/docs/git-add
* Documentação do `git commit`: https://git-scm.com/docs/git-commit
* Documentação do `git branch`: https://git-scm.com/docs/git-branch
* Documentação do `git switch`: https://git-scm.com/docs/git-switch
* Documentação do `git merge`: https://git-scm.com/docs/git-merge
* Documentação do `git pull`: https://git-scm.com/docs/git-pull
* Documentação do `git push`: https://git-scm.com/docs/git-push

## Git for Windows

* Site: https://gitforwindows.org/
* Requisitos: https://gitforwindows.org/requirements.html

## GitHub

* Documentação: https://docs.github.com/
* SSH no GitHub: https://docs.github.com/en/authentication/connecting-to-github-with-ssh

## Homebrew

* Site: https://brew.sh/
* Fórmula do Git: https://formulae.brew.sh/formula/git

---

# Conclusão

Depois da instalação, uma máquina preparada para trabalhar com Git deve chegar a este estado:

```text
Sistema operacional
        ↓
Git instalado
        ↓
Git disponível no PATH
        ↓
Nome configurado
        ↓
E-mail configurado
        ↓
Branch padrão configurado
        ↓
Editor configurado
        ↓
Autenticação configurada
        ↓
Repositório criado
        ↓
Primeiro commit realizado
        ↓
GitHub conectado
```

A partir desse ponto, a próxima etapa é aprofundar o uso do Git:

```text
Branches
    ↓
Merge
    ↓
Rebase
    ↓
Conflitos
    ↓
Stash
    ↓
Tags
    ↓
Reset
    ↓
Revert
    ↓
Cherry-pick
    ↓
Remotes
    ↓
Pull Requests
    ↓
GitHub Actions
    ↓
Estratégias profissionais de versionamento
```

Essa base é suficiente para preparar uma máquina nova e começar a utilizar Git de forma funcional em Windows, macOS ou Linux.

```
```
