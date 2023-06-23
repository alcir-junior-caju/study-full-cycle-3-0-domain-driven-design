# Curso Full Cycle 3.0 - Módulo Domain Driven Design

<div>
    <img alt="Criado por Alcir Junior [Caju]" src="https://img.shields.io/badge/criado%20por-Alcir Junior [Caju]-%23f08700">
    <img alt="License" src="https://img.shields.io/badge/license-MIT-%23f08700">
</div>

---

## Descrição

O Curso Full Cycle é uma formação completa para fazer com que pessoas desenvolvedoras sejam capazes de trabalhar em projetos expressivos sendo capazes de desenvolver aplicações de grande porte utilizando de boas práticas de desenvolvimento.

---

## Repositório Pai
https://github.com/alcir-junior-caju/study-full-cycle-3-0

---

## Visualizar o projeto na IDE:

Para quem quiser visualizar o projeto na IDE clique no teclado a tecla `ponto`, esse recurso do GitHub é bem bacana

---
### Domain Driven Design
- É uma forma de desenvolver software com o foco no coração da aplicação (o que chamamos de domínio), tendo o objetivo de enrender suas regras, processos e complexidades, separando-as assim de outros pontos complexos que normalmente são adicionados durante o processo de desenvolvimento.

#### De onde vem o DDD?
- Eric Evans;
- Livro lançado em 2003;
    - Filosofia;
    - Exemplos gerais;
    - Patterns;
- Comunidade de entusiastas seguindo essa prática;
- Lançamento de outros livros;

#### Softwares complexos
- DDD é / deve ser aplicado para casos de projetos de softwares complexos;
- Grandes projetos possuem muitas áreas, muitas regras de negócio, muitas pessoas com diferentes visões em diferentes contextos;
- Não há como não utilizar técnicas avançadas em projetos de alta complexidade;
- Grande parte da complexidade desse tipo de software não vem da tecnologia, mas sim da comunicação, separação de contextos, entedimento do negócio por diversos ângulos;
- Pessoas;

#### Como DDD pode ajudar
- Entender com profundidade o domínio e subdomínios da aplicação;
- Ter uma linguagem universal (linguagem ubíqua) entre todos os envolvidos;
- Criar o design estratégico utilizando Bounded Contexts;
- Criar o design tático para conseguir mapear e agregar as entidades e objetos de valor da aplicação, bem como os eventos de domínio;
- Clareza do que é complexidade de negócio e complexidade técnica;

#### Domínio x Subdomínios

DDD busca identificar e organizar os diferentes subdomínios dentro de um domínio maior, a fim de criar uma arquitetura que reflita as complexidades e interações do negócio.

No contexto do DDD, o domínio representa o problema a ser resolvido e toda a complexidade envolvida. Conforme o conhecimento do negócio aumenta, é possível identificar áreas específicas dentro desse domínio que podem ser separadas em subdomínios menores. Esses subdomínios são partes distintas do domínio maior e são chamados de subdomínios.

A importância do "Core Domain" (domínio principal), que é o núcleo do negócio e representa a parte essencial para a existência do sistema. É o diferencial competitivo da empresa e deve ser cuidadosamente projetado para oferecer valor único. Além do Core Domain, existem os subdomínios de suporte, que fornecem suporte ao domínio principal, auxiliando em suas operações diárias, mesmo não sendo o ponto central de diferenciação. Por exemplo, em um e-commerce, um centro de distribuição seria um subdomínio de suporte, pois é fundamental para o funcionamento do negócio, mas não é o aspecto que o torna único.

Também é mencionado o conceito de subdomínios genéricos, que são subdomínios que apoiam outros sistemas, mas geralmente não possuem um diferencial competitivo significativo para a empresa. Esses subdomínios podem ser substituídos por software de prateleira, pois não agregam um valor estratégico específico.

O DDD vai além do desenvolvimento de software e padrões de projeto, envolvendo a exploração e compreensão dos domínios e subdomínios do negócio. É importante compreender como esses diferentes elementos se relacionam e se encaixam no processo de desenvolvimento.

Em resumo, o DDD é uma abordagem de design de software que visa entender e organizar os diferentes subdomínios dentro de um domínio maior. O Core Domain representa o núcleo do negócio, os subdomínios de suporte fornecem suporte ao domínio principal, e os subdomínios genéricos são menos estratégicos para a empresa. O DDD envolve a exploração e modelagem desses domínios e subdomínios para criar uma arquitetura de software que reflita as complexidades do negócio.

#### Problema x Solução

No espaço do problema, temos uma visão geral do domínio e de suas complexidades. Ao analisar o problema, é possível identificar subdomínios e separar o domínio principal em partes menores. Esses subdomínios podem ser classificados como Core Domain (domínio principal), que é o aspecto mais importante e diferencial competitivo do negócio, e domínios de suporte, que ajudam a operação do Core Domain.

No espaço da solução, a ideia é modelar o domínio e encontrar soluções para os subdomínios delimitados anteriormente. A modelagem do domínio é destacada como um dos pilares do DDD. A importância de delimitar os contextos, ou seja, identificar subprodutos que precisam ser resolvidos e trabalhados. Cada contexto delimitado torna-se um problema específico a ser resolvido.

O DDD propõe abordar o problema, modelar o domínio, dividir o domínio em subdomínios e transformar esses subdomínios em contextos delimitados, com o objetivo de criar soluções para desenvolvimento. A partir dessa abordagem, é possível entender o que precisa ser feito e qual a prioridade de cada aspecto. Grande parte do trabalho em DDD ocorre dentro desses contextos delimitados.

#### Bounded Contexts

Um bounded context é uma divisão explícita dentro de um modelo de domínio. O termo "boundary" uma fronteira ou limite entre diferentes partes do domínio.

Embora a definição de bounded context seja genérica, uma das formas de delimitá-lo é através do uso de uma linguagem comum e específica dentro desse contexto. Isso é conhecido como "linguagem ubíqua" ou "linguagem universal", que se refere à terminologia e comunicação específicas utilizadas pelas pessoas envolvidas no domínio. A linguagem é um forte indicador do contexto delimitado em que se está trabalhando.

Em contextos muito pequenos e simples, como um sistema de padaria com poucas funcionalidades, a aplicação do DDD pode não fazer muito sentido, pois não há complexidade e todos falam a mesma linguagem geral. No entanto, em domínios maiores e mais complexos, como uma padaria industrial com diferentes departamentos e áreas de atuação, cada área pode ter seu próprio contexto delimitado com uma linguagem específica.

#### Contexto é rei

O contexto é crucial e determina em qual área da empresa estamos trabalhando e o tipo de problema que estamos resolvendo. A linguagem utilizada em cada contexto tem significados diferentes.

Um exemplo de dois contextos delimitados:

Venda de ingressos e suporte ao cliente, ambos envolvendo a entidade `ticket`. Embora as palavras sejam as mesmas, elas têm significados diferentes em cada contexto. No contexto da venda de ingressos, `ticket` refere-se aos ingressos vendidos, enquanto no contexto de suporte ao cliente, `ticket` representa solicitações de suporte. Essa diferença de significado indica que estamos lidando com contextos delimitados diferentes.

Em um sistema monolítico, onde tudo está integrado, se duas áreas usam a mesma palavra com significados diferentes, é necessário separar e modularizar o sistema para adaptá-lo aos diferentes contextos. Por exemplo, seria necessário criar entidades separadas para lidar com `ticket` na venda de ingressos e no suporte ao cliente.

É importante observar o oposto:

Quando duas palavras diferentes têm o mesmo significado, provavelmente estão em contextos diferentes. O exemplo da área de contabilidade do banco, que chama um relatório de `boletos pagos`, enquanto a área bancária na agência chama de `francesinhas`. Embora as palavras sejam diferentes, representam a mesma informação e indicam contextos distintos.

#### Elementos Transversais

A interseção entre diferentes contextos no Domain Driven Design (DDD) destaca a importância de entender as relações entre entidades e elementos transversais. Mesmo em contextos delimitados diferentes, algumas entidades se relacionam e compartilham o mesmo nome, mas com perspectivas diferentes.

O exemplo de um cliente, que está presente tanto no contexto de vendas de ingressos quanto no contexto de suporte ao cliente.

No contexto de vendas de ingressos, o foco está no evento, no ticket do cliente, no local da compra e no vendedor.

Já no contexto de suporte ao cliente, o foco está nos tickets de dúvidas, nos departamentos responsáveis e nos atendentes. Embora o cliente seja o mesmo, as perspectivas e os requisitos são diferentes.

Os desenvolvedores muitas vezes tendem a modelar todas as perspectivas de um cliente em uma única classe, o que resulta em uma entidade complexa e abrangente. No entanto, quando existem contextos diferentes, é importante modelar o cliente de acordo com cada contexto específico. Caso contrário, a aplicação se tornará difícil de gerenciar e, no futuro, será necessário reescrever tudo ao tentar dividir em microsserviços ou outras arquiteturas.

A delimitação e o entendimento dos contextos são essenciais para desenvolver um sistema de forma mais eficiente.

#### Visão estratégica (Context Mapping)

A importância da modelagem estratégica e do context mapping no desenvolvimento de software. Ao realizar a modelagem, é necessário ter uma visão geral de como as diferentes partes se encaixam. A separação e delimitação dos contextos são realizadas no espaço do problema, onde se procura entender o domínio de forma geral.

No entanto, durante o trabalho com esses contextos, eles inevitavelmente irão se comunicar e se complementar. Nesse ponto, é necessário adotar uma abordagem mais estratégica para ter uma visão ampla de como as coisas vão interagir e como organizar as equipes durante o processo de modelagem e desenvolvimento.

Para isso, é proposto o uso do context mapping, que consiste essencialmente em mapear os contextos. Essa técnica permite entender os relacionamentos entre os contextos, como as coisas funcionam e facilita a organização das equipes. O context mapping proporciona uma visão de cima, mais estratégica, para compreender como os diferentes contextos se conectam e colaboram entre si.

Portanto, o context mapping é apresentado como uma ferramenta importante na modelagem estratégica, permitindo uma compreensão mais clara dos relacionamentos e comunicações entre os diferentes contextos envolvidos no desenvolvimento de software.

#### Modelagem estratégica / Context Mapping

A modelagem estratégica e o mapeamento de contextos em um projeto de desenvolvimento de software. A importância de compreender como diferentes contextos se relacionam entre si e como podem ser organizados em equipes específicas.

Exemplo uma empresa que vende ingressos online e offline, com uma área de suporte ao cliente e parcerias com shoppings e casas noturnas.

A parceria é destacada como uma relação em que dois times trabalham em conjunto para alcançar objetivos comuns, como a venda de ingressos online e offline.

O shared kernel (núcleo compartilhado) é uma forma de compartilhar recursos ou componentes entre diferentes sistemas, podendo gerar dependências e impactos. A relação de cliente-fornecedor é abordada quando um contexto depende de serviços ou informações fornecidos por outro, como a área de vendas de ingressos que depende da área de pagamento.

Exemplos de relações de upstream (fornecedor) e downstream (cliente) entre contextos, onde o contexto upstream dita as regras e o contexto downstream se adapta para consumir os serviços. A possibilidade de um contexto atuar como fornecedor de informações para outro contexto, estabelecendo uma relação de suporte ao cliente.

Uma parte precisa se adaptar às especificações e requisitos definidos pela outra parte, como a integração com uma gateway de pagamento externa. Nesses casos, é recomendado utilizar camadas de interface, como a camada anticorrupção (ACL), para minimizar a dependência e facilitar possíveis trocas de fornecedores.

A importância do context mapping para obter uma visão estratégica, entender as interações e relacionamentos entre os contextos, e organizar as equipes de desenvolvimento de forma adequada.

#### Padrões de Context Mapping
- Partnership;
- Shared Kernel;
- Customer-Supplier Development;
- Conformist;
- Anticorruption-layer (ACL);
- Open host service;
- Published language;
- Separated ways;
- Big Ball of Mud;

Projeto: https://github.com/ddd-crew/context-mapping
