## Data Science

Este arquivo é um arquivo norteador e de revisão do autor sobre seus estudos na pós-graduação de "Business intelligence, big data e analytics - ciência de dados", o intuito deste arquivo não é conteúdo técnico, mas sim de uma linguagem mais natural e de fácil acesso para facilitar o entendimento e revisar caso seja necessário em algum momento no futuro. como o arquivo é .md não terá revisão do textos, podendo então haver problemas de digitação e afins, caso esse material seja disponibilizado posteriormente para alguém, desconsiderar os erros de digitação.


### Fundamentos de Data Warehouse e Modelagem de dados

Antes de começar, necessário fazer uma recapitulação do que é um banco de dados, alguns populares atualmente (2026). Na decáda de 70, um engenheiro da IBM surge com uma solução para armazenamento de dados, assim nascendo o banco de dados relacional, orientado a tabelas, fortemente estruturado, possuindo índices, chaves primárias, chaves estrangeiras (foreign key) entidades e seus relacionamentos. Possuindo o conceito de ACID (Atomicidade, Consistência, Isolamento e disponiblidade). 

Em meados dos anos 2000, devido a uma necessidade de uma fragilidade do BD relacional, surge então o NoSQL. O banco de dados relacional possuia algumas certas limitações, quando fosse necessário mais capacidade de processamento, de armazenamento, era necessário a substituição completa do maquinário, era necessário montar um novo servidor com peças possuindo potência superiores. Devido a volumetria de dados, devindo ao 'Boom' de dados nos anos 2000 com web services, tais como: Google, Netflix, Redes Sociais e afins. Uma quantidade massiva de dados começaram a ser gerados e utilizados simultanêamentes, para essas problemáticas, o NoSQL vem solucionando. O que antes era necessário montar uma máquina totalmente nova para uma escalabilidade, o NoSQL vem com uma escalabilidade vertical, permitindo assim que ao invés de montar uma máquina nova para substituir a anterior, servidores possam rodar simultanêamente assim garantindo a capacidade de transferir mais dados simultanêamente, assegurando velocidade e confiábilidade.  

### OLTP versus OLAP


OLTP (Online transaction Process) é os bancos de dados que citamos acima, projetado para as atividades cotidianas, famosa escala 24/7. Segue uma estrutura, fortemente na escrita e na leitura. Tais como sistemas e-commerces, sistemas ERP. Focado no armazenamento das informações com as garantias necessárias das transações. Ex: Armazenamento para controle de estoque, RH com folha salarial, numero de funcionarios e afins.

OLAP (Online Analytic Process) - Projetado para responder perguntas complexas, focado na leitura de dados, então não seguindo uma "estrutura" conforme o OLTP, ele é voltado para grandes volumes de dados pensando em gerar relatórios, dashboards para perguntas complexas que gerem valor estratégico para a empresa. Ex: Na minha empresa eu possuo, varios clientes quem é meu maior comprador, quais os fatores que o levaram a comprar.

Ralph Kimball - Escreveu o livro ``The Data Warehouse Toolkit`` um dos principais livros que traz um conteúdo sobre Data Warehouse, um dos pilares para se entender bancos de dados análiticos. Todo conteúdo aprendido será retirado desse livro, exatamente a terceira versão dele.

Bill Inmon - Outro autor muito importante, ele traz uma outra maneira de se estruturar um banco de dados Warehouse.

Ambos autores trazem propostas que hoje são consolidadas em nosso meio, surgiram com essas propostas por volta da decada de 1996, antes mesmos do 'Boom' da internet web. Primeiro ponto a se entender, não há um método vencedor, ou seja, não um melhor que o outro, cada proposta resolve um tipo de problema, e entender suas caracteristicas é extremamente importante. Kimball defende que dados é um "ativo" da empresa, ou seja, um bem intángivel, ele define que um banco de dados Warehouse ele tem que possuir certos principios/metas. Sendo ela categorizadas em 7 metas. <br><br/>
1. (Simply and Fast) - O banco tem que ser simples e de fácil visualização
2. (Consistently) - Ele tem que apresentar informação consistente, ou seja ele tem que apresentar informação crível, limpos e padronizados
3. (Must adapt to change) - Flexibilidade para mudança, portanto tem que ser fácil para mudanças
4. (Timely) - Entregar as informações no tempo correto.
5. (Protect Information) - Proteger as informações da empresa.
6. (Serve as the authoritative and Trustworthy foundation for improved decision making) Servir como fonte confiável para tomada de decisões
7. (The business community must accept to deem it successful) Ser aceito e ativamente utilizado pelos colaboradores da empresa

## Metáfora do Jornal (Ralph Kimball) | Publishing Metaphor

Kimball, faz uma comparação de um gestor de DW/BI com um editor chefe de um jornal. Kimball elenca três tópicos essenciais para um manager de DW/BI sendo eles:

1. Entender o leitor.
2. Manter a alta qualidade.
3. Sustentar o négocio.

Com base nesses três tópicos podemos compreender certos aspectos assimilando as 7 metas com os três tópicos na metáfora. Compreender o leitor, é fundamental ao escrever um artigo (levando em consideração a comparação) entender o publico alvo, tem que ser um artigo voltado para o usuário, ou seja, ele tem que ser simples é fácil de se entender, ser uma fonte confiável, ser consistente, todas essas metas dentro da metafora podemos colocar como perguntas, uma delas sendo: "O que meu leitor quer ver?", "Quais dados ele precisa ver", "Está compreensível o conteúdo?", tudo isso voltado pela a melhor qualidade possível, pois uma vez que qualquer uma das metas não estejam sendo abordadas, impacta no terceiro tópico a sustentabilidade do négocio, ou seja o DW/BI quando pensamos nessa perspectiva, entendemos como o DW/BI deve ser estruturado, Kimball foi muito assertivo nessa comparação, pois uma vez que esses três tópicos falhem, não fará sentido o cliente (Business Manager) investir no jornal (Manager DW/BI).

## Introdução ao Modelo Dimensional

Existe dois requisitos que reforçam o motivo da ampla adoção do modelo do Kimball, Kimball entende e propõe a simplicidade, destaca a importância de ser fácil compreendimento, Kimball reforça a necessidade do sistema ser voltado a  leitura, tanto como para o leitor quanto para o programa.

1. Tem que ser de fácil compreeensão ao usuarios.
2. Tem que de rápida perfomance de busca.