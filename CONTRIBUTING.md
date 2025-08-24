# Guia de Contribuição

*Bem-vindo ao Guia de Contribuição.*

Este documento centraliza as convenções técnicas e os padrões de estilo utilizados neste repositório. Seguir as diretrizes detalhadas abaixo é fundamental para manter a consistência, a organização e a qualidade do projeto, servindo como um manual de boas práticas para mim e para qualquer futuro colaborador.

## Como Contribuir

A principal forma de contribuição é através de [Issues do GitHub](https://github.com/WilliamdeSousa/WilliamdeSousa/issues). Todas as sugestões são bem-vindas:

* **🐛 Reportando Erros:** Se você encontrar um erro de digitação, uma informação incorreta ou um link quebrado, por favor, abra uma Issue descrevendo o problema.
* **💡 Sugerindo Melhorias:** Tem uma ideia para organizar melhor o conteúdo ou um link para um material de apoio que não está aqui? Use as Issues para fazer sugestões.

## Código de Conduta

Espera-se que todas as interações neste projeto (issues, comentários, etc.) sigam um código de conduta amigável e respeitoso. O foco é o aprendizado e a colaboração.

## Guias de Estilo

Para manter a organização, seguimos algumas convenções importantes.

### 📂 Estrutura de Diretórios

A organização das pastas neste repositório segue uma hierarquia lógica e previsível para facilitar a navegação e a manutenção. A estrutura geral é ilustrada abaixo:

```text
.
├── Instituicao/ (ex: IFPB, UFCG)
│   └── curso-ou-projeto/
│       ├── ano.periodo/ (opcional)
│       │   └── disciplina/ (opcional)
│       │       └── ...
│       └── ...
└── Escopo-Geral/ (ex: Scripts)
    └── ...
````

#### Regras de Nomenclatura e Estrutura

* **Diretórios na Raiz:** Os diretórios no nível principal do repositório podem ter nomes com formatação flexível (`Uppercase`, `lowercase`, `PascalCase`), como `IFPB` ou `Scripts`, conforme for mais adequado ao contexto.

* **Subdiretórios e Pastas Internas:** Todos os diretórios abaixo do nível raiz (como nomes de cursos, projetos, disciplinas e suas subpastas) **devem** obrigatoriamente seguir o formato `lowercase-com-hifens` (kebab-case) e de preferência sem acentuações.

* **Estrutura de Cursos vs. Projetos:** Para materiais de **cursos** dentro de uma instituição, a estrutura `ano.periodo/disciplina` é fortemente recomendada. Para **projetos**, esses níveis são opcionais e podem ser omitidos.

### 📄 Nomenclatura de Arquivos

A nomenclatura de arquivos visa a clareza e uma boa experiência de navegação no repositório.

1. **`README.md` (Arquivo de Apresentação/Índice):**
    Este arquivo deve ser usado como a "página inicial" de um diretório. Sua função é **apresentar, organizar e fornecer links** para os arquivos de conteúdo relevantes daquela pasta. O `README.md` de uma disciplina, por exemplo, apresenta a ementa e links para as avaliações. O `README.md` de uma avaliação exibe as imagens das questões e das respostas.

2. **Arquivos de Conteúdo Bruto:**
    Estes são os arquivos que guardam a informação final. Eles devem ter nomes descritivos e, sempre que possível, serem organizados em subpastas (como `rsc/` para recursos ou `assets/`).

      * **Exemplos:** `prova1.jpg`, `respostas.jpg`, `relatorio_final.pdf`, `codigo_lab1.py`.

### 💬 Convenção de Commits

Este projeto utiliza o padrão [Conventional Commits](https://www.conventionalcommits.org/pt-br/v1.0.0/) para criar um histórico de commits explícito e legível.

#### Estrutura da Mensagem

```text
<tipo>[escopo opcional]: <descrição>

[corpo opcional]

[rodapé(s) opcional(is)]
````

#### Tipos de Commit

* **feat**: Para adicionar um novo conteúdo principal (uma nova avaliação, um novo resumo, um novo script, etc.).
* **fix**: Para corrigir um erro em um arquivo existente (um erro de digitação, uma informação errada).
* **docs**: Para adicionar ou modificar arquivos de documentação (como `README.md` ou este próprio guia).
* **refactor**: Para reestruturar arquivos sem alterar o conteúdo (mover ou renomear arquivos/pastas).
* **style**: Para mudanças que não afetam o significado do conteúdo (formatação, espaços em branco).
* **chore**: Para tarefas de manutenção que não afetam o conteúdo principal (atualizar scripts, configurar ferramentas).

#### Escopo

O escopo indica a parte do projeto que foi modificada, seguindo a estrutura `instituição/curso/período/disciplina` sempre em minúsculo.

**Códigos dos Cursos/Projetos:**
Para manter o escopo conciso, utilize os seguintes códigos:

* `ec`: Engenharia de Computação
* `pg`: Petróleo e Gás
* `tele`: Telemática
* `pop`: Projeto Olímpico de Programação

**Abreviações das Disciplinas:**

* `micro`: Microprocessadores e Microcontroladores
* `teoria-comp`: Teoria da Computação
* `lsa`: Laboratório de Sistemas Abertas
* `psd`: Projeto de Sistemas Digitais

**Exemplos de Escopo:**

* `(ifpb/ec/2025.1/micro)`
* `(ifpb/pop/2023)`
* `(ufcg/pibic)`
* `(scripts)`

#### Descrição

* Use o **modo imperativo** no presente (ex: "adiciona", "corrige", "move" em vez de "adicionado", "corrigido" ou "movido").
* Comece com letra minúscula.
* Não termine com um ponto final.

#### Corpo do Commit (Opcional)

O corpo da mensagem é utilizado quando a descrição não é suficiente para explicar o contexto completo da mudança. Ele deve detalhar o **"o quê"** e o **"porquê"** da alteração.

#### Rodapé(s) do Commit (Opcional)

O rodapé serve para adicionar metadados sobre o commit, como referências a *Issues* ou a declaração de mudanças drásticas (*Breaking Changes*).

* **Referenciando Issues:** Para vincular o commit a uma Issue, utilizam-se palavras-chave como `Closes`, `Fixes`, `Resolves` seguidas do número da Issue (ex: `Closes #17`).
* **Mudanças Drásticas (Breaking Changes):** Para indicar uma mudança que quebra a compatibilidade, o rodapé **deve** iniciar com `BREAKING CHANGE:` (com os dois pontos e um espaço), seguido de uma explicação clara da mudança e seu impacto.
