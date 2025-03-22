---
node_size: "5"
---
## Modelo de Dados
- Coleção de conceitos que podem ser usados para descrever a estrutura de um banco de dados
- Com *estrutura de banco de dados*, fala-se sobre os tipos, relacionamentos e restrições que se aplicam aos dados
- Oferece os meios necessários para alcançar a [[Características da Abordagem de Banco de Dados#Abstração de Dados|abstração de dados]]
- A maioria dos modelos de dados também inclui um conjunto de **operações básicas** para especificar recuperações e atualizações no banco de dados
- Além das operações básicas, modelos mais atuais incluem também conceitos no modelo de dados para especificar o *aspecto dinâmico* ou *comportamento* de uma aplicação no banco de dados
	- Isso permite ao projetista especificar um conjunto de operações válidas, definidas pelo usuário, sobre os objetos do banco de dados
	- Por sua vez, operações genéricas de inserção, exclusão, modificação ou recuperação de qualquer tipo de objeto normalmente estão incluídas nas operações básicas
- No modelo de dados _relacional básico_, existe um recurso para conectar um comportamento às relações na forma de **módulos de armazenamento persistente**, conhecidos como **procedimentos armazenados (storage procedures)**
## [[Categorias de Modelos de Dados]]
### Modelos Conceituais
- Usam conceitos como *entidades*, *atributos* e *relacionamentos*
	- **Entidades** - Representa um objeto ou conceito do mundo real
	- **Atributo** - Representa alguma propriedade de interesse que descreve melhor uma entidade
	- **Relacionamento** - Representa uma associação entre duas ou mais entidades
- Dividem-se entre três principais modelos:
#### Modelos de Alto Nível
- Oferecem conceitos próximos ao modo como muitos usuários percebem os dados
#### Modelos de Baixo Nível
- Oferecem conceitos que descrevem os detalhes de como os dados são armazenados no computador
#### Modelos Representativos
- Localizados entre o alto e o baixo nível
- Ocultam muitos detalhes do armazenamento dos dados em disco, mas podem ser implementados diretamente em um sistema digital
- Oferecem conceitos que podem ser facilmente entendidos pelos usuários finais, mas também próximos ao modo como os dados são organizados e armazenados no computador
### Modelos Representativos
- Usados com mais frequência nos SGBDs comerciais tradicionais
- Mostram os dados usando estruturas de registro, sendo comumente chamados de modelos de dados baseados em registro
#### Modelos Relacionais
- Modelo baseado em tabelas onde os dados são armazenados em *linhas* e *colunas*
- Usa chaves primárias e estrangeiras para garantir a integridade e relacionar os dados entre diferentes tabelas
#### Modelos de Dados de Objeto
- Nova família de modelos de dados de implementação de nível mais alto, mais próximos dos modelos de dados conceituais
- Frequentemente utilizados como modelos conceituais de alto nível, em particular no domínio da engenharia de software
#### Modelos Autodescritivos
- O armazenamento de dados nos sistemas baseados nesses modelos combina a descrição dos dados com seus próprios valores
- Incluem _XML_, além de muitos _armazenamentos de chave-valor_ e _sistemas NOSQL_
### Modelos Legados
#### Modelos de Rede
- 
#### Modelos Hierárquicos
- 