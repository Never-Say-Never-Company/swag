# <p align = "center"> SWAG - API 5º Semestre - BD 2025

Um projeto que analisa métricas de um time de desenvolvimento coleta dados sobre produtividade, qualidade e eficiência do processo. Essas informações são organizadas e processadas para gerar insights claros sobre desempenho e evolução da equipe. Por fim, os resultados são apresentados em um dashboard interativo que apoia a tomada de decisão e a melhoria contínua.

<br>
<p align="center">
  <a href="#integrantes-da-equipe">Integrantes do Time</a> |
  <a href="#descrição-do-desafio">Descrição do Desafio</a> |
  <a href="#objetivo">Objetivo do Projeto</a> |
  <a href="#requisitos">Detalhamento de Requisitos</a> |
  <a href="#cronograma">Cronograma</a> |
  <a href="#tecnologias-utilizadas">Tecnologias Utilizadas</a>
</p>

<br>

## <a id="integrantes-da-equipe"> Integrantes do Time: </a>

| **Nome**            | **Função**        | **LinkedIn**                                                                                                                                           |
|:-------------------:|:-----------------:|:------------------------------------------------------------------------------------------------------------------------------------------------------:|
| Isaque de Souza     | Scrum Master      | [![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-blue?style=flat-square&logo=linkedin&labelColor=blue)](https://www.linkedin.com/in/isaque-souza-6760b8270/) |
| Paloma Soares       | Desenvolvedor     | [![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-blue?style=flat-square&logo=linkedin&labelColor=blue)](https://www.linkedin.com/in/paloma-soares-rocha/) |
| Ricardo Campos      | Product Owner     | [![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-blue?style=flat-square&logo=linkedin&labelColor=blue)](https://www.linkedin.com/in/ricardo-campos-ba56091b5/) |
| Vinícius Monteiro   | Desenvolvedor     | [![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-blue?style=flat-square&logo=linkedin&labelColor=blue)](https://www.linkedin.com/in/viniciusvasm/) |


<br>

## <a id="objetivo"> Objetivo do Projeto </a>

O objetivo deste produto é fornecer uma plataforma de gestão e análise de desempenho de projetos que atenda tanto gestores quanto desenvolvedores. Para os gestores, o sistema oferece visão detalhada do desempenho individual e coletivo do time, permitindo gerar dashboards interativos, boards consolidados e acompanhar indicadores-chave de progresso. Para os desenvolvedores, a plataforma possibilita monitorar seu próprio desempenho, atividades concluídas e métricas pessoais, promovendo maior autoconhecimento e engajamento. O sistema garante ainda controle de acesso por perfis, assegurando que cada usuário visualize informações adequadas ao seu nível de permissão.

<p align="center">
    <a href="documentacao/fluxodeatualizacao.svg">
        <img src="https://img.shields.io/badge/Fluxo_de_Comunicação_do_Sistema-blue?style=for-the-badge&logo=Diagrams" alt="Fluxo de Comunicação do Sistema">
    </a>
    <a href="documentacao/funcionamentoatualizacao.svg">
        <img src="https://img.shields.io/badge/Evolução_do_Fluxo_de_Atualização-green?style=for-the-badge&logo=Diagrams" alt="Evolução do Fluxo de atualização da base por sprint">
    </a>
</p>

<br>

---
## <a id="requisitos"> Detalhamento de Requisitos </a>

### Requisitos Funcionais (RF)

| ID do Requisito | Descrição | Origem (Pessoa/Documento) |
| :---: | :--- | :--- |
| **RF1** | O sistema deve **consumir dados da API do Jira** (Host: `https://necto.atlassian.net/`, Username: `api5bdfatec@gmail.com`). | Requisitos de Cliente [p. 1] |
| **RF2** | O sistema deve **consolidar os dados em um Data Warehouse** (DW). | Requisitos de Cliente [p. 1] |
| **RF3** | O sistema deve gerar **indicadores, dashboards e boards** sobre o andamento dos projetos. | Requisitos de Cliente [p. 1] |
| **RF4** | O sistema deve permitir a **criação de visualizações (desenhos de tela)** utilizando **Figma ou Miro** (sugerido pela Vanessa). | Vanessa Matsumura [16:47] |
| **RF5** | O sistema deve permitir o uso de **fluxos em BPMN** para validar fluxos de trabalho. | Vanessa Matsumura [16:46] |
| **RF6** | O sistema deve **restringir a visualização de informações de custo** apenas ao **Gerente de Projetos**. | Vanessa Matsumura [16:46, 19:02] |
| **RF7** | O sistema deve exibir a **Quantidade de Horas Utilizadas** por: cada atividade, módulo (Epic/Produto/Entregável), e pelo desenvolvedor (por atividade/módulo/dia). | Vanessa Matsumura [15:41] |
| **RF8** | O sistema deve exibir a **Quantidade de Bugs (Total)**. | Vanessa Matsumura [15:41] |
| **RF9** | O sistema deve exibir a **Quantidade de Issues Abertas** por status: **aguardando, em andamento, em MR e concluídas**. | Vanessa Matsumura [15:41] |
| **RF10**| O sistema deve **mensurar o tempo de trabalho** de cada desenvolvedor por **módulo/projeto**. | Vanessa Matsumura [7:22] |
| **RF11**| O sistema deve **mensurar a quantidade de atividades finalizadas** de cada desenvolvedor dentro do período definido ou por projeto. | Vanessa Matsumura [7:22] |

### Requisitos Não Funcionais (RNF)

| ID do Requisito | Descrição | Origem (Pessoa/Documento) |
| :---: | :--- | :--- |
| **RNF1** | O modelo de dados dimensional (Star/Snowflake) deve ser **documentado e validado** antes da implementação de cada Sprint. A documentação deve incluir: conceitual, lógico, físico e dicionário de dados. | Requisitos de Cliente [p. 2], Ata da Reunião |
| **RNF2** | Deve ser entregue um **Manual de Instalação** (obrigatório, no Git). | Requisitos de Cliente [p. 2] |
| **RNF3** | Deve ser entregue um **Manual do Usuário** (obrigatório). | Requisitos de Cliente [p. 2] |
| **RNF4** | O acesso deve contemplar **diferentes perfis de usuário**: Gerente de Projetos, Líder de Equipe e Membro da Equipe (Desenvolvedor). | Requisitos de Cliente [p. 1], Vanessa Matsumura [16:46] |
| **RNF5** | O sistema deve garantir que o **nível de permissão seja distinto**. | Requisitos de Cliente [p. 1] |
| **RNF7** | O sistema deve ser **escalável**, suportando de **10** (usuários atuais) a **1000** (estimativa futura) usuários. | Vanessa Matsumura [14:06] |
| **RNF8** | **Sugestão de Linguagem/Framework**: Python e Django. | Requisitos de Cliente [p. 2] |
| **RNF9** | **Sugestão de Ferramentas**: Docker e AWS. | Requisitos de Cliente [p. 2] |
| **RNF10**| Devem ser aplicados **conceitos e ferramentas de DevOps** em todo o projeto, com justificativas técnicas. | Requisitos de Cliente [p. 1], Ata da Reunião |
| **RNF11**| Requisitos de **Qualidade de Código**: Análise Estática de Código e Testes Automatizados (Unidade, Integração e Funcionais de Sistema API/UI). | Requisitos de Cliente [p. 2] |

---

<br>

## <a id="cronograma"> Cronograma</a>

| Sprint | Nome                        | Data Início | Data Fim | Status |
|--------|-----------------------------|------------|----------|--------|
| --     | Kick-off geral              | 25/08      | 29/08    | Ok     |
| 1      | Sprint 1                   | 08/09      | 28/09    |        |
| 2      | Sprint Review / Planning    | 29/09      | 03/10    |        |
| 3      | Sprint 2                   | 06/10      | 26/10    |        |
| 4      | Sprint Review / Planning    | 27/10      | 31/10    |        |
| 5      | Sprint 3                   | 03/11      | 23/11    |        |
| 6      | Sprint Review              | 24/11      | 28/11    |        |
| 7      | Feira de Soluções           | 04/12      | 04/12    |        |

<br>

## <a id="tecnologias-utilizadas"> Planejamento de Sprints</a>

| Sprint | Meta da Sprint | Foco | User Stories e Requisitos Principais |
| :---: | :--- | :--- | :--- |
| **Sprint 1** | **Entendimento, Prova de Conceito (Mockados) e Modelagem de Dados Inicial** | Estudo da API, validação do DW (**Snowflake**), Prova de Conceito de gráficos com **dados mockados** e apresentação do fluxo futuro. | **Modelagem Conceitual/Lógica/Física do DW** (RNF1), **Conexão com a API e POC com Dados Mockados** (RF1), Definição e Justificativa de **DevOps** (RNF10), Criação de **Desenhos de Tela** (RF4). |
| **Sprint 2** | **Construção do Data Warehouse e Dashboards Essenciais** | Implementação do ETL (extração e carga) e dos indicadores de maior prioridade. | **US001, US002, US003, US004, US005** (Indicadores de Alto Impacto). **Implementação do ETL** e do DW (RF2). **Controle de Acesso de Custo** (RF6). |
| **Sprint 3** | **Refinamento, Métricas Individuais e Qualidade/Documentação** | Implementação das métricas mais detalhadas, escalabilidade (RNF7), testes e documentação final (RNF2, RNF3). | **US006, US007, US008, US009** (Métricas de Desempenho Individual e Funcionalidade de Perfis). **Testes e Qualidade** (RNF11), **Documentação Final** (RNF2, RNF3). |


# 🌳 Estratégia de Branching e Commit
<details>
<summary>Clique para expandir a documentação completa da Estratégia</summary>
Esta documentação descreve a estrutura dos nossos repositórios, o fluxo de trabalho de desenvolvimento, a estratégia de *branching* (ramificação) e os padrões de *commit* (registro de alterações) adotados pela equipe.

## 1\. Estrutura dos Repositórios

Nosso projeto está organizado em três repositórios distintos, seguindo a separação de responsabilidades:

| Repositório | Descrição |
| :--- | :--- |
| `swagback` | Desenvolvimento do *backend*. |
| `swagfront` | Desenvolvimento do *frontend*. |
| `swag` | Repositório dedicado à documentação do projeto. |

**Importante:** A estratégia de *branching* e o padrão de *commits* detalhados abaixo se aplicam **igualmente aos três repositórios**.

## 2\. Fluxo de Branching (Estratégia por Sprint)

Adotamos um fluxo baseado em *sprints*, onde a *branch* principal (`main`) reflete sempre o estado de produção estável e uma *branch* intermediária gerencia o desenvolvimento da sprint atual.

### 2.1. Branches Principais

  * **`main`**: A *branch* principal. **Sempre deve conter código estável e pronto para produção.** O *merge* direto na `main` é proibido; todas as alterações chegam via *merge* da *branch* da Sprint.

### 2.2. Branches de Sprint

  * **Nomeclatura:** `Sprint<número da sprint atual>` (Ex: `Sprint1`, `Sprint2`, `Sprint10`).
  * **Criação:** No início de cada ciclo de desenvolvimento (Sprint), uma nova *branch* é criada a partir da **`main`**.
  * **Propósito:** Esta *branch* serve como o **ambiente de integração** para todas as *tasks* da sprint. Todas as *branches* de *features* ou *fixes* são mergeadas nela.
  * **Fechamento da Sprint:** Ao final da Sprint, após a conclusão e validação do código, a *branch* da sprint é **mergeada na `main`**. A *branch* da sprint anterior é descontinuada (ou mantida como histórico, a critério da equipe).

### 2.3. Branches de Task (Desenvolvimento)

  * **Criação:** Para o desenvolvimento de qualquer *task* (nova *feature*, correção de *bug*, refatoração, etc.), o desenvolvedor deve criar uma nova *branch* **a partir da *branch* da sprint atual** (`Sprint<número>`).
  * **Propósito:** Isolar o desenvolvimento de uma única *task* ou correção.
  * **Merge:** Após a conclusão e o **Code Review**, esta *branch* é mergeada de volta na **`Sprint<número da sprint atual>`**.

## 3\. Padrão de Commit (Convenção Semântica)

Para manter um histórico de commits limpo e significativo, é **obrigatório** seguir o padrão de commit semântico abaixo:

### 3.1. Formato

```
<tipo da task>(#<número do card da task>): <descrição breve do que foi feito>
```

**Exemplo:**

```
feat(#34): desenvolvido método para coleta de dados
```

ou

```
fix(#15): corrigida quebra de layout na página inicial
```

### 3.2. Tipos de Task (Principais)

| Tipo | Descrição |
| :--- | :--- |
| `feat` | Uma nova *feature* ou funcionalidade. |
| `fix` | Uma correção de *bug*. |
| `docs` | Alterações apenas na documentação. |
| `style` | Mudanças que não afetam o significado do código (espaços, formatação, ponto e vírgula, etc.). |
| `refactor` | Uma mudança de código que não corrige um bug nem adiciona uma feature. |
| `test` | Adicionando testes ausentes ou corrigindo testes existentes. |
| `chore` | Mudanças na build, dependências ou outras ferramentas e bibliotecas externas. |

### 3.3. Pull Requests (PRs)

1.  Após finalizar o desenvolvimento em sua *branch* de *task*, o desenvolvedor deve abrir um **Pull Request (PR)**.
2.  O PR deve ter como **destino** a *branch* da sprint atual (Ex: `Sprint<número>`).
3.  O PR deve ser revisado por pelo menos um membro da equipe (Code Review).
4.  Após a **aprovação**, a *branch* de *task* é mergeada na *branch* da Sprint.
</details>

## <a id="tecnologias-utilizadas"> Tecnologias Utilizadas</a>

### **Back-end**
- **[Python:](https://www.python.org/)** Versão 3.13.7
- **[DJango:](https://www.djangoproject.com/)** Versão 5.2.6
- **[MongoDB:](https://www.mongodb.com/)** Versão 8.2

### **Front-end**
- **[Vue.js:](https://vuejs.org/)** Versão 3.5.13
- **[Vue Router:](https://router.vuejs.org/)** Versão 4.5.0
- **[Vuetify:](https://vuetifyjs.com/en/)** Versão 3.9.7
- **[Axios:](https://axios-http.com/)** Versão 1.8.4
- **[Chart.js:](https://www.chartjs.org/)** Versão 4.0

### **Ambiente de Execução**
- **[Node.js:](https://nodejs.org/pt)** Versão 22.14

### **Ferramentas de Desenvolvimento** 
- **[Vite:](https://vitejs.dev/)** Versão 6.2.1
- **[TypeScript:](https://www.typescriptlang.org/)** Versão 5.8.0
- **[Git:](https://git-scm.com/)** Controle de versão
- **[GitHub:](https://github.com/)** Repositório remoto
