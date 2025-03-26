---
node_size: "5"
---
## [[Linguagens do SGBD]]
#### Data Definition Language - DDL
- Usada pelo DBA e projetistas de banco de dados para **definir os esquemas conceituais e internos**
- *O SGBD terá um compilador da DDL* cuja função é *processar funções desta linguagem a fim de identificar as restrições dos construtores de esquema e armazenar a descrição de esquema no catálogo* do SGBD
- Nos SGBDs que mantém uma *separação clara entre os níveis conceitual e interno, a DDL é usada para especificar apenas o esquema conceitual*
#### Storage Definition Language - SDL
- Utilizada para **especificar o esquema interno**
- Os *mapeamentos entre os esquemas conceituais e internos podem ser especificados usando linguagens DDL ou SDL*
- Na maioria dos SGBDs relacionais, *não existe uma linguagem específica que realize o papel de SDL*
- Em vez disso, **o esquema interno é especificado por uma combinação de funções, parâmetros e especificações relacionadas ao armazenamento de arquivos**, permitindo ao DBA controlar opções de indexação e mapeamento de dados
#### View Definition Language - VDE
- Usada para obter uma verdadeira arquitetura de três esquemas, **especifica visões do usuário e seus mapeamentos ao esquema conceitual**
- Na maioria dos SGBDs, *a DDL é usada para definir tanto o esquema conceitual como o externo*
- Nos *SGBDs relacionais*, a *SQL é usada no papel de VDL* para definir visões do usuário ou da aplicação como resultados de consultas predefinidas
#### Data Manipulation Language - DML
- Usada para **realizar manipulações nos dados presentes no banco**
- As manipulações típicas incluem **recuperação, inserção, exclusão e modificação** dos dados
- Existem *dois tipos de DML*:
	**Alto Nível**
	- Também chamada de **DML não procedural**, pode ser utilizada para *especificar operações de banco de dados complexas de forma concisa*
	- DMLs de alto nível, como a SQL, **podem especificar e recuperar muitos registros em uma única instrução DML** e, por conta disso, são chamadas de **DMLs orientadas a conjunto** ou **DMLs de um conjunto de cada vez**
	**Baixo Nível** 
	- Também chamada de **DML procedural**, *deve ser embutida em uma linguagem de programação de uso geral*
	- *Recupera registros individuais ou objetos do banco de dados e processa cada um deles separadamente*, sendo chamadas também de **DMLs de um registro por vez**
- Nos SGBDs atuais, *geralmente uma única linguagem integrada e abrangente é usada na definição do esquema conceitual, definição de visão e manipulação de dados*
## [[Interfaces do SGBD]]
#### Interfaces Baseadas em Menu
- Apresentam ao usuário menus que acompanham o mesmo na formulação de uma solicitação
- Os menus *acabam com a necessidade de memorizar os comandos específicos e a sintaxe de uma linguagem de consulta*
#### Aplicativos para Dispositivos Móveis
- Dão acesso aos dados para os usuários móveis
- Os aplicativos *possuem interfaces programadas embutidas que permitem que os usuários acessem opções limitadas* para o acesso móvel aos dados do usuário
#### Interfaces Baseadas em Formulário
- Apresenta um formulário para cada usuário
- *Os usuários podem preencher todas as entradas para inserir novos dados ou preencher apenas certas entradas, caso o SGBD seja capaz de recuperar/inferir os dados correspondentes às entradas restantes*
- Normalmente são *projetados e programados para usuários finais como interfaces para transações já programadas*
- *Muitos SGBDs possuem linguagens de especificação de formulários*, que ajudam os programadores a especificar tais formulários
#### Interfaces Gráficas com o Usuário
- Uma GUI *normalmente apresenta um esquema para o usuário em formato de diagrama, que pode ser manipulado pelo usuário*
- Em muitos casos, as GUIs *utilizam menus e formulários*
#### Interfaces de Linguagem Natural
- *Aceitam solicitações escritas em alguma linguagem do mundo real e*, por meio de algoritmos, *tentam compreendê-la*
- **Costumam ter o próprio esquema**, semelhante ao esquema conceitual do banco de dados
- Se a interpretação for bem-sucedida, a interface gera uma consulta de alto nível correspondente à solicitação de linguagem natural e a submete ao SGBD para processamento
- Caso contrário, é realizada uma tentativa adicional de esclarecimento da solicitação
#### Pesquisa do Banco de Dados baseada em Palavra-Chave
- **Semelhantes aos mecanismos de busca**
- *Utilizam índices predefinidos sobre palavras e funções de pontuação* (ranking) *para recuperar e apresentar documentos resultantes* em um grau decrescente de combinação
#### Entrada e Saída de Voz
- A entrada de voz é detectada com o uso de uma biblioteca de palavras predefinidas e usadas para configurar os parâmetros fornecidos para as consultas
- Para a saída, ocorre uma conversão semelhante, mas com o propósito inverso
#### Interfaces para Usuários Paramétricos
#### Interfaces para o DBA