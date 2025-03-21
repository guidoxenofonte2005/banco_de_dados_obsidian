---
node_size: "5"
---
## [[Banco de Dados]]
- Coleção de dados relacionados
	- Dados - Fatos conhecidos que podem ser registrados e que possuem significado implícito
- Possui as seguintes propriedades implícitas:
	- Representa algum aspecto do mundo real
	- É uma coleção logicamente coerente de dados com algum significado inerente
	- É projetado, montado e preenchido com dados com algum significado coerente
- Pode ter qualquer tamanho e complexidade
- Pode ser gerado e mantido manualmente ou de forma computadorizada
- Um banco de dados computadorizado pode ser criado e mantido por um grupo de programas de aplicação, especificamente escritos para esta tarefa, ou por um [[Definições Básicas#Sistema de Gerenciamento de Banco de Dados (SGDB)|sistema de gerenciamento de banco de dados]]
## [[Sistema de Gerenciamento de Banco de Dados (SGDB)]]
- Sistema de software de uso geral que facilita o processo de [[Definições Básicas#Definição|definição]], [[Definições Básicas#Construção|construção]], [[Definições Básicas#Manipulação|manipulação]] e [[Definições Básicas#Compartilhamento|compartilhamento]] de bancos de dados entre diversos usuários e aplicações
- Um **programa de aplicação** acessa o banco de dados enviando consultas ou solicitações ao SGBD
	- Consulta - Faz com que alguns dados sejam recuperados
	- Transação - Pode fazer com que alguns dados sejam lidos e alguns sejam gravados no banco de dados
- Outras funções importantes fornecidas pelo SGBD incluem:
	- Proteção do banco de dados - Inclui proteção do sistema contra falhas de hardware ou software e proteção de segurança contra acesso não autorizado/malicioso
	- Manutenção do banco de dados
- A união do banco de dados com o software de SGBD é chamada de **sistema de banco de dados**
#### Definição
- Envolve especificar os tipos de dados, as estruturas e restrições dos dados a serem armazenados
- A definição/informação descritiva do banco de dados é armazenada pelo SGBD na forma de um *catálogo* ou dicionário, chamado de **metadados**
#### Construção
- Processo de armazenar os dados em algum meio de armazenamento controlado pelo SGBD
#### Manipulação
- Inclui funções como consulta, atualização e geração de relatórios a partir dos dados
#### Compartilhamento
- Permite que vários usuários e programas acessem o banco de dados simultaneamente