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

Armazenamento
Redundância no Azure Storage
A redundância no Azure Storage garante que seus dados estejam sempre disponíveis e protegidos contra falhas. Existem várias opções de redundância:

LRS (Locally Redundant Storage):
O que é: Replica seus dados três vezes dentro de uma única região.
Uso: Ideal para proteção contra falhas de hardware local1.
ZRS (Zone-Redundant Storage):
O que é: Replica seus dados em três zonas diferentes dentro de uma mesma região.
Uso: Protege contra falhas de zona, oferecendo maior resiliência2.
GRS (Geo-Redundant Storage):
O que é: Replica seus dados em uma região secundária, localizada a centenas de quilômetros da região primária.
Uso: Oferece proteção contra falhas regionais, garantindo alta durabilidade3.
RA-GRS (Read-Access Geo-Redundant Storage):
O que é: Similar ao GRS, mas permite acesso de leitura aos dados na região secundária.
Uso: Ideal para cenários onde a leitura dos dados deve continuar mesmo em caso de falha na região primária

Serviços de Armazenamento da Azure
Blob Storage:
O que é: Armazenamento de objetos para grandes quantidades de dados não estruturados, como imagens, vídeos e backups.
Uso: Ideal para streaming de mídia, armazenamento de dados de backup e arquivamento.
File Storage:
O que é: Armazenamento de arquivos compartilhados acessíveis via SMB (Server Message Block).
Uso: Perfeito para migração de aplicativos legados e compartilhamento de arquivos entre várias máquinas.
Queue Storage:
O que é: Armazenamento de mensagens para comunicação entre componentes de aplicativos distribuídos.
Uso: Útil para gerenciamento de tarefas e processamento assíncrono.
Table Storage:
O que é: Armazenamento de dados estruturados em um formato de tabela NoSQL.
Uso: Ideal para armazenar grandes volumes de dados estruturados que não exigem relacionamentos complexos.

Pontos de Extremidade Públicos
O que são: Pontos de extremidade públicos são endereços IP públicos que permitem o acesso a recursos do Azure a partir de qualquer lugar do mundo.
Uso: Utilizados para acessar serviços como Azure Storage, Azure SQL Database e outros serviços que precisam ser acessíveis pela internet.
Segurança: É importante configurar regras de firewall e políticas de acesso para proteger esses pontos de extremidade contra acessos não autorizados.

Camadas de Acesso
O que são: Camadas de acesso definem os níveis de controle e segurança aplicados aos dados armazenados no Azure.
Tipos:
Camada de Rede: Inclui pontos de extremidade de serviço e links privados para restringir o acesso aos dados apenas a redes específicas.
Camada de Aplicação: Envolve autenticação e autorização para garantir que apenas usuários autorizados possam acessar os dados.
Camada de Dados: Protege os dados com criptografia e políticas de acesso baseadas em funções.

Migração para o azure
Azure data box pode armazenar até 80TB de dados, mover e protejer seus dados em uma caixa robusta durante o transito
O **Azure Data Box** é uma solução da Microsoft para transferir grandes volumes de dados para o Azure de forma rápida e segura. Aqui está um resumo:

### **O que é o Azure Data Box?**

- **Dispositivos e Serviços**: Inclui uma variedade de dispositivos, como Data Box, Data Box Disk, Data Box Heavy e Data Box Gateway².
- **Uso**: Ideal para mover grandes quantidades de dados (terabytes a petabytes) para o Azure, especialmente quando a transferência via rede não é prática ou é muito lenta³.

### **Principais Características**

- **Segurança**: Os dados são criptografados durante o transporte para garantir a segurança³.
- **Facilidade de Uso**: A Microsoft envia o dispositivo para você, você carrega os dados e o envia de volta. A Microsoft então carrega os dados no Azure³.
- **Variedade de Opções**:
  - **Data Box**: Para grandes volumes de dados.
  - **Data Box Disk**: Para volumes menores e mais portabilidade.
  - **Data Box Heavy**: Para volumes extremamente grandes.
  - **Data Box Gateway**: Uma solução de transferência de dados contínua e em tempo real².

### **Benefícios**

- **Rápido e Confiável**: Acelera a transferência de dados em comparação com métodos tradicionais de rede³.
- **Custo-efetivo**: Reduz custos associados à transferência de grandes volumes de dados³.

Claro! **AzCopy** é uma ferramenta de linha de comando usada para copiar dados de e para o Armazenamento do Azure. Aqui está um resumo:

### **O que é o AzCopy?**

- **Funcionalidade**: Permite transferir dados entre contas de armazenamento do Azure, ou entre o armazenamento local e o Azure¹.
- **Uso**: Ideal para mover grandes volumes de dados de forma eficiente e segura².

### **Principais Características**

- **Alta Velocidade**: Otimizado para transferências rápidas de dados.
- **Flexibilidade**: Suporta vários tipos de armazenamento, incluindo blobs, arquivos e tabelas².
- **Autenticação**: Pode ser autorizado usando Microsoft Entra ID (anteriormente Azure AD) ou tokens SAS (Shared Access Signature)¹.

### **Como Usar**

1. **Instalação**: Baixe e instale o AzCopy a partir do site da Microsoft².
2. **Autorização**: Autorize o AzCopy com suas credenciais do Azure¹.
3. **Comandos**: Use comandos específicos para copiar, mover ou sincronizar dados. Por exemplo:
   ```sh
   azcopy copy 'source' 'destination'
   ```

### **Benefícios**

- **Eficiência**: Reduz o tempo necessário para transferir grandes volumes de dados.
- **Segurança**: Garante que os dados sejam transferidos de forma segura com criptografia.

resumo sobre identidade, acesso e segurança no Azure:

### **Identidade e Acesso**

1. **Microsoft Entra ID (anteriormente Azure AD)**:
   - **O que é**: Serviço de gerenciamento de identidade e acesso baseado na nuvem.
   - **Funcionalidades**: Autenticação multifator (MFA), Single Sign-On (SSO), e gerenciamento de identidades externas³.

2. **Controle de Acesso Baseado em Funções (RBAC)**:
   - **O que é**: Sistema que permite gerenciar permissões de acesso aos recursos do Azure com base nas funções dos usuários.
   - **Uso**: Define quem pode fazer o quê em quais recursos, garantindo que apenas usuários autorizados tenham acesso⁴.

3. **Acesso Condicional**:
   - **O que é**: Ferramenta que aplica políticas de acesso com base em condições específicas, como localização, dispositivo e risco de login.
   - **Uso**: Ajuda a proteger os recursos ao exigir autenticação adicional em situações de risco⁴.

### **Segurança**

1. **Modelo Zero Trust**:
   - **O que é**: Abordagem de segurança que assume que nenhuma rede, interna ou externa, é segura.
   - **Princípios**: Verificação explícita, uso do menor privilégio e suposição de violação⁵.

2. **Defesa em Profundidade**:
   - **O que é**: Estratégia de segurança que utiliza várias camadas de defesa para proteger os dados e recursos.
   - **Camadas**: Inclui segurança de identidade, rede, aplicativos e dados⁵.

3. **Microsoft Defender for Cloud**:
   - **O que é**: Serviço que fornece visibilidade e proteção contra ameaças para recursos do Azure.
   - **Funcionalidades**: Avaliação contínua de segurança, recomendações de melhoria e proteção contra ameaças⁵.

resumo sobre o Microsoft Entra ID e o Microsoft Entra Domain Services:

### **Microsoft Entra ID (anteriormente Azure AD)**

- **O que é**: Um serviço de gerenciamento de identidade e acesso baseado na nuvem.
- **Funcionalidades**:
  - **Autenticação**: Suporta autenticação multifator (MFA) e Single Sign-On (SSO).
  - **Gerenciamento de Identidades**: Permite gerenciar usuários, grupos e dispositivos.
  - **Integração**: Funciona com milhares de aplicativos SaaS e serviços da Microsoft³.
- **Uso**: Ideal para gerenciar identidades e acessos em ambientes híbridos e na nuvem.

### **Microsoft Entra Domain Services (anteriormente Azure AD DS)**

- **O que é**: Um serviço gerenciado que fornece serviços de domínio compatíveis com o Active Directory, como ingressar em domínios, políticas de grupo, LDAP e autenticação Kerberos/NTLM¹.
- **Funcionalidades**:
  - **Gerenciamento de Domínio**: Permite que máquinas virtuais do Azure ingressem em um domínio sem a necessidade de controladores de domínio locais.
  - **Compatibilidade**: Suporta aplicativos legados que dependem de serviços de domínio tradicionais².
- **Uso**: Ideal para migrar aplicativos locais para a nuvem e centralizar o gerenciamento de identidades e acessos.

resumo sobre autenticação e autorização no Azure:

### **Autenticação**

- **O que é**: O processo de verificar a identidade de um usuário ou aplicativo.
- **Como funciona**: Utiliza credenciais como nome de usuário e senha, certificados, ou métodos de logon único (SSO) para confirmar a identidade⁴.
- **Ferramentas no Azure**:
  - **Microsoft Entra ID**: Suporta autenticação multifator (MFA) e Single Sign-On (SSO) para proteger o acesso aos recursos³.
  - **Azure AD B2C**: Permite autenticação de usuários externos, como clientes e parceiros⁴.

### **Autorização**

- **O que é**: O processo de conceder ou negar acesso a recursos com base na identidade autenticada.
- **Como funciona**: Define permissões e políticas que determinam o que um usuário ou aplicativo pode fazer após a autenticação⁴.
- **Ferramentas no Azure**:
  - **RBAC (Role-Based Access Control)**: Permite gerenciar permissões de acesso aos recursos do Azure com base nas funções dos usuários⁴.
  - **Acesso Condicional**: Aplica políticas de acesso com base em condições específicas, como localização e dispositivo⁴.

### **Diferença entre Autenticação e Autorização**

- **Autenticação**: Verifica quem você é.
- **Autorização**: Verifica o que você pode fazer.

O **Acesso Condicional** no Microsoft Entra ID (anteriormente Azure AD) é uma ferramenta essencial para proteger o acesso aos recursos da sua organização. Aqui está um resumo:

### **O que é o Acesso Condicional?**

- **Definição**: O Acesso Condicional é uma política baseada em identidade que aplica controles de acesso com base em sinais específicos, como usuário, localização, dispositivo e risco de login².
- **Objetivo**: Garantir que apenas usuários autorizados e em condições seguras possam acessar os recursos da organização².

### **Como Funciona**

1. **Sinais de Identidade**:
   - **Usuário e Grupo**: Políticas podem ser aplicadas a usuários ou grupos específicos.
   - **Localização**: Acesso pode ser restrito com base na localização geográfica.
   - **Dispositivo**: Verifica se o dispositivo está em conformidade com as políticas de segurança da organização¹.

2. **Controles de Acesso**:
   - **Requer MFA**: Exige autenticação multifator para aumentar a segurança.
   - **Bloquear Acesso**: Pode bloquear o acesso de usuários ou dispositivos que não atendem aos critérios definidos.
   - **Condições de Sessão**: Impõe restrições adicionais durante a sessão, como limitar o download de dados¹.

### **Benefícios**

- **Segurança Aprimorada**: Reduz o risco de acesso não autorizado.
- **Flexibilidade**: Permite criar políticas personalizadas para diferentes cenários e necessidades.
- **Conformidade**: Ajuda a atender requisitos de conformidade e regulamentação².

### **Exemplo de Uso**

- **Trabalho Remoto**: Exigir MFA para acessos fora do escritório.
- **Acesso Sensível**: Bloquear acesso a dados sensíveis de dispositivos não gerenciados.

