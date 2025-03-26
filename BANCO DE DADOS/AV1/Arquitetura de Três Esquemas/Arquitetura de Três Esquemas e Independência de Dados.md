---
node_size: "5"
---
## [[Arquitetura de Três Esquemas]]
- Possui como objetivo *separar as aplicações do usuário* no banco de dados
- É uma *ferramenta conveniente com a qual o usuário pode visualizar os níveis de esquema* de um sistema de banco de dados
- A _arquitetura ANSI de três níveis_ tem um lugar importante no desenvolvimento da tecnologia de banco de dados, pois separa claramente os três níveis (interno, conceitual e externo) no projeto de um banco de dados
- Divide-se em **três níveis**:
	**Nível Interno**
	- **Descreve a estrutura do armazenamento físico** do banco de dados
	- Usa um **modelo de dados físico** e *descreve os detalhes completos do armazenamento dos dados*, bem como os caminhos de acesso ao banco
	**Nível Conceitual**
	- **Descreve a estrutura do banco de dados inteiro** para uma comunidade de usuários
	- *Oculta os detalhes de armazenamento* físico e *se concentra na descrição de entidades, tipos de dados, relacionamentos, operações e restrições*
	- O *esquema conceitual de implementação costuma estar baseado em um projeto de esquema conceitual* em um modelo de dados de alto nível
	**Nível externo**
	- Também chamado de **nível de visão**, *inclui uma série de esquemas externos* ou **visões do usuário**
	- *Cada esquema externo descreve a parte do banco de dados em que um grupo de usuários em particular está interessado* e oculta o restante do banco
- Na maioria dos SGBDs que têm suporte a múltiplas visões do usuário, os _esquemas externos são especificados no mesmo modelo de dados que descreve a informação no nível conceitual_
- *Os três esquemas são apenas descrições dos dados*, e *os dados armazenados* que realmente *existem estão apenas no nível físico*
- Cada grupo de usuários recorre ao seu próprio esquema externo, e assim o SGBD precisa _transformar uma solicitação especificada em um esquema externo_ em uma _solicitação no esquema conceitual_ e depois em uma _solicitação no esquema interno_ para processamento no banco
- Os *processos de transformação de requisições e os resultados entre os níveis* são chamados de **mapeamentos**
- Esses mapeamentos *podem ser demorados a ponto de alguns SGBDs* (especialmente os que têm como foco pequenos bancos de dados) *não oferecerem suporte a visões externas*
## [[Independência de Dados]]
- Pode ser definida como *a capacidade de alterar o esquema em um nível do sistema de banco de dados sem ter de alterar o esquema no próximo nível mais alto*
- Pode-se definir **dois tipos** de independência de dados:
#### Independência Lógica
- **Capacidade de alterar o esquema conceitual sem alterar os esquemas externos** ou programas de aplicação
- Pode ser usado para *expandir o banco de dados, alterar suas restrições ou reduzi-lo*
- *Em caso de redução* do banco, *esquemas externos que se referem apenas aos dados restantes não seriam afetados*
- *Somente a definição da visão e os mapeamentos precisam ser alterados* em um SGBD que suporta este tipo de independência
- As *mudanças nas restrições podem ser aplicadas ao esquema conceitual sem afetar os esquemas externos* ou programas de aplicação
#### Independência Física
- Capacidade de **alterar o esquema interno sem ter de alterar o esquema conceitual**
- *Mudanças no esquema interno podem ser necessárias*, dado que alguns arquivos físicos foram reorganizados, *para melhorar o desempenho da recuperação ou atualização dos dados*
	- Se os mesmos dados permanecem no banco de dados, pode não ser necessária a alteração do esquema conceitual
- Em geral, este tipo de independência _existe na maioria dos bancos de dados e ambientes de arquivo_, onde os detalhes físicos e detalhes de hardware são ocultados do usuário
- Por sua vez, a _independência lógica é mais difícil de ser alcançada_, dado que **permite alterações estruturais e de restrição sem afetar os programas de aplicação**
- Sempre que se tem um _SGBD de múltiplos níveis_, seu _catálogo deve ser expandido_ para _incluir informações sobre como mapear solicitações e dados entre os níveis_