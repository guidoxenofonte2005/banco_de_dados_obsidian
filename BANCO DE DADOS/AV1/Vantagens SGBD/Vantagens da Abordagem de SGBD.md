---
node_size: "5"
---
## [[Controle de Redundância]]
- No *desenvolvimento de software tradicional* com processamento de arquivos, *cada grupo de usuários mantém seus próprios arquivos* para tratar das suas aplicações de processamento de dados
- Essa redundância em armazenar os mesmos dados várias vezes *pode ocasionar vários problemas*:
	- **Duplicação de esforço**
	- **Desperdício de espaço de armazenamento**
	- **Possibilidade de inconsistência entre arquivos** que representam os mesmos dados
- Às vezes, é necessário o uso de **redundância controlada** para melhorar o desempenho das consultas
## [[Restrição de Acesso Não Autorizado]]
- Um SGBD *deve oferecer um subsistema de segurança e autorização,* disponível para uso do DBA para *criar contas e especificar restrições*
- Relaciona-se diretamente com o conceito de **software privilegiado**
## [[Armazenamento Persistente]]
- Bancos de dados podem ser usados para **oferecer armazenamento permanente para objetos e estruturas de dados** do programa
- Um dos principais motivos para se usar **sistemas de banco de dados orientados a objeto**
- Um objeto é considerado **persistente** quando **sobrevive ao término da execução e pode ser recuperado posteriormente** por outro programa
- Os sistemas tradicionais normalmente sofrem do ***problema de divergência de impedância***, pois as estruturas de dados fornecidas pelo SGBD eram incompatíveis com as estruturas da linguagem de programação
## [[Estruturas de Armazenamento e Processamento Eficiente de Consulta]]
- Sistemas de banco de dados *precisam oferecer capacidades para executar consultas e atualizações de maneira eficiente*
- Para isso, arquivos auxiliares chamados de **índices** são comumente utilizados
- O SGBD normalmente tem um **módulo de buffering ou caching** que *mantém partes do banco de dados nos buffers de memória principais*
- O módulo de **processamento e otimização de consulta** do SGBD é *responsável por escolher um plano de execução eficiente para cada consulta* com base nas estruturas de armazenamento existentes
## [[Backup e Recuperação]] 
- Um SGBD *precisa oferecer facilidades para se recuperar de falhas* de hardware ou software
- O **sistema de backup e recuperação** do SGBD é responsável pela recuperação
## [[Múltiplas Interfaces de Usuário]]
- *Visam reduzir a limitação de uso, dados os diferentes níveis de conhecimento técnico* dos usuários
- As interfaces no estilo de formulários e controladas por menus normalmente são conhecidas como **interfaces gráficas de usuário** (GUIs)
- *Geralmente envolve o uso de uma linguagem/ambiente especializado* para criação de GUIs
## [[Representação de Relacionamentos Complexos entre os Dados]]
## [[Imposição de Restrições de Integridade]]
- A *maioria das aplicações* de banco de dados *possui algumas restrições de integridade*
- O **tipo mais simples de restrição** envolve **especificar um tipo de dados para cada item** de dados
- Outro tipo de restrição especifica *unicidade sobre valores de item de dados*, como definição de valores obrigatórios e/ou únicos
	- Conhecido como **restrição de chave** ou **unicidade**
- São *derivadas do significado ou da **semântica dos dados*** e do que eles representam
- É *responsabilidade dos projetistas* do banco de dados *identificar restrições de integridade durante o projeto*
- **Um item** de dados **pode ser inserido erroneamente e ainda satisfazer as restrições de integridade** especificadas
- Regras que pertencem a um modelo de dados específico são chamadas de **regras inerentes ao modelo de dados**
## [[Permissão de Dedução e Ações usando Regras e Gatilhos]]
- Alguns sistemas de banco de dados oferecem capacidades para definir **regras de dedução** a fim de *inferir novas informações com base nos fatos armazenados no banco* de dados
- Os sistemas que oferecem tais capacidades são chamados de **sistemas de banco de dados dedutivos**
- Nos sistemas de banco de dados relacionais mais atuais, é possível associar **gatilhos/triggers** a tabelas
	- **Gatilho** - *Forma de regra ativada por atualizações na tabela*, que resulta na realização de operações adicionais
- Procedimentos mais elaborados para impor regras são popularmente chamados de **procedimentos armazenados** (*stored procedures*)
- A funcionalidade mais poderosa é fornecida por ***sistemas de banco de dados ativos***, que **oferecem regras ativas que automaticamente iniciam ações quando ocorrem certos eventos** e condições
## [[Implicações Adicionais]]
#### Potencial para Garantir Padrões
- O DBA pode **garantir padrões em um ambiente de banco de dados centralizado mais facilmente** do que em um ambiente no qual cada grupo de usuários tem controle dos seus próprios arquivos de dados e software
#### Tempo Reduzido para Desenvolvimento de Aplicação
- O **desenvolvimento de uma nova aplicação** - como a recuperação de certos dados para geração de um novo relatório - **leva um tempo consideravelmente curto**
- Estima-se que o *tempo de desenvolvimento usando um SGBD seja um sexto a um quarto* daquele para um sistema de arquivo tradicional
#### Flexibilidade
- Pode, em algum momento, ser necessário alterar a estrutura de um banco de dados à medida em que os requisitos mudam
- Os *SGBDs modernos permitem certos tipos de mudanças evolutivas na estrutura sem afetar os dados armazenados e os programas* de aplicação existentes
#### Disponibilidade de Informações Atualizadas
- Um SGBD **torna o banco de dados disponível a todos os usuários**
- A disponibilidade de informações atualizadas é possibilitada pelos subsistemas de *controle de ocorrência e recuperação* de um SGBD
#### Economias de Escala
- Permite a **consolidação de dados e aplicações, reduzindo a quantidade de sobreposição desperdiçada** entre as atividades do pessoal de processamento de dados em diferentes projetos/departamentos, **bem como as redundâncias entre aplicações**
- *Reduz os custos gerais de operação e gerenciamento*