# Nuno Leitao

[photo]: http://avatars0.githubusercontent.com/u/10015316?v=3&s=460

* About
* Technical skills
* Endorsements

--

### [Hack'Aveiro](https://hackaveiro.org)

Pela prática, divulgação, promoção, desenvolvimento,
investigação e estudo das tecnologias,
técnicas, ciências e artes por

** hackers, makers e artistas. **

--

### Luís Faceira

* Director da [be.ubi](http://www.beubi.com)
* Software / Continuous Delivery / DevOps
* https://github.com/luisfaceira
* [luisfaceira@gmail.com](mailto:luisfaceira@gmail.com)

--

### Temas a abordar:

1. Controlo de revisões?
2. Histórico linear
3. Trabalhar em equipa
4. Trabalhar em comunidade
5. Que mais?

--

### Pré-requisitos:

* Conta em github.com
* Git/GitHub instalado no computador

--

# Tomem notas de erros/melhorias aos slides!

----

## 1. Controlo de revisões?

--

### Git ou GitHub?

`git` - é o sistema distribuído de controlo de revisões mais utilizado

`github` - é a empresa/plataforma de alojamento de repositorios git mais utilizada

--

> Revision control, also known as version control or source control, is the management of _**changes**_ to documents, computer programs, large web sites, and other collections of information

--

Um sistema de controlo de revisões permite gerir a _**evolução**_ de um conjunto de documentos/ficheiros

--

Ajuda a resolver, entre outras, as seguintes necessidades:

* Armazenamento seguro dos items de trabalho
* Coordenação de equipa
* Gestão de trabalho em paralelo
* Acesso a múltiplas versões
* Análise de causa raíz
* Reversão de erros cometidos
* Análise de diferenças

--

### Sistemas centralizados (e.g. svn)

* Repositório central único
* Apenas trabalho actual existe localmente
* Requer uma ligação de rede
* Exige mais largura de banda
* Operações são lentas
* Workflows simplificados

--

### Sistemas distribuídos (e.g. **git**)

* Usa pelo menos dois repositórios
* Todas as versões existem localmente
* Funciona offline
* Exige mais espaço
* Operações são rápidas
* Múltiplos workflows possíveis

----

## 2. Histórico linear

--

### TODO: Iniciar um repositório online:

1. Aceder a https://github.com/new
2. Preencher com nome "hello-world"
3. Descrição surge nas listagens no site do projeto
4. Escolher opção para inicializar com README
5. Navegar pelo repositório

> git init

--

Ficheiros comuns:

* `README.md` - Descrição do projeto, como o usar/instalar, etc.
* `LICENSE` - declara em que condições outros podem usar o conteúdo do projeto
* `CONTRIBUTING.md` - explica a terceiros como podem contribuir para o projeto
* `.gitignore` e `.gitattributes`- opções avançadas de git

--

### TODO: Fazer 'clone' na aplicação:

1. Clicar em '+'
2. Clone
3. hello-world
4. Clone hello-world
5. Escolher pasta

> git clone git@github.com:HackAveiro/hello-world.git

--

### TODO: Editar ficheiro

Abrir o ficheiro nu editor de texto e colocar:

```markdown
# hello-world

Este é um pequeno projeto de aprendizagem
das opções básicas de utilização do git.

Sequência de operações que
serão experimentadas:

* add - selecção de alterações a registar
* commit - registar um conjunto de alterações
* push - remeter as alterações para um servidor central

```

--

### TODO: Primeiro commit

| Linha de comandos   | Aplicação                           |
| ------------------- | ----------------------------------- |
| `git add README.md` | Seleccionar ficheiros               |
| `git commit`        | Escrever mensage e clicar em Clone  |
| `git push`          | Clicar em "Sync"                    |

--

* Primeira linha é obrigatória, deve ser inferior a 50 carateres
* Após linha de intervalo pode-se descrever em maior detalhe
* Repetir 3 vezes com outras edições
* Analisar resultado online

--

### Fluxo

clone/pull -> add -> commit -> push

----

## 3. Trabalhar em equipa

--

### O Git é um DAG (Directed Acyclic Graph) de commits

Cada commit contém:

* Os commits que lhe dão origem
* Um autor, um commiter, uma mensagem
* Um conjunto de alterações
* Um conjunto de dados resultantes
* Um identificador único (SHA):

f643986c985998abd74076afe0247c81e0399512

--

### Referências

As referências são apontadores para determinados commits.

* tags - apontam para commits fixos, normalmente usadas para marcar uma versão estável (e.g. v3.4) 
* branches - apontam para o extremo de uma ramificação, normalmente usadas para marcar uma iniciativa de evolução em curso

--

### TODO: Criar e seleccionar uma branch

| Linha de comandos      | Aplicação                                                                     |
| ---------------------- | ----------------------------------------------------------------------------- |
| `git branch english`   | Clicar no ícone no topo junto a 'master' e dar o nome à branch como `english` |
| `git checkout english` | Branch seleccionada por omissão                                               |

--

* Normalmente a branch principal chama-se 'master' ou 'develop'
* Em CLI a branch é criada a partir da branch em que estamos
* Em CLI podemos usar o atalho `git checkout -b english`

--

### TODO: Fazer um commit na branch 'english'

Editar a **primeira** frase para inglês e fazer commit e push para o servidor.

--

### TODO: Fazer um commit na branch principal

* Mudar de volta para a branch principal
* Adicionar conteúdo no FINAL do ficheiro descrevendo os novos passos aprendidos
* Fazer commit e publicar online
* Navegar online

--

### TODO: Fazer merge de master -> english

| Linha de comandos      | Aplicação                                                       |
| ---------------------- | --------------------------------------------------------------- |
| `git checkout english` | Escolher 'english' na lista de selecção no topo                 |
| `git diff master`      | Clicar em 'Compare', escolher 'master' e analisar grafo no topo |
| `git merge master`     | Clicar em 'Update from master'                                  |
| `git push`             | Clicar em `Publish` ou `Sync`                                   |

--

### Fluxo

branch A -> checkout A -> commit -> checkout B -> merge A

----

## 4. Trabalhar em comunidade

--

### A revolução do open-source

* `Fork` - Permite criar, numa **plataforma de alojamento**, uma cópia integral de um projeto e evoluir o mesmo livremente
* `Pull Request`- Pedido de autorização, discussão e melhoria colaborativa da integração de uma ramificação de um projeto

Estas funções foram popularizadas pelo GitHub mas já se encontram disponíveis em qualquer plataforma de alojamento de git.

--

### TODO: Fork dos slides do workshop

* https://github.com/HackAveiro/hackaveiro.github.io
* Clicar em 'Fork'

--

### TODO: Melhorar os slides

* Fazer git clone do VOSSO fork
* Fazer 1 ou mais commits
* Sincronizar para o servidor

--

### TODO: Abrir pull-request

* Navegar para a própria branch, online
* Clicar em 'Create Pull Request'
* Escolher como destino o 'master' da conta 'HackAveiro'
* Submeter

--

### DEMO: Aceitação do pull-request

----

## 5. Que mais?

--

### Outras funções do github

* Issues, Wiki, Permissions
* Alojamento de páginas - https://pages.github.com
* Pequenos scripts - https://gist.github.com

--

### Outros comandos github

| Comando                  | Descrição                                                                |
| ------------------------ | ------------------------------------------------------------------------ |
| `git status`             | Apresenta em que branch/commit estamos, ficheiros alterados, etc.        |
| `git commit -a`          | Adiciona todos os ficheiros antes de fazer commit                        |
| `git checkout -- <file>` | Descarta alterações não commited de um certo ficheiro ou pasta           |
| `git log`                | Apresenta o histórico de evolução que levou até ao ponto actual          |
| `git reset --HARD <ref>  | Resolve muitos problemas, ignora tudo e coloca-nos numa certa referência |

--

# Dúvidas?

[luisfaceira@gmail.com](mailto:luisfaceira@gmail.com)

[hackaveiro.org](https://hackaveiro.org)

--

Beijinhos
