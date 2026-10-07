<div align="center">

**CENTRO PAULA SOUZA**

**FACULDADE DE TECNOLOGIA DE JAHU**

**CURSO DE TECNOLOGIA EM DESENVOLVIMENTO DE SOFTWARE MULTIPLATAFORMA**

# DOCUMENTO DA APLICAÇÃO WEB

## Auxílio aos Problemas da Secretária

</div>

**Integrantes:**

- Daniel Augusto Melo
- Daniel Borges De Oliveira
- Maxwell da Silva Costa
- Michel Moraes Luz da Silva
- Tiago Miranda dos Santos

**Jahu, SP — 1º semestre/2026**

---

<details>
<summary><strong>Sumário</strong></summary>

- [1. Resumo da Aplicação Web](#1-resumo-da-aplicação-web)
  - [1.1 Objetivos](#11-objetivos)
  - [1.2 Métodos da Pesquisa](#12-métodos-da-pesquisa)
- [2. Documento de Requisitos](#2-documento-de-requisitos)
  - [2.1 Requisitos Funcionais](#21-requisitos-funcionais)
  - [2.2 Requisitos Não Funcionais](#22-requisitos-não-funcionais)
  - [2.3 Diagrama de Casos de Uso](#23-diagrama-de-casos-de-uso)
  - [2.4 Diagrama de Classes](#24-diagrama-de-classes)
- [3. Regras de Negócio](#3-regras-de-negócio)
- [4. Estudo de Viabilidade](#4-estudo-de-viabilidade)
  - [4.1 Viabilidade Técnica](#41-viabilidade-técnica)
  - [4.2 Viabilidade Financeira](#42-viabilidade-financeira)
  - [4.3 Viabilidade de Mercado](#43-viabilidade-de-mercado)
  - [4.4 Viabilidade Operacional](#44-viabilidade-operacional)
- [5. Modelo de Dados](#5-modelo-de-dados)
- [6. Design](#6-design)
- [7. Protótipo](#7-protótipo)
- [8. Aplicação](#8-aplicação)
- [9. Banco de Dados](#9-banco-de-dados)
- [10. Considerações Finais](#10-considerações-finais)
- [Referências Bibliográficas](#referências-bibliográficas)

</details>

---

## 1. Resumo da Aplicação Web

O projeto a ser desenvolvido tem como finalidade facilitar o dia a dia da secretária, pois existe uma demanda de problemas que poderiam ser resolvidos diretamente pelo sistema, que, além de deixar tudo automatizado e organizado, facilita mais do que apenas deixar documentos em Forms e procurar por e-mails.

### 1.1 Objetivos

Temos como objetivo a criação de um sistema que possa resolver praticamente toda a demanda da secretária de forma digitalizada e estruturada, com foco na facilidade da comunicação entre alunos e a secretária, pois, com essa facilitação, o resultado pode chegar mais rápido e modernizar grande parte dos processos.

### 1.2 Métodos da Pesquisa

O nosso método para a realização desse projeto é utilizar o que temos no momento, avaliando a forma de trabalho da secretária, as dificuldades dos alunos quanto aos aplicativos que atualmente são utilizados e a forma de solicitação de documentos, que atualmente é feita por Forms, WhatsApp, SIGA e e-mail. Então, com as ferramentas que já são utilizadas, nos cabe apenas uma junção das solicitações dentro de um sistema.

Portanto, através desse nosso sistema web, o aluno passará a conseguir solicitar, anexar e ter acesso a prazos de documentação, e a secretária terá uma melhor gestão de solução de problemas, facilitando o envio das solicitações, entre outras coisas que fazem parte do dia a dia.

---

## 2. Documento de Requisitos

Quando falamos em requisitos de um sistema, automaticamente o que vem à mente é o processo de estabelecer as funções e restrições que o sistema deve possuir, com base na solicitação do cliente.

Então, a documentação de requisitos se trata das descrições e dos detalhes do projeto, deixando claro o que será implantado.

### 2.1 Requisitos Funcionais

O sistema de secretaria deve permitir que o aluno registre demandas, acesse a plataforma informando seu CPF e visualize o andamento do atendimento em tempo real por meio de status (como 'em andamento' ou 'finalizado'), garantindo um canal direto de comunicação entre o aluno e a secretaria.

#### 2.1.1 Grupo de RF 1 – Interface do Sistema para os Alunos

- **RF 1 - Autenticação por CPF:** O sistema deve permitir que o aluno acesse a plataforma informando exclusivamente o seu número de CPF.
- **RF 2 - Menu de Solicitações:** O sistema deve exibir um menu digital interativo substituindo os formulários antigos por botões de requisição direta.

#### 2.1.2 Grupo de RF 2 – Direcionamento Externo

- **RF 4 - Alerta de Solicitações Externas:** O sistema deve exibir uma mensagem de aviso e um link de redirecionamento para a plataforma SIGA quando o aluno tentar solicitar um documento específico que não seja gerido pela secretaria.

#### 2.1.3 Grupo de RF 3 – Interface do Sistema da Secretária

- **RF 5 - Painel de Gestão de Ocorrências:** O sistema deve disponibilizar uma tela para a secretaria gerenciar os protocolos através de filtros de status (*A resolver*, *Em andamento*, *Resolvidos*).
- **RF 6 - Atualização de Status:** A secretaria deve ser capaz de alterar o status das ocorrências dos alunos.
- **RF 7 - Armazenamento de Links de Certificação:** O sistema deve permitir que a secretaria cadastre e armazene links de certificação digital atrelados aos documentos gerados.

### 2.2 Requisitos Não Funcionais

Os requisitos não funcionais focam na qualidade do nosso sistema, ou seja, no desempenho, na segurança, na responsividade e na usabilidade.

#### 2.2.1 Requisitos de Produto

- **RNF 1 - Responsividade (Aluno):** A interface do aluno deve ser totalmente responsiva, adaptando-se a dispositivos móveis e desktops.
- **RNF 2 - Otimização Desktop (Secretaria):** A interface da secretaria deve ser otimizada para telas desktop, priorizando a visualização de painéis e tabelas de protocolos.
- **RNF 3 - Usabilidade e Simplicidade:** O sistema deve substituir os antigos formulários (*Forms*) por um fluxo dinâmico, permitindo a abertura de uma solicitação com no máximo 3 cliques.

#### 2.2.2 Requisitos de Organização

- **RNF 4 - Entrega e Validação Incremental:** A interface do aluno deve ser prototipada, testada e homologada antes da liberação final do módulo de atendimento da secretaria.

#### 2.2.3 Requisitos de Confiabilidade

- **RNF 7 - Preservação de Dados (Backup):** O armazenamento dos links de certificação digital e o histórico de status dos protocolos devem possuir rotinas automatizadas de backup diário para evitar a perda de informações.

#### 2.2.4 Requisitos de Implementação

- **RNF 9 - Tecnologia Web:** O sistema deve ser desenvolvido utilizando tecnologias web modernas que permitam a execução direta no navegador, sem a necessidade de instalação de softwares locais nas máquinas da secretaria.
- **RNF 10 - Arquitetura Leve:** A aplicação deve ser implementada de modo a consumir o mínimo de banda de internet.

#### 2.2.5 Requisitos de Padrões

- **RNF 11 - Padrão de Acesso Simplificado:** O acesso do aluno deve seguir estritamente o padrão de identificação única via campo de **CPF**, sem a exigência de criação de senhas complexas nesta primeira fase.
- **RNF 12 - Conformidade com a LGPD:** O tratamento do CPF e dos dados de ocorrências dos alunos deve seguir rigorosamente os padrões legais da Lei Geral de Proteção de Dados (Lei nº 13.709).
- **RNF 13 - Identidade Visual:** O sistema deve seguir o padrão visual e de cores.

#### 2.2.6 Requisitos de Interoperabilidade

- **RNF 14 - Redirecionamento para o SIGA:** O sistema deve ser capaz de identificar solicitações restritas e realizar o direcionamento externo (links/avisos) de forma integrada e funcional para a plataforma SIGA.
- **RNF 15 - Integração de Certificação Digital:** O campo de armazenamento da secretaria deve ser compatível com links gerados por plataformas externas de certificação digital reconhecidas.

### 2.3 Diagrama de Casos de Uso

### 2.4 Diagrama de Classes

---

## 3. Regras de Negócio

---

## 4. Estudo de Viabilidade

### 4.1 Viabilidade Técnica

A viabilidade técnica é sustentada pelas competências práticas desenvolvidas nas disciplinas de Engenharia de Software, Desenvolvimento Web e Design Digital. Tecnicamente, o desafio consiste em centralizar os fluxos fragmentados (atualmente distribuídos em Microsoft Forms, WhatsApp, SIGA e e-mail) em uma plataforma única. O sistema utilizará tecnologia web acessível para implementar o mecanismo de autenticação por CPF, o upload de anexos e o motor de atualização de status em tempo real ('em andamento' ou 'finalizado'). A infraestrutura física e de rede necessária para o desenvolvimento é integralmente fornecida pelos laboratórios da Fatec.

### 4.2 Viabilidade Financeira

O projeto apresenta custo financeiro direto nulo, visto que toda a infraestrutura de hardware, conectividade e ferramentas de desenvolvimento já estão disponíveis na instituição. A substituição das ferramentas gratuitas e descentralizadas (como Forms e e-mails manuais) por um sistema web customizado não gerará custos de licenciamento. O investimento resume-se à mão de obra dos próprios alunos, cujo cronograma está dimensionado para o período letivo. O retorno financeiro indireto se dará pela redução do tempo de atendimento e otimização da força de trabalho da secretaria, além do ganho de produtividade acadêmica para os alunos, gerando valor imaterial para a instituição.

### 4.3 Viabilidade de Mercado

Por se tratar de um software sob medida para uso interno, a viabilidade de mercado avalia o impacto da solução frente às alternativas atuais. O sistema proposto valida-se ao solucionar a ineficiência da pulverização de canais, unificando as interações em um ambiente digital estruturado. O mercado-alvo (composto pelo corpo discente e pela equipe administrativa da Fatec) apresenta alta receptividade, pois a solução elimina processos manuais e resolve diretamente a dificuldade dos alunos no acompanhamento de prazos e na solicitação de documentos, estabelecendo um padrão de modernização institucional.

### 4.4 Viabilidade Operacional

A viabilidade operacional é alta, pois o sistema foi desenhado com base em um método de pesquisa que avaliou a rotina real da secretaria e as dores dos alunos. A transição para o novo sistema será natural, pois a secretaria passará a gerir todas as demandas em uma única tela de controle, facilitando o envio de respostas. Para os alunos, a usabilidade baseada em Design Digital garantirá que o ato de solicitar documentos, anexar arquivos e consultar prazos seja simples e intuitivo. O apoio consultivo dos professores garante a qualidade do deploy, e a facilidade operacional do software assegura que ele será plenamente adotado no dia a dia da secretaria.

---

## 5. Modelo de Dados

- Modelo conceitual
- Modelo lógico
- Físico

---

## 6. Design

- Paleta de cor
- Tipografia
- Logo
- Wireframe
- Modelo de navegação

---

## 7. Protótipo

Gere um protótipo funcional na ferramenta que se sentir mais confortável (Figma, por exemplo) e apresente aqui, indicando o link.

---

## 8. Aplicação

Apresente o processo de desenvolvimento, as etapas, algumas telas da Aplicação, atualizadas agora com Banco de Dados.

---

## 9. Banco de Dados

(MODELO CONCEITUAL)

---

## 10. Considerações Finais

Faça uma breve contextualização do processo de desenvolvimento da Aplicação, comente sobre limitações, dificuldades enfrentadas, contribuições da Aplicação etc.

---

## Referências Bibliográficas
