# Auxílio aos Problemas da Secretária

**Centro Paula Souza — Faculdade de Tecnologia de Jahu**
Curso de Tecnologia em Desenvolvimento de Software Multiplataforma
**Documento da Aplicação Web** · Jahu, SP · 1º semestre/2026

## Integrantes

- Daniel Augusto Melo
- Daniel Borges De Oliveira
- Maxwell da Silva Costa
- Michel Moraes Luz da Silva
- Tiago Miranda dos Santos

## Sumário

1. [Resumo da Aplicação Web](#1-resumo-da-aplicação-web)
2. [Documento de Requisitos](#2-documento-de-requisitos)
3. [Regras de Negócio](#3-regras-de-negócio)
4. [Estudo de Viabilidade](#4-estudo-de-viabilidade)
5. [Modelo de Dados](#5-modelo-de-dados)
6. [Design](#6-design)
7. [Protótipo](#7-protótipo)
8. [Aplicação](#8-aplicação)
9. [Banco de Dados](#9-banco-de-dados)
10. [Considerações Finais](#10-considerações-finais)
11. [Referências Bibliográficas](#referências-bibliográficas)

---

## 1. Resumo da Aplicação Web

O projeto a ser desenvolvido tem como finalidade facilitar o dia a dia da secretária, pois existe uma demanda de problemas que poderia ser resolvida diretamente pelo sistema, que além de deixar tudo automatizado e organizado, facilita em relação a apenas deixar documentos em Forms e procurar por e-mails.

### 1.1 Objetivos

Temos como objetivo a criação de um sistema que possa praticamente resolver toda a demanda da secretária de forma digitalizada e estruturada, com foco na facilidade da comunicação entre alunos e a secretária. Com essa facilitação, o resultado pode chegar mais rápido e modernizar grande parte dos processos.

### 1.2 Métodos da Pesquisa

Os nossos métodos para realização deste projeto consistem em usar o que temos no momento, avaliando a forma de trabalho da secretária, as dificuldades dos alunos quanto aos aplicativos que atualmente são utilizados e a forma de solicitação de documentos, que atualmente é por Forms, WhatsApp, SIGA e e-mail. Com as ferramentas que já são utilizadas, nos cabe apenas uma junção das solicitações dentro de um sistema.

Portanto, através do nosso sistema web, o aluno passará a conseguir solicitar, anexar e ter acesso a prazos de documentação. E a secretária terá uma melhor gestão de solução de problemas e facilidade no envio das solicitações, entre outras coisas que fazem parte do dia a dia.

---

## 2. Documento de Requisitos

Quando se fala em requisitos de um sistema, automaticamente o que vem à mente é o processo de estabelecer as funções e restrições que o sistema deve possuir, com base na solicitação do cliente.

Então, a documentação de requisitos trata das descrições e detalhes do projeto, deixando claro o que será implantado.

### 2.1 Requisitos Funcionais

O sistema de secretaria deve permitir que o aluno registre demandas, acesse a plataforma informando seu CPF e visualize o andamento do atendimento em tempo real por meio de status (como "em andamento" ou "finalizado"), garantindo um canal direto de comunicação entre o aluno e a secretaria.

#### 2.1.1 Interface do Sistema para os Alunos

- **RF 1 – Autenticar por CPF:** o sistema deve permitir que o aluno acesse a plataforma informando exclusivamente o seu número de CPF.
- **RF 2 – Exibir Menu de Solicitações:** o sistema deve exibir um menu digital interativo, substituindo os formulários antigos por botões de requisição direta, com atributos: emissão de certificados, emissão de atestado etc.
- **RF 3 – Emitir Alerta de Solicitações Externas:** o sistema deve exibir uma mensagem de aviso e um link de redirecionamento para a plataforma SIGA quando o aluno tentar solicitar um documento específico que não seja gerido pela secretaria.

#### 2.1.2 Interface do Sistema da Secretária

- **RF 4 – Expor painel de gestão de ocorrências:** o sistema deve disponibilizar uma tela para a secretaria gerenciar os protocolos através de filtros de status (*A resolver*, *Em andamento*, *Resolvidos*).
- **RF 5 – Atualizar status:** a secretaria deve ser capaz de alterar o status das ocorrências dos alunos.
- **RF 6 – Armazenar links de certificação:** o sistema deve permitir que a secretaria cadastre e armazene links de certificação digital atrelados aos documentos gerados.

### 2.2 Requisitos Não Funcionais

Os requisitos não funcionais focam na qualidade do nosso sistema, ou seja, o desempenho, a segurança, a responsividade e a usabilidade.

#### 2.2.1 Requisitos de Produto

- **RNF 1 – Responsividade (Aluno):** a interface do aluno deve ser totalmente responsiva, adaptando-se a dispositivos móveis e desktops.
- **RNF 2 – Otimização Desktop (Secretaria):** a interface da secretaria deve ser otimizada para telas desktop, priorizando a visualização de painéis e tabelas de protocolos.
- **RNF 3 – Usabilidade e Simplicidade:** o sistema deve substituir os antigos formulários (*Forms*) por um fluxo dinâmico, permitindo a abertura de uma solicitação com no máximo 3 cliques.

#### 2.2.2 Requisitos de Organização

- **RNF 4 – Entrega e Validação Incremental:** a interface do aluno deve ser prototipada, testada e homologada antes da liberação final do módulo de atendimento da secretaria.

#### 2.2.3 Requisitos de Confiabilidade

- **RNF 7 – Preservação de Dados (Backup):** o armazenamento dos links de certificação digital e o histórico de status dos protocolos devem possuir rotinas automatizadas de backup diário para evitar a perda de informações.

#### 2.2.4 Requisitos de Implementação

- **RNF 9 – Tecnologia Web:** o sistema deve ser desenvolvido utilizando tecnologias web modernas que permitam a execução direta no navegador, sem a necessidade de instalação de softwares locais nas máquinas da secretaria.
- **RNF 10 – Arquitetura Leve:** a aplicação deve ser implementada de modo a consumir o mínimo de banda de internet.

#### 2.2.5 Requisitos de Padrões

- **RNF 11 – Padrão de Acesso Simplificado:** o acesso do aluno deve seguir estritamente o padrão de identificação única via campo de **CPF**, sem a exigência de criação de senhas complexas nesta primeira fase.
- **RNF 12 – Conformidade com a LGPD:** o tratamento do CPF e dos dados de ocorrências dos alunos deve seguir rigorosamente os padrões legais da Lei Geral de Proteção de Dados (Lei nº 13.709).
- **RNF 13 – Identidade Visual:** o sistema deve seguir o padrão visual e de cores.

#### 2.2.6 Requisitos de Interoperabilidade

- **RNF 14 – Redirecionamento para o SIGA:** o sistema deve ser capaz de identificar solicitações restritas e realizar o direcionamento externo (links/avisos) de forma integrada e funcional para a plataforma SIGA.
- **RNF 15 – Integração de Certificação Digital:** o campo de armazenamento da secretaria deve ser compatível com links gerados por plataformas externas de certificação digital reconhecidas.

### 2.3 Diagrama de Casos de Uso

<!-- Adicione a imagem do diagrama: ![Diagrama de Casos de Uso](imagens/casos-de-uso.png) -->

### 2.4 Diagrama de Classes

<!-- Adicione a imagem do diagrama: ![Diagrama de Classes](imagens/classes.png) -->

---

## 3. Regras de Negócio

Para nossa regra de negócios utilizamos o Business Model Canvas, que é uma ferramenta de gestão estratégica que permite esboçar e estruturar o modelo de funcionamento de um projeto através de 9 blocos fundamentais. No contexto deste projeto, estabelece as diretrizes operacionais para transformar a gestão manual da secretaria em um fluxo digital.

<!-- Adicione a imagem do canvas: ![Business Model Canvas](imagens/canvas.png) -->

Para melhor entendimento dos blocos da imagem, segue um resumo de como cada um desses 9 blocos se encaixa no nosso sistema da secretária:

### 1. Segmento de Mercado

Define os diferentes grupos de pessoas ou organizações que a aplicação visa atender e gerar valor.

No nosso projeto, ele concentra-se nos **Alunos da Fatec Jahu**, que necessitam de um canal ágil para solicitar documentos e acompanhar prazos, e na **Equipe da Secretaria**, que demanda um painel gerencial para monitorar solicitações através de atualizações de status (não respondido, em atendimento e finalizado).

### 2. Proposta de Valor

O conjunto de produtos, serviços e diferenciais que criam valor para um segmento de cliente específico, resolvendo um problema ou satisfazendo uma necessidade.

Projetamos o sistema para oferecer transparência total aos estudantes por meio do acompanhamento em tempo real das solicitações via CPF, além de promover agilidade operacional ao substituir formulários estáticos e fragmentados por um fluxo de atendimento dinâmico, resolvido em até 3 cliques.

### 3. Canais

Descreve como a aplicação se comunica e alcança seus segmentos de clientes para entregar sua proposta de valor.

Centralizado em um Portal Web institucional, com interface totalmente responsiva, adaptada para celulares e computadores, operando também como um indexador de avisos e links de redirecionamento integrado para a plataforma oficial SIGA.

### 4. Relacionamento com o Cliente

Estabelece o tipo de relação e as estratégias de interação que a aplicação mantém com cada segmento de cliente.

Baseia-se no autoatendimento simples, rápido e intuitivo, proporcionando clareza informativa com o uso de filtros de status públicos ("A resolver", "Em andamento", "Resolvido") e garantindo a privacidade dos dados sob estrita conformidade com a LGPD.

### 5. Fontes de Renda

Representa a forma como o projeto gera valor, receita ou retornos justificáveis para a organização que o mantém.

Para este sistema, o retorno é imaterial, focado na otimização do tempo de atendimento e no aumento da produtividade acadêmica, gerando uma significativa economia institucional pela redução drástica do retrabalho manual com e-mails e planilhas.

### 6. Recursos Chave

Os ativos e meios mais importantes exigidos para fazer o modelo de negócios funcionar e viabilizar a proposta de valor.

No nosso sistema, consistem na infraestrutura física de rede e computadores dos laboratórios da Fatec Jahu e na força de trabalho da equipe de desenvolvedores, ou seja, os alunos do curso de DSM.

### 7. Atividades Chave

As ações e rotinas mais cruciais que a equipe e o sistema devem executar frequentemente para manter a operação ativa.

O sistema contempla os processos de autenticação simplificada e segura através do CPF, a triagem automatizada para o encaminhamento interno de chamados, o cadastro e armazenamento de links de certificação digital e a execução de backups diários automáticos.

### 8. Parceiros Chave

A rede de fornecedores, aliados e agentes externos que contribuem para a otimização, redução de riscos ou expansão dos recursos do projeto.

Neste caso, envolve o Sistema Acadêmico SIGA (essencial para o redirecionamento de requisições específicas), o suporte consultivo do corpo docente e professores orientadores da instituição, e as plataformas externas de certificação digital integradas.

### 9. Estrutura de Custos

Descreve todos os custos operacionais, financeiros e de recursos direcionados para a construção e manutenção do modelo de negócios.

Neste caso, configura-se com custo monetário nulo, em decorrência do aproveitamento de tecnologias open-source e da infraestrutura computacional já existente na Fatec, somado ao investimento de horas através da alocação do tempo letivo dos alunos desenvolvedores.

---

## 4. Estudo de Viabilidade

### 4.1 Viabilidade Técnica

A viabilidade técnica é sustentada pelas competências práticas desenvolvidas nas disciplinas de Engenharia de Software, Desenvolvimento Web e Design Digital. Tecnicamente, o desafio consiste em centralizar os fluxos fragmentados (atualmente distribuídos em Microsoft Forms, WhatsApp, SIGA e e-mail) em uma plataforma única. O sistema utilizará tecnologia web acessível para implementar o mecanismo de autenticação por CPF, o upload de anexos e o motor de atualização de status em tempo real ("em andamento" ou "finalizado"). A infraestrutura física e de rede necessária para o desenvolvimento é integralmente fornecida pelos laboratórios da Fatec.

### 4.2 Viabilidade Financeira

O projeto apresenta custo financeiro direto nulo, visto que toda a infraestrutura de hardware, conectividade e ferramentas de desenvolvimento já estão disponíveis na instituição. A substituição das ferramentas gratuitas e descentralizadas (como Forms e e-mails manuais) por um sistema web customizado não gerará custos de licenciamento. O investimento resume-se à mão de obra de nós, alunos, cujo cronograma está dimensionado para o período letivo. O retorno financeiro indireto se dará pela redução do tempo de atendimento e otimização da força de trabalho da secretaria, além do ganho de produtividade acadêmica para os alunos, gerando valor imaterial para a instituição.

### 4.3 Viabilidade de Mercado

Por se tratar de um software sob medida para uso interno, a viabilidade de mercado avalia o impacto da solução frente às alternativas atuais. O sistema proposto valida-se ao solucionar a ineficiência da pulverização de canais, unificando as interações em um ambiente digital estruturado. O mercado-alvo (composto pelo corpo discente e pela equipe administrativa da Fatec) apresenta alta receptividade, pois a solução elimina processos manuais e resolve diretamente a dificuldade dos alunos no acompanhamento de prazos e na solicitação de documentos, estabelecendo um padrão de modernização institucional.

### 4.4 Viabilidade Operacional

A viabilidade operacional é alta, pois o sistema foi desenhado com base em um método de pesquisa que avaliou a rotina real da secretaria e as dores dos alunos. A transição para o novo sistema será natural, pois a secretaria passará a gerir todas as demandas em uma única tela de controle, facilitando o envio de respostas. Para os alunos, a usabilidade baseada em Design Digital garantirá que o ato de solicitar documentos, anexar arquivos e consultar prazos seja simples e intuitivo. O apoio consultivo dos professores garante a qualidade do deploy, e a facilidade operacional do software assegura que ele será plenamente adotado no dia a dia da secretaria.

---

## 5. Modelo de Dados

- Modelo conceitual
- Modelo lógico
- Modelo físico

---

## 6. Design

- Paleta de cores
- Tipografia
- Logo
- Wireframe
- Modelo de navegação

---

## 7. Protótipo

<!-- Adicione aqui o link do protótipo (Figma, por exemplo). -->

---

## 8. Aplicação

<!-- Apresente o processo de desenvolvimento, as etapas e algumas telas da aplicação, atualizadas com o banco de dados. -->

---

## 9. Banco de Dados

<!-- Modelo conceitual -->

---

## 10. Considerações Finais

<!-- Contextualização do processo de desenvolvimento, limitações, dificuldades enfrentadas e contribuições da aplicação. -->

---

## Referências Bibliográficas

<!-- Liste aqui as referências utilizadas. -->
