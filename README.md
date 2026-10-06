<div align="center">

CENTRO PAULA SOUZA

FACULDADE DE TECNOLOGIA DE JAHU

CURSO DE TECNOLOGIA EM DESENVOLVIMENTO DE SOFTWARE MULTIPLATAFORMA

DOCUMENTO DA APLICAÇÃO WEB
Auxílio aos Problemas da Secretária
</div>

Integrantes:

Daniel Augusto Melo
Daniel Borges De Oliveira
Maxwell da Silva Costa
Michel Moraes Luz da Silva
Tiago Miranda dos Santos

Jahu, SP — 1º semestre/2026

<details> <summary><strong>Sumário</strong></summary>
1. Resumo da Aplicação Web
1.1 Objetivos
1.2 Métodos da Pesquisa
2. Documento de Requisitos
2.1 Requisitos Funcionais
2.2 Requisitos Não Funcionais
2.3 Diagrama de Casos de Uso
2.4 Diagrama de Classes
3. Regras de Negócio
4. Estudo de Viabilidade
5. Modelo de Dados
6. Design
7. Protótipo
8. Aplicação
9. Banco de Dados
10. Considerações Finais
Referências Bibliográficas
</details>
1. Resumo da Aplicação Web

O projeto a ser desenvolvido tem como finalidade facilitar o dia a dia da secretária, pois existe uma demanda de problemas que poderiam ser resolvidos diretamente pelo sistema, que, além de deixar tudo automatizado e organizado, facilita mais do que apenas deixar documentos em Forms e procurar por e-mails.

1.1 Objetivos

Temos como objetivo a criação de um sistema que possa resolver praticamente toda a demanda da secretária de forma digitalizada e estruturada, com foco na facilidade da comunicação entre alunos e a secretária, pois, com essa facilitação, o resultado pode chegar mais rápido e modernizar grande parte dos processos.

1.2 Métodos da Pesquisa

O nosso método para a realização desse projeto é utilizar o que temos no momento, avaliando a forma de trabalho da secretária, as dificuldades dos alunos quanto aos aplicativos que atualmente são utilizados e a forma de solicitação de documentos, que atualmente é feita por Forms, WhatsApp, SIGA e e-mail. Então, com as ferramentas que já são utilizadas, nos cabe apenas uma junção das solicitações dentro de um sistema.

Portanto, através desse nosso sistema web, o aluno passará a conseguir solicitar, anexar e ter acesso a prazos de documentação, e a secretária terá uma melhor gestão de solução de problemas, facilitando o envio das solicitações, entre outras coisas que fazem parte do dia a dia.

2. Documento de Requisitos

Quando falamos em requisitos de um sistema, automaticamente o que vem à mente é o processo de estabelecer as funções e restrições que o sistema deve possuir, com base na solicitação do cliente.

Então, a documentação de requisitos se trata das descrições e dos detalhes do projeto, deixando claro o que será implantado.

2.1 Requisitos Funcionais

O sistema de secretaria deve permitir que o aluno registre demandas, acesse a plataforma informando seu CPF e visualize o andamento do atendimento em tempo real por meio de status (como 'em andamento' ou 'finalizado'), garantindo um canal direto de comunicação entre o aluno e a secretaria.

2.1.1 Grupo de RF 1 – Interface do Sistema para os Alunos
RF01 - Autenticação por CPF: O sistema deve permitir que o aluno acesse a plataforma informando exclusivamente o seu número de CPF.
RF002 - Menu de Solicitações: O sistema deve exibir um menu digital interativo substituindo os formulários antigos por botões de requisição direta.
2.1.2 Grupo de RF 2 – Direcionamento Externo
RF04 - Alerta de Solicitações Externas: O sistema deve exibir uma mensagem de aviso e um link de redirecionamento para a plataforma SIGA quando o aluno tentar solicitar um documento específico que não seja gerido pela secretaria.
2.1.3 Grupo de RF 3 – Interface do Sistema da Secretária
RF005 - Painel de Gestão de Ocorrências: O sistema deve disponibilizar uma tela para a secretaria gerenciar os protocolos através de filtros de status (A resolver, Em andamento, Resolvidos).
RF006 - Atualização de Status: A secretaria deve ser capaz de alterar o status das ocorrências dos alunos.
RF007 - Armazenamento de Links de Certificação: O sistema deve permitir que a secretaria cadastre e armazene links de certificação digital atrelados aos documentos gerados.
2.2 Requisitos Não Funcionais

Os requisitos não funcionais focam na qualidade do nosso sistema, ou seja, no desempenho, na segurança, na responsividade e na usabilidade.

• Requisitos de Produto

RNF001 - Responsividade (Aluno): A interface do aluno deve ser totalmente responsiva, adaptando-se a dispositivos móveis e desktops.
RNF002 - Otimização Desktop (Secretaria): A interface da secretaria deve ser otimizada para telas desktop, priorizando a visualização de painéis e tabelas de protocolos.
RNF003 - Usabilidade e Simplicidade: O sistema deve substituir os antigos formulários (Forms) por um fluxo dinâmico, permitindo a abertura de uma solicitação com no máximo 3 cliques.

• Requisitos de Organização

RNF004 - Entrega e Validação Incremental: A interface do aluno deve ser prototipada, testada e homologada antes da liberação final do módulo de atendimento da secretaria.

• Requisitos de Confiabilidade

RNF007 - Preservação de Dados (Backup): O armazenamento dos links de certificação digital e o histórico de status dos protocolos devem possuir rotinas automatizadas de backup diário para evitar a perda de informações.

• Requisitos de Implementação

RNF009 - Tecnologia Web: O sistema deve ser desenvolvido utilizando tecnologias web modernas que permitam a execução direta no navegador, sem a necessidade de instalação de softwares locais nas máquinas da secretaria.
RNF010 - Arquitetura Leve: A aplicação deve ser implementada de modo a consumir o mínimo de banda de internet.

• Requisitos de Padrões

RNF011 - Padrão de Acesso Simplificado: O acesso do aluno deve seguir estritamente o padrão de identificação única via campo de CPF, sem a exigência de criação de senhas complexas nesta primeira fase.
RNF012 - Conformidade com a LGPD: O tratamento do CPF e dos dados de ocorrências dos alunos deve seguir rigorosamente os padrões legais da Lei Geral de Proteção de Dados (Lei nº 13.709).
RNF013 - Identidade Visual: O sistema deve seguir o padrão visual e de cores.

• Requisitos de Interoperabilidade

RNF014 - Redirecionamento para o SIGA: O sistema deve ser capaz de identificar solicitações restritas e realizar o direcionamento externo (links/avisos) de forma integrada e funcional para a plataforma SIGA.
RNF015 - Integração de Certificação Digital: O campo de armazenamento da secretaria deve ser compatível com links gerados por plataformas externas de certificação digital reconhecidas.
2.3 Diagrama de Casos de Uso
2.4 Diagrama de Classes
3. Regras de Negócio
4. Estudo de Viabilidade

(TÉCNICA, FINANCEIRA, DE MERCADO, OPERACIONAL)

5. Modelo de Dados
Modelo conceitual
Modelo lógico
Físico
6. Design
Paleta de cor
Tipografia
Logo
Wireframe
Modelo de navegação
7. Protótipo

Gere um protótipo funcional na ferramenta que se sentir mais confortável (Figma, por exemplo) e apresente aqui, indicando o link.

8. Aplicação

Apresente o processo de desenvolvimento, as etapas, algumas telas da Aplicação, atualizadas agora com Banco de Dados.

9. Banco de Dados

(MODELO CONCEITUAL)

10. Considerações Finais

Faça uma breve contextualização do processo de desenvolvimento da Aplicação, comente sobre limitações, dificuldades enfrentadas, contribuições da Aplicação etc.

Referências Bibliográficas
