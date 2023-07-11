# Intensivão Java Spring

## Aula 1 - (10/07/2023)

![image](https://github.com/pabloo-cunha/dslist-devsuperior/assets/111435624/acd8a585-07fc-4416-9f53-2dc0696feb7f)

A primeira aula foi repleta de aprendizados e eu vou tentar deixar explicado abaixo, cada um dos topicos que estão na revisão.

### Sistema Web e Recursos

![image](https://github.com/pabloo-cunha/dslist-devsuperior/assets/111435624/4aa64f3f-a3bf-4c99-92b9-6745959d7c95)

#### Front-End
O front-end é a parte visual do sistema web. É responsável por exibir o conteúdo para os usuários e permitir que eles interajam com o sistema. O navegador é a ferramenta utilizada para visualizar imagens, campos, botões e realizar as interações com o sistema.

#### Back-End
O back-end é a parte responsável pelo processamento das requisições vindas do front-end. É onde as requisições são processadas e as respostas são geradas. Ele executa a lógica de negócio, manipula os dados e retorna as respostas para o front-end. O back-end recebe as requisições HTTP enviadas pelo navegador, realiza operações no banco de dados e envia as respostas adequadas de volta ao front-end.

#### Padrão Rest para API Web
O padrão REST é um conjunto de requisitos que utilizamos no Spring para mapear nosso sistema. Seguindo esse padrão, usamos as seguintes requisições HTTP:

- GET: Utilizado para receber dados do servidor. É usado quando desejamos obter informações existentes no sistema.
- PUT: Utilizado para adicionar dados ao servidor. É usado quando queremos inserir novas informações no sistema.
- POST: Utilizado para atualizar dados no servidor. É usado quando desejamos modificar informações já existentes no sistema.
- DELETE: Utilizado para remover dados do servidor. É usado quando queremos excluir informações do sistema.

No Spring, podemos utilizar essas requisições HTTP para criar uma API RESTful, que permite a comunicação entre o cliente e o servidor de forma padronizada e sem estado. Isso facilita o desenvolvimento de aplicações web e o acesso aos recursos do sistema de forma clara e consistente.

#### ORM (Object-Relational Mapping)
O ORM é um conceito utilizado no desenvolvimento de software para facilitar a integração entre banco de dados relacionais e sistemas orientados a objetos.

Basicamente, o ORM permite persistir dados em um banco de dados relacional sem a necessidade de escrever consultas SQL manualmente. Em vez disso, você pode usar anotações ou configurações para mapear as entidades do seu sistema para as tabelas do banco de dados.

Um framework muito utilizado para Java é o Spring JPA. Ele fornece um conjunto de anotações e métodos para realizar a persistência de dados, além de recursos para consultas e operações diversas.

Com o uso do ORM, é possível abstrair a complexidade do mapeamento objeto-relacional e trabalhar com objetos e suas relações de forma mais natural no código. Isso torna o desenvolvimento mais produtivo e menos suscetível a erros.

O Spring JPA é apenas um exemplo de framework ORM para Java, existem outras opções disponíveis, como o Hibernate, EclipseLink, entre outros.

#### Database seeding
O database seeding é um processo de preenchimento inicial do banco de dados com dados de teste ou dados padrão. É uma prática comum em desenvolvimento de software para garantir que o banco de dados tenha registros iniciais necessários para o funcionamento correto do sistema.

O seeding geralmente é realizado durante a fase de inicialização do aplicativo, onde um script ou código é executado para inserir dados no banco de dados. Esses dados podem incluir informações básicas, como usuários padrão, configurações iniciais, registros de referência, dados de amostra, entre outros.

No caso desse projeto, o seeding foi todo configurado no application-test.properties, utilizando para isso o banco de teste H2.

#### Padrão de Camadas 

![image](https://github.com/pabloo-cunha/dslist-devsuperior/assets/111435624/0b4d409f-3ad6-4c28-866a-fa4d2b600121)

O padrão de camadas é um padrão arquitetural comumente utilizado no desenvolvimento de software para separar e organizar as diferentes responsabilidades de um sistema em camadas distintas. Cada camada possui uma função específica e se comunica com as camadas adjacentes seguindo uma hierarquia bem definida.

O objetivo principal do padrão de camadas é promover a separação de preocupações, modularidade, reutilização de código e facilidade de manutenção do sistema. Além disso, ele também ajuda a melhorar a escalabilidade, permitindo que cada camada seja escalonada de forma independente, conforme necessário.

Nesse projeto as reponsabilidade estão sendo dividas conforme a imagem acima: Services, Controllers e Repository.<br>
A camada de dados(repository) se comunica com os Serviços(services) que por sua vez é utilizado pelo Controller para fazer as requisições HTTP.

#### Padrão DTO
O padrão DTO (Data Transfer Object) é um padrão de projeto usado para transferir dados entre diferentes componentes de um sistema, geralmente entre a camada de apresentação (ou camada de interface do usuário) e a camada de aplicação (ou camada de negócio). O objetivo do padrão DTO é encapsular dados e fornecer uma estrutura simplificada para o transporte de informações.

O padrão DTO é útil em cenários em que é necessário transferir dados entre diferentes camadas ou componentes do sistema, mas as classes de domínio (entidades) não são adequadas para esse propósito, seja porque contêm mais informações do que o necessário ou porque não possuem os formatos desejados para a transferência de dados.

Nesse projeto a classe "Game" possuia muitas informações que não eram necessariass de forma imediata para quem a via. Então foi o utilizado o padrão DTO para formatar esses dados e organiza-los de forma que fosse apresentado apenas dados primarios para quem estava vendo ao invés dos dados completos.
