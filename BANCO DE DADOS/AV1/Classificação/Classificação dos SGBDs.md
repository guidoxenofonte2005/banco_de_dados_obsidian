---
node_size: "5"
aliases:
---
## Critério 1: [[Modelo de Dados]]
#### Modelo Relacional
- Representa um banco de dados como uma **coleção de tabelas**, onde *cada tabela pode ser armazenada como um arquivo separado*
- *A maior parte dos bancos de dados relacionais usa a linguagem de consulta de alto nível (SQL)* e admite uma forma limitada de visões do usuário
#### Modelo de Objeto
- Define um **banco de dados em termos de objetos, suas propriedades e operações**
- *Objetos com a mesma estrutura e comportamento* pertencem a uma **classe**, e *as classes são organizadas em **hierarquias***
- As *operações de cada classe são especificadas com procedimentos predefinidos*, chamados **métodos**
- Os *SGBDs relacionais têm estendido seus modelos para incorporar conceitos de banco de dados de objeto* e outras funcionalidades, originando os chamados **sistemas objeto-relacional** ou **sistemas relacionais estendidos**
#### Modelo de Chave-Valor
- *Associa uma chave única a cada valor* (que pode ser um registro ou um objeto) e *fornece acesso muito rápido a um valor a partir de sua chave*
#### Modelo de Documento
- *Baseado em **JSON*** (Java Script Object Notation)
- *Armazena os dados como documentos* semelhantes a objetos complexos
#### Modelo de Grafo
- *Armazena objetos como **nós de um grafo***
- As *relações entre objetos* são representadas como *arestas direcionadas do grafo*
#### Modelo Baseado em Coluna
- *Armazenam as colunas de linhas agrupadas em várias páginas de disco*
- Garantem um *acesso mais rápido* e permitem *múltiplas versões dos dados*
#### Modelo XML
- **Surgiu como um padrão para troca de dados pela web** e foi *usado como base para implementar vários protótipos de sistemas com XML nativa*
- Os **dados são representados como elementos**. Com o uso de tags, os dados podem ser aninhados para criar estruturas hierárquicas complexas
#### Modelos Legados (Rede e Hierárquico)
## Critério 2: [[Número de Usuários]]
#### Sistemas Monousuário
- Admitem **apenas um usuário de cada vez**
- Usados *principalmente com computadores pessoais*
#### Sistemas Multiusuário
- Incluem a *maioria dos SGBDs*
- Admitem **múltiplos usuários simultaneamente**
## Critério 3: [[Número de Locais]]
#### SGBD Centralizado
- Os **dados estão armazenados em um único computador**
- *Pode atender a vários usuários, mas o SGBD e o banco de dados residem integralmente em um único computador*
#### SGBD Distribuído
- Também chamados de **SGBDDs**, *podem ter o banco de dados real e o software de SGBD distribuídos por vários locais*, conectados por uma rede de computadores
- *Os dados são, normalmente, replicados em vários locais*, de modo que a falha de um deles não tornará os dados indisponíveis
- Subdivide-se em mais *dois grupos*:
	- **SGBDD Homogêneo** - Usam o *mesmo software de SGBD* em todos os locais
	- **SGBDD Heterogêneo** - Podem usar *um software de SGBD diferente em cada local*
## Critério 4: [[Custo]]
- *Critério mais difícil de se propor uma classificação*
- Há muitos SGBDs de *código aberto*; outros com *versões gratuitas, porém limitadas*; e outros mais avançados, porém com *altos custos de licença*
## Critérios Adicionais
#### Tipos de Caminho de Acesso
#### Tipo de Uso (Geral/Especial)