---
node_size: "5"
---
## [[Atores em Cena]]
#### Administradores do Banco de Dados
- Responsável por administrar os recursos do banco, autorizar o acesso, coordenar e monitorar seu uso e adquirir recursos de software e hardware conforme a necessidade
- Responsável por problemas como falhas de segurança e latência
#### Projetistas de Banco de Dados
- Responsáveis por identificar os dados a serem armazenados e escolher estruturas apropriadas para representar e armazenar esses dados
- É responsabilidade dos projetistas se comunicarem com todos os usuários do banco de dados em potencial a fim de entender seus requisitos e criar um projeto que os atenda
- Normalmente interagem com cada grupo em potencial e desenvolvem **visões** do banco de dados que cumprem os requisitos
#### Usuários Finais
- Pessoas cujas funções exigem acesso ao banco de dados para consulta, atualização e geração de relatórios
- O banco de dados existe principalmente para seu uso
- Existem várias categorias:
	- Casuais - Ocasionalmente acessam o banco, mas podem precisar de diferentes informações a cada vez
	- Iniciantes/Paramétricos - Compõem uma grande parte dos usuários finais, cuja principal função gira em torno de consultar e atualizar o banco de dados constantemente, usando tipos padrão de consultas e atualizações (**transações programadas**)
	- Sofisticados - Incluem profissionais que estão profundamente familiarizados com as facilidades do SGBD a fim de implementar suas próprias aplicações
	- Isolados - Mantêm bancos de dados pessoais usando pacotes de programas prontos, que oferecem interfaces de fácil visualização
#### Analistas de Sistemas e Programadores de Aplicações
- Analistas de sistemas determinam os requisitos dos usuários finais, especialmente os usuários comuns e paramétricos, e desenvolvem especificações para transações programadas que cumpram esses requisitos
- Programadores de aplicações implementam essas especificações como programas, seguidos de testes, depuração, documentação e manutenção das transações programadas
- Ambos devem estar familiarizados com toda a gama de capacidades fornecidas pelo SGBD
## [[Bastidores]]
#### Projetistas e Implementadores de SGBD
- Projetam e implementam os módulos e interfaces do SGBD como um pacote de software
#### Desenvolvedores de Ferramentas
- Projetam e implementam **ferramentas** - pacotes opcionais que, em geral, são adquiridos separadamente
- Incluem pacotes para projeto de banco de dados, monitoramento de desempenho, linguagem natural, protótipo, simulação e geração de dados de teste
#### Operadores e Manutenção
- Responsáveis pela execução e manutenção real do ambiente de hardware e software para o sistema