---
node_size: "5"
---
## [[Arquitetura Centralizada]]
- As *arquiteturas mais antigas usavam computadores mainframe para oferecer o processamento principal* para todas as funções do sistema
- A *maioria dos usuários acessava tais sistemas por **terminais de computador***, que não tinham capacidade de processamento e *serviam apenas para exibição*
- *Todo o processamento era realizado de forma remota no computador central, que continha o SGBD*, e somente informações de exibição e controle eram enviadas do computador para os terminais
- *Com a substituição dos terminais por PCs* (bem como estações de trabalho e dispositivos móveis), *os sistemas de banco de dados, a princípio, usavam esses computadores de modo semelhante aos terminais*
- *Gradualmente, os sistemas de SGBD começaram a explorar o poder de processamento disponível no lado do usuário*, levando a arquiteturas cliente/servidor
## [[Arquiteturas Cliente e Servidor Básicas]]
- Arquitetura *desenvolvida para lidar com ambientes de computação em que um grande número de PCs e outros softwares e equipamentos são conectados por uma rede*
- A ideia é definir **servidores especializados com funcionalidades específicas**
- Os _recursos_ fornecidos pelos servidores especializados _podem ser acessados por **máquinas clientes**_
- As **máquinas clientes** *oferecem ao usuário as interfaces apropriadas para utilizar esses servidores, bem como poder de processamento local* para executar aplicações locais
- O conceito de arquitetura cliente/servidor assume uma *estrutura básica* composta por *muitas máquinas clientes* e um *número menor de máquinas servidoras*, conectadas por redes de computadores
- Um **cliente**, nesta estrutura, normalmente é uma *máquina que oferece capacidades de interface com o usuário e processamento local*
- Um **servidor** é um *sistema com hardware e software que pode oferecer serviços às máquinas clientes*
- Em geral, algumas máquinas têm instalados *apenas software cliente*, outras *apenas possuem software servidor*, e ainda outras podem incluir *ambos software cliente e servidor*
- É *mais comum* que o software cliente e servidor seja executado em *máquinas separadas*
- A partir desta arquitetura básica, foram criadas outras duas arquiteturas: de **duas camadas** e **três camadas**
## [[Arquiteturas de Duas Camadas]]
- *Em SGBD relacionais (SGBDRs), os componentes do sistema movidos inicialmente para o lado do cliente foram a interface com o usuário e os programas* de aplicação
- As *funcionalidades de consulta e de transação relacionadas ao processamento da SQL permaneceram do lado do servidor*
- Nesse tipo de arquitetura, *o servidor é comumente chamado de* **servidor de consulta** ou **servidor de transação** (em SGBDR, também é chamado de **servidor SQL**)
- Os *programas da interface com o usuário e programas de aplicação podem ser executados no lado do cliente*
- Quando é necessário acessar o SGBD, o programa estabelece uma conexão com o SGBD e, após criada a conexão, o programa cliente pode se comunicar com o SGBD
- Um padrão denominado **Conectividade de Banco de Dados Aberta (OBDC)** oferece uma **interface de programação de aplicações (API)** que *permite que os programas do cliente chamem o SGBD, desde que ambas as máquinas tenham o software necessário instalado*
- *Um programa cliente pode se conectar a vários SGBDRs e enviar solicitações de consulta e transação usando a API da ODBC*, que é processada nos servidores
- Essas arquiteturas são chamadas de **arquiteturas de duas camadas** porque *os componentes de software são distribuídos entre os sistemas cliente e servidor*
- As **vantagens** dessa arquitetura são sua *simplicidade e compatibilidade transparente com os sistemas existentes*
- Esta arquitetura possui como **desvantagens** sua *escalabilidade limitada e segurança reduzida*
## [[Arquiteturas de Três Camadas e n Camadas para Aplicações Web]]
- Muitas aplicações web utilizam uma arquitetura chamada **arquitetura de três camadas**, que *acrescenta uma camada intermediária entre o cliente e o servidor*
- Essa camada intermediária é chamada de **servidor de aplicação**, que *desempenha um papel intermediário pela execução de programas de aplicação e armazenamento de regras de negócios* usados para acessar os dados do servidor de banco de dados
- Em partes, é ***responsável por melhorar a segurança do banco de dados**, verificando as credenciais de um cliente antes de encaminhar uma solicitação* ao servidor
- *O servidor intermediário aceita e processa solicitações do cliente, envia consultas e comandos do banco de dados ao servidor e, por fim, atua como um canal para passar (parcialmente) dados processados do servidor aos clientes*, onde podem ser processados e filtrados antes de serem apresentados
- Resumindo as funções de cada camada:
	- A **camada de apresentação/esquema externo** *exibe informações ao usuário e permite a entrada de dados*
	- A **camada de lógica de negócios/esquema conceitual** *cuida das regras e restrições intermediárias antes dos dados serem passados para o usuário ou devolvidos ao SGBD*
		- Também *pode atuar como um servidor web*, que recupera resultados das consultas do servidor de banco de dados e os formata para páginas web dinâmicas
	- A **camada inferior/esquema interno** *inclui todos os serviços de gerenciamento de dados*
- Outras arquiteturas foram propostas, em especial a de *subdivisão das 3 camadas em outros componentes ainda mais detalhados*, o que resulta em uma **arquitetura de n camadas**
	- *Geralmente, a camada da lógica de negócios é dividida em várias camadas* para obter este tipo de arquitetura
- Os *fabricantes de pacotes de **ERP** e **CRM*** costumam utilizar uma *camada mediadora*, que é responsável pelos módulos de front-end que se comunicam com uma série de bancos de dados de back-end