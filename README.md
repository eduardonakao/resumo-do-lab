# resumo-do-lab
Este repositório contém o resumo das lições aprendidas durante o desenvolvimento do lab na DIO

- Benefícios da Nuvem Azure
Tem uma alta disponibilidade, ter recursos sempre disposiveis
Caso a disponibilidade do serviço não esteja acessivel durante um periodo de tempo maior do que o vigente no contrado o contratante é resarcido dentro da plataforma em forma de credito.

Escalabilidade poder ajustar a capacidade do nosso ambiente para atender melhor a demanda
Sempre pagar o que estar usando, sempre poder ajustar e pagar conforme o uso.

Elasticidade poder expandir seus recursos implantados rapidamente, podendo adicionar maquinas virtuais ou containeres por meio de expansão
Caso houver uma queda na demanda podemos reduzir os recursos implantados automaticamente ou manualmente.

Confiabilidade, devido a um design decentralizado a nuvem permite ter recursos implantados em várias regiões.
Previsibilidade e segurança.

Governança, podemos estabelecer regras e criar regras prontas para atender padroes de mercado ou até mesmo dentro da empresa.
Gerenciabilidade, facilitar o gerenciamento para nossos usuários, gerenciar os recursos da Nuvem, implantar recursos já pré-configurados, não necessitando fazer manual.

SLA quanto mais noves tiver menor sera o tempo de indisponibilidade

- Tipos de serviços de Nuvem
IaaS, PaaS e SaaS

IaaS (Infrastructure as a Service):
Provedor: Gerencia a infraestrutura física e virtual.
Cliente: Gerencia o sistema operacional, aplicativos, dados e configurações de segurança.
PaaS (Platform as a Service):
Provedor: Gerencia a infraestrutura e a plataforma.
Cliente: Foca no desenvolvimento e gerenciamento dos aplicativos e dados.
SaaS (Software as a Service):
Provedor: Gerencia tudo, desde a infraestrutura até o software.
Cliente: Gerencia apenas os dados e o acesso ao software.

Serviços de computação e MVs
podemos criar MVs para qualquer tipo de utilidade, desde uma MV para alguém que mora em um outro estado trabalhar ou para amarzenar um sistema

Conjuntos de Disponibilidade de MVs
O mais correto seria ter 3 Racks de dominio de falha com 2 VM dentro de cada rack para quando tivermos problemas de indisponibilidade em algum deles podermos usar o outro

Area de trabalho virtual e conteineres do Azure
funciona como uma virtualização de area de trabalho e aplicativo executada na nuvem
criar um ambiente completo de virtualização sem precisar executar outros servidores gateway
reduz o risco de que o recurso seja deixado para tras
Implantações reais de várias sessões

Serviços de contêineres é um serviço leve e virtualizado que não exige o gerenciamento do sistema o peracional e pode responder a alterações sob demanda

Azure functions e serviçoes de aplicativo
O que é: Azure Functions permite executar código em resposta a eventos sem a necessidade de gerenciar a infraestrutura do servidor1.
Como funciona: Você escreve funções que são acionadas por eventos, como mudanças em um banco de dados, mensagens em uma fila, ou até mesmo solicitações HTTP2.

Azure App Service é uma plataforma de hospedagem gerenciada para criar e implantar aplicativos web, back-ends móveis e APIs RESTful. Aqui estão os principais pontos:
O que é: Um serviço PaaS (Platform as a Service) que permite desenvolver e hospedar aplicativos em várias linguagens de programação, como .NET, Java, Node.js, PHP e Python

