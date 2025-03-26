---
node_size: "5"
---
- No **processamento de arquivos tradicional**, *cada usuário define e implementa os arquivos necessários* para uma aplicação de software específica como parte da programação da aplicação
- Na **abordagem de banco de dados**, *um único repositório mantém dados que são definidos uma vez* e, posteriormente, acessados por vários usuários repetidamente por meio de consultas, transações e programas de aplicação
## [[Natureza de Autodescrição]]
- O *sistema contém não apenas o próprio banco de dados*, mas também uma *definição ou descrição completa de sua estrutura e restrições*
- Essa definição é *armazenada no catálogo do SGBD*, que contém informações como a *estrutura de cada arquivo, o tipo e o formato de armazenamento de cada item e restrições* sobre os dados
- A *informação armazenada no catálogo* é chamada de **metadados**, e *descreve a estrutura do banco de dados principal*
- No **processamento de arquivos tradicional**, a *definição de dados normalmente faz parte dos próprios programas* de aplicação
- O **catálogo é usado pelo SGBD e também pelos usuários** do banco de dados que precisam de informações sobre a estrutura do banco de dados
- Um *pacote de software de SGBD de uso geral não é escrito para uma aplicação* de banco de dados *específica*
- O **software de SGBD precisa trabalhar de forma satisfatória com qualquer quantidade de aplicações** de banco de dados
## [[Isolamento entre Programas e Dados]]
- A *estrutura dos arquivos de dados é armazenada no catálogo do SGBD separadamente dos programas* de acesso
- Essa propriedade é chamada de **independência de dados do programa**
- Uma **operação** (também chamada de função ou método) é **especificada em duas partes**:
	- **Interface/Assinatura** - Inclui o *nome da operação e os tipos de dados de seus argumentos* (ou parâmetros)
	- **Implementação/Método** - *Especificada separadamente*, podendo ser alterada sem afetar a interface
- Os **programas de aplicação** do usuário *podem operar sobre os dados usando operações por meio de seus nomes e argumentos*, independentemente de como elas são implementadas (**independência de operação do programa**)
- A característica que permite a independência de dados do programa é chamada de **[[Características da Abordagem de Banco de Dados#Abstração de Dados|abstração de dados]]**
#### [[Abstração de Dados]]
- **Representação conceitual de dados**
- *Não inclui muitos dos detalhes* de implementação/armazenamento dos dados
- Um **modelo de dados** é um *tipo de abstração usado para oferecer essa representação conceitual*
- *Usa conceitos lógicos que os usuários podem compreender mais rapidamente* que os conceitos de armazenamento no computador
- A **estrutura e organização detalhadas** de cada arquivo **são armazenadas no catálogo**
- Em **bancos de dados orientados a objeto e objeto-relacional**, o processo de abstração *não inclui apenas a estrutura dos dados, mas também as operações* sobre eles
## [[Suporte para Múltiplas Visões]]
- Uma ***visão*** (ou view) pode ser um **subconjunto do banco de dados que pode (ou não) conter dados virtuais derivados dos arquivos**
- Um **SGBD multiusuário** cujos usuários têm uma série de aplicações distintas **precisa oferecer facilidades para definir múltiplas visões**
## [[Compartilhamento de Dados]]
- Um **SGBD multiusuário** precisa incluir **software de controle de ocorrência**, a fim de *garantir que vários usuários tentando atualizar os mesmos dados façam isso de maneira controlada*, de modo que o resultado das atualizações seja correto
## [[Processamento de Transação Multiusuário]]
- Uma **transação** é um **programa em execução ou processo que inclui um ou mais acessos ao banco** de dados, como a leitura ou atualização dos registros
- *Cada transação deve executar um acesso ao banco* de dados, sendo *logicamente correta para ser executada em sua totalidade*, sem interferência de outras transações
- Possui as seguintes propriedades:
	- **Isolamento** - Garante que *cada transação pareça executar isoladamente das outras transações*, embora várias possam estar acontecendo simultaneamente
	- **Atomicidade** - Garante que *todas as operações em uma transação sejam executadas ou nenhum seja*