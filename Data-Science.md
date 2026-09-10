## Data Science

Este arquivo é um arquivo norteador e de revisão do autor sobre seus estudos na pós-graduação de "Business intelligence, big data e analytics - ciência de dados", o intuito deste arquivo não é conteúdo técnico, mas sim de uma linguagem mais natural e de fácil acesso para facilitar o entendimento e revisar caso seja necessário em algum momento no futuro. como o arquivo é .md não terá revisão do textos, podendo então haver problemas de digitação e afins, caso esse material seja disponibilizado posteriormente para alguém, desconsiderar os erros de digitação.


### Fundamentos de Data Warehouse e Modelagem de dados

Antes de começar, necessário fazer uma recapitulação do que é um banco de dados, alguns populares atualmente (2026). Na decáda de 70, um engenheiro da IBM surge com uma solução para armazenamento de dados, assim nascendo o banco de dados relacional, orientado a tabelas, fortemente estruturado, possuindo índices, chaves primárias, chaves estrangeiras (foreign key) entidades e seus relacionamentos. Possuindo o conceito de ACID (Atomicidade, Consistência, Isolamento e disponiblidade). 

Em meados dos anos 2000, devido a uma necessidade de uma fragilidade do BD relacional, surge então o NoSQL. O banco de dados relacional possuia algumas certas limitações, quando fosse necessário mais capacidade de processamento, de armazenamento, era necessário a substituição completa do maquinário, era necessário montar um novo servidor com peças possuindo potência superiores. Devido a volumetria de dados, devindo ao 'Boom' de dados nos anos 2000 com web services, tais como: Google, Netflix, Redes Sociais e afins. Uma quantidade massiva de dados começaram a ser gerados e utilizados simultanêamentes, para essas problemáticas, o NoSQL vem solucionando. O que antes era necessário montar uma máquina totalmente nova para uma escalabilidade, o NoSQL vem com uma escalabilidade vertical, permitindo assim que ao invés de montar uma máquina nova para substituir a anterior, servidores possam rodar simultanêamente assim garantindo a capacidade de transferir mais dados simultanêamente, assegurando velocidade e confiábilidade.  

### OLTP versus OLAP


OLTP (Online transaction Process) é os bancos de dados que citamos acima, projetado para as atividades cotidianas, famosa escala 24/7. Segue uma estrutura, fortemente na escrita e na leitura. Tais como sistemas e-commerces, sistemas ERP. Focado no armazenamento das informações com as garantias necessárias das transações. Ex: Armazenamento para controle de estoque, RH com folha salarial, numero de funcionarios e afins.

OLAP (Online Analytic Process) - Projetado para responder perguntas complexas, focado na leitura de dados, então não seguindo uma "estrutura" conforme o OLTP, ele é voltado para grandes volumes de dados pensando em gerar relatórios, dashboards para perguntas complexas que gerem valor estratégico para a empresa. Ex: Na minha empresa eu possuo, varios clientes quem é meu maior comprador, quais os fatores que o levaram a comprar.

