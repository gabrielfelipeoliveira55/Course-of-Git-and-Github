# Fundamentos do Git e do GitHub

> Este documento reúne os primeiros conceitos do curso: o que é o Git, por que ele existe, quem pode utilizá-lo e onde os projetos versionados podem ser hospedados através do GitHub.

## Menu de Navegação

- [O que é Git?](#o-que-é-git)
- [Quem pode usar?](#quem-pode-usar)
- [Qual é o objetivo do Git?](#qual-é-o-objetivo-do-git)
  - [Objetivos e Funções Principais](#objetivos-e-funções-principais)
- [Por que preciso usar Git?](#por-que-preciso-usar-git)
- [Onde hospedo meus projetos versionados?](#onde-hospedo-meus-projetos-versionados)
  - [O que é o GitHub?](#o-que-é-o-github)
  - [Para que serve?](#para-que-serve)
  - [Principais Recursos](#principais-recursos)

---

## O que é Git?

> **Git** é um software de versionamento: ele registra e organiza as modificações feitas em um conjunto de arquivos dentro de um **repositório Git local** — uma pasta no seu próprio computador que armazena todos os arquivos do projeto, junto com o histórico completo de alterações e versões.

## Quem pode usar?

> O Git é usado, principalmente, para coordenar o trabalho entre programadores que desenvolvem código-fonte de forma colaborativa. Mas ele não se limita a isso: por funcionar com praticamente qualquer tipo de arquivo, também pode ser utilizado por outros profissionais — o objetivo central continua o mesmo: guardar as modificações de um conjunto de arquivos.

## Qual é o objetivo do Git?

> O principal objetivo do Git é controlar e armazenar o histórico — chamado de **snapshot** ("fotografia" do estado dos arquivos em um determinado momento) — das alterações feitas em um código-fonte ou conjunto de arquivos, de forma distribuída. Isso permite navegar entre os diferentes marcos e ramificações do projeto, facilitando o trabalho em equipe.

### Objetivos e Funções Principais

- **Controle de versão:** rastreia cada mudança feita nos arquivos, permitindo saber quem alterou, o que foi alterado e quando.
- **Trabalho simultâneo:** permite que vários desenvolvedores editem o mesmo projeto ao mesmo tempo, sem que um sobrescreva o trabalho do outro.
- **Segurança e histórico:** mantém um histórico completo do projeto, facilitando a recuperação de versões anteriores caso ocorram erros.
- **Desenvolvimento não linear:** usa ramificações (**branches**) para testar novas ideias ou corrigir falhas de forma isolada, antes de uni-las ao projeto principal.
- **Distribuição:** garante que cada colaborador tenha uma cópia completa do repositório e do seu histórico no próprio computador, permitindo trabalhar também offline.

> **Resumindo:** o Git dá controle total sobre cada modificação, sem que o trabalho de um integrante da equipe sobrescreva o de outro — tudo isso preservando a integridade dos dados e mantendo alta velocidade de operação.

## Por que preciso usar Git?

### Exemplos

- **Apagou algo importante sem querer?** Basta voltar para uma versão anterior do arquivo e recuperar o que foi perdido.
- **Dois colegas mexendo no mesmo projeto ao mesmo tempo?** Cada um trabalha na sua parte sem que as alterações de um sobrescrevam as do outro.
- **Quer testar uma ideia arriscada?** Você isola essa mudança em uma ramificação separada e só une ao projeto principal se der certo.
- **Precisa saber quem alterou o quê e quando?** O histórico completo do projeto mostra exatamente isso.
- **Ficou sem internet no meio do trabalho?** Como cada colaborador tem uma cópia completa do repositório, dá para continuar trabalhando offline normalmente.

### Comparando na prática: sem Git vs. com Git

> **O cenário:** uma microempresa está desenvolvendo um novo projeto — a pasta de um formulário de cadastro. O chefe pede que 4 profissionais diferentes criem, cada um, seu próprio modelo do formulário, para depois comparar e decidir qual usar.

| Situação | Sem Git | Com Git |
|---|---|---|
| Cada profissional cria sua versão | Arquivos soltos, tipo `formulario_v1.html`, `formulario_maria_final.html`, `formulario_FINAL_USAR_ESSE.html` | Cada um trabalha em sua própria ramificação (branch), isolada das demais, dentro do mesmo repositório |
| Comparar as 4 versões | O chefe precisa abrir os 4 arquivos manualmente e comparar visualmente, um por um | O chefe visualiza as 4 ramificações lado a lado, cada uma com seu histórico completo de alterações |
| Alguém não gosta do resultado e quer voltar à versão anterior | Precisa lembrar de cabeça como estava antes e **reescrever tudo do zero, à mão** — sem garantia de acertar exatamente igual | Basta **um único comando**: a versão anterior volta exatamente como estava, sem reescrever nada |
| Trabalho sem internet | Depende do arquivo estar salvo localmente e ser sincronizado manualmente depois | Cada colaborador tem uma cópia completa do repositório e do histórico, funcionando offline normalmente |
| Escolher a versão final | Risco real de sobrescrever ou perder alguma versão sem querer | O chefe escolhe a melhor ramificação, ou une as melhores partes de cada uma ao projeto principal, sem perder nenhuma versão pelo caminho |

> **Sem Git:** imagine a frustração de um dos profissionais que já reescreveu o formulário do zero, tentando lembrar cada detalhe de como ele era antes — só para perceber, depois de todo esse esforço, que a versão anterior já estava boa.
>
> **Com Git:** essa mesma situação não vira drama nenhum. É só um comando, e a versão anterior volta exatamente como estava — nenhum retrabalho, nenhuma reconstrução manual.

## Onde hospedo meus projetos versionados?

### O que é o GitHub?

> O **GitHub** é uma plataforma online de hospedagem de código-fonte e controle de versão, baseada na nuvem, que utiliza o sistema Git.

### Para que serve?

- **Armazenamento:** guarda arquivos e códigos de projetos de forma segura na nuvem.
- **Colaboração:** permite que vários desenvolvedores trabalhem no mesmo projeto ao mesmo tempo, sem sobrescrever o trabalho uns dos outros.
- **Histórico:** registra todas as alterações feitas no código, facilitando a reversão para versões anteriores, se necessário.

### Principais Recursos

- **Repositórios:** onde os arquivos do projeto ficam armazenados.
- **Pull Requests:** ferramentas para propor e revisar alterações antes de adicioná-las ao projeto oficial.
- **Issues:** espaço para relatar erros, sugerir melhorias e organizar tarefas.

---

## Revisão Rápida

| Conceito | Resumo |
|---|---|
| **Git** | Software de controle de versão que registra o histórico de um repositório local. |
| **GitHub** | Plataforma na nuvem que hospeda repositórios Git e adiciona recursos de colaboração (Pull Requests, Issues). |
| **Snapshot** | "Fotografia" do estado dos arquivos em um momento específico do histórico. |
| **Branch** | Ramificação usada para desenvolver algo isolado do código principal. |

---

<p align="center"><a href="https://github.com/gabrielfelipeoliveira55" target="_blank">Gabriel Felipe de Oliveira Rateiro</a></p>