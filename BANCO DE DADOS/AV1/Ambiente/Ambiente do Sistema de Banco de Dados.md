---
node_size: "5"
---
## [[Módulos Componentes do SGBD]]
- O _banco de dados_ e o _catálogo do SGBD_ normalmente são _armazenados em disco_
- O acesso ao disco é controlado, em especial, pelo **sistema operacional (SO)**, que **escalona a leitura/escrita em disco**
- Muitos SGBDs possuem o próprio **módulo de gerenciamento de buffer** para **planejar a leitura/escrita em disco**
- Um **módulo gerenciador de dados armazenados** de nível mais alto do SGBD controla o acesso às informações do SGBD armazenadas em disco, caso façam parte do banco de dados ou do catálogo
- O **compilador da DDL** é responsável por **processar as definições de esquema** e **armazenar os metadados no catálogo do SGBD**
- Usuários casuais e pessoas com necessidade ocasional de informações do banco interagem usando a **interface de consulta interativa**
- As consultas interativas são analisadas e validadas pela exatidão da sintaxe da consulta, que são _compiladas para um formato interno_ pelo **compilador de consulta**
- Entre outras coisas, o **otimizador de consulta** preocupa-se com o **rearranjo e possível reordenação de operações, a eliminação de redundâncias e o uso de algoritmos de busca eficientes durante a execução**
- O **pré-compilador** é responsável por **extrair comandos DML do programa de aplicação**, escrito em uma linguagem de programação hospedeira
	- Esses comandos são _enviados ao compilador DML para serem compilados em código objeto_ para acesso ao banco de dados
	- O restante do programa é enviado ao compilador da linguagem hospedeira
	- Os _códigos objeto_ para os comandos DML _e o restante do programa são ligados_ (linkados), formando uma _transação programada_ cujo código executável inclui _chamadas para o processador de banco de dados em tempo de execução_
- O **processador de banco de dados em tempo de execução** executa os _comandos privilegiados_, os _planos de consulta executáveis_ e as _transações programadas com parâmetros_ em tempo de execução
	- Ele trabalha com o _catálogo do sistema_ e pode atualizá-lo com estatísticas
	- Também trabalha com o *gerenciador de dados armazenados*, que utiliza os serviços básicos do sistema operacional para executar operações de entrada/saída de baixo nível entre o disco e a memória principal
- É comum que o **programa cliente** acesse o SGBD executando em um computador separado daquele em que o banco de dados reside
	- O primeiro é chamado *computador cliente*, que executa um software cliente do SGBD, e o segundo é chamado *servidor de banco de dados*
	- Em alguns casos, o cliente acessa um computador intermediário, conhecido como **servidor de aplicações** que, por sua vez, acessa o servidor
## [[Utilitários do Sistema]]
- Os utilitários são utilizados para **ajudar o DBA a gerenciar o sistema**
- Têm os seguintes tipos de funções:
#### Carga
- Um utilitário de carga é _usado para carregar os arquivos de dados existentes no banco_ de dados
- Normalmente, o formato atual do arquivo de dado e a estrutura do arquivo desejado são especificados pelo utilitário, que reformata automaticamente os dados e os armazenas no banco de dados
- Alguns fornecedores de SGBDs fornecem **ferramentas de conversão** que geram os programas de carga apropriados, tendo como base descrições de armazenamento de banco de dados de origem e destino
#### Backup
- Um utilitário de backup _cria uma cópia de segurança do banco de dados_, normalmente copiando-o inteiro para o meio de armazenamento desejado
- Os **backups incrementais** também costumam ser utilizados e _registram apenas as mudanças ocorridas após o backup anterior_
	- O backup incremental é mais complexo, mas economiza espaço de armazenamento
#### Reorganização do Armazenamento
- Pode ser usado para _reorganizar um conjunto de arquivos de banco de dados em diferentes organizações de arquivo_, criando novos caminhos de acesso para melhorar o desempenho
#### Monitoração de Desempenho
- Responsável por _monitorar o uso do banco de dados_ e _oferecer estatísticas ao DBA_
- O DBA usa tais estatísticas para decidir se deve ou não reorganizar arquivos ou se deve incluir ou remover índices para melhorar o desempenho
## [[Ferramentas, Ambientes de Aplicação e Facilidades de Comunicações]]
- Ferramentas *CASE* são usadas na fase de projeto dos sistemas de banco de dados
	- Servem para automatizar diversas etapas do ciclo de vida do desenvolvimento de software
- Um **sistema de dicionário de dados expandido** é responsável por, além de armazenar informações de catálogo sobre esquemas e restrições, armazenar decisões do projeto, padrões de uso, descrições da aplicação e informações do usuário
	- Também pode ser chamado de *repositório de informação*
	- Essa informação pode ser acessada diretamente pelos usuários ou pelo DBA
	- É semelhante ao catálogo do SGBD, mas inclui uma variedade maior de informações e é acessado principalmente pelos usuários
- **Ambientes de Desenvolvimento de Aplicação** oferecem um ambiente para desenvolver aplicações de banco de dados, 