# RESUMOS

### LAB 1 - Localizando Serviços por Categoria

Para acessar o portal é necessário criar uma conta no Azure, disponível em portal.azure.com. 

O menu de recursos é padrão para todos os usuários, mas alguns serviços não estão disponíveis na conta gratuita. A navegação pelo portal permite personalizar idioma e aparência. A aba "Todos os serviços" exibe os recursos do Azure por categoria, como Banco de Dados, DevOps, Segurança, etc. Recursos em versão prévia não possuem SLA (Service Level Agreement), podendo ser removidos a qualquer momento, o que pode impactar a confiabilidade desses serviços em ambientes críticos.

### LAB 2 - Criando Máquinas Virtuais no Azure

Cada serviço na Azure possui um SLA, que define sua disponibilidade, variando de 99% a 99.999%. Quanto maior o SLA, menor a indisponibilidade, porém o custo aumenta. 

Para criar uma Máquina Virtual (VM), navegue até "Computação" no menu "Todos os serviços". A redundância do armazenamento pode ser escolhida entre LRS, GRS, ZRS e GZRS, impactando a disponibilidade e o custo. A criação da VM pode ser distribuída em até três zonas de disponibilidade, com diferentes opções de alta disponibilidade. Além disso, ao configurar a VM, é possível habilitar o Azure Spot, que oferece VMs com descontos significativos, mas sem garantia de que a máquina ficará sempre disponível.

### LAB 3 - Tipos de Serviços de Nuvem

Este laboratório aborda a criação de recursos na Azure, diferenciando os tipos de serviços de nuvem: IaaS (Infraestrutura como Serviço), PaaS (Plataforma como Serviço) e SaaS (Software como Serviço). A IaaS requer mais especificações do cliente (hardware, sistema, etc.), enquanto PaaS e SaaS demandam menos envolvimento do usuário. 

A calculadora de custos do Azure oferece uma estimativa dos valores a serem pagos pelos recursos. Cada tipo de serviço exige um nível diferente de administração e controle por parte do usuário: IaaS oferece mais controle, enquanto PaaS e SaaS reduzem a carga administrativa.

### LAB 4 - Componentes de Arquitetura do Azure

O site Azure Global Infrastructure oferece informações detalhadas sobre infraestrutura, sustentabilidade e datacenters da Azure, enquanto o datacenters.microsoft.com explora a cultura dos datacenters e sua distribuição global. Nesse último, é possível visualizar um mapa 3D com informações sobre residência dos dados, zonas disponíveis, localização e replicação, além de fazer um tour virtual pelos datacenters.

Para criar um grupo de recursos, é necessário ter uma assinatura, definir o nome e a região, e opcionalmente adicionar marcações para facilitar a gestão de custos. Funcionalidades úteis incluem: log de atividades, que informa o histórico de criação/exclusão de recursos; IAM, que garante permissões sobre o grupo de recursos; visualizador de recursos, que exibe os recursos em uma estrutura em árvore; eventos, que permitem automação; e implantações, que detalham os recursos criados e seu status.

### LAB 5 - Computação e Rede

A criação de VMs pode ser feita utilizando configurações predefinidas ou especificando todos os detalhes. Algumas opções incluem assinatura, grupo de recursos, disponibilidade (zonas ou conjuntos de dimensionamento) e opções de Spot, que permite utilizar VMs a preços mais baixos com menor garantia de disponibilidade. Funções como backup, alertas e extensões também podem ser configuradas. Durante a criação de áreas de trabalho virtuais, pode-se definir limites de sessões e tipos de hosts. Em aplicativos de funções, a pilha de runtime depende da linguagem escolhida. Além disso, a opção "Excluir com VM" garante que, ao deletar a VM, o disco e outros recursos associados sejam excluídos automaticamente.

### LAB 6 - Armazenamento

Contas de armazenamento no Azure suportam diferentes tipos de dados (blobs, arquivos, tabelas), com redundância ajustável (LRS, GRS, ZRS ou GZRS). Dependendo das necessidades de latência, pode-se optar por armazenamento Standard ou Premium. Ferramentas como o AzCopy e o Gerenciador de Armazenamento do Azure facilitam a transferência de dados para a nuvem. Também existem várias opções de migração de dados, como o Data Box Disk, Data Box e Import/Export Job. As contas de armazenamento também devem ter um nome exclusivo globalmente, pois o acesso se dá por meio de URLs específicas para cada conta e tipo de dado.

### LAB 7 - Identidade, Acesso e Segurança

No Microsoft Entra ID, usuários podem ser criados, sincronizados de ambientes on-premise, ou convidados externamente. O reset de senha pode ser habilitado via Self-Service Password Reset. Domínios personalizados podem ser configurados, assim como convites em massa através de upload de CSV. O Microsoft Defender for Cloud oferece recomendações de segurança para ambientes Azure e multicloud. Usuários excluídos ficam "congelados" por 30 dias, permitindo sua restauração antes da exclusão definitiva.

### LAB 8 - Gerenciamento de Custos

A Calculadora de TCO (Custo Total de Propriedade) estima o custo da migração para a nuvem comparando com o ambiente on-premise. A Calculadora de Preço do Azure prevê o custo dos recursos baseados em suas especificações. O Cost Management permite configurar alertas e orçamentos de custo, ajudando a controlar os gastos e otimizá-los. Além disso, é possível adicionar marcas (tags) para melhorar a organização e a identificação dos custos entre os grupos de recursos.

### LAB 9 - Governança e Conformidade

O Portal de Confiança do Serviço oferece informações sobre regulamentos e certificações aplicados pela Microsoft. O Microsoft Purview, que pode ser testado por 90 dias, auxilia na coleta e validação de dados. Políticas de governança podem ser criadas para monitorar a conformidade dos recursos com os padrões estabelecidos, e essas políticas podem ser personalizadas e testadas antes da ativação completa. Políticas podem ser ajustadas para ficarem inativas enquanto estão sendo testadas, com a possibilidade de enforcement automático quando ativadas.

### LAB 10 - Ferramentas de Gerenciamento e Implantação

A Azure CLI permite executar comandos diretamente no portal, sem depender da interface gráfica. O Azure Arc é uma ferramenta de gerenciamento multicloud, permitindo centralizar a gestão de recursos de diferentes nuvens. É uma solução robusta, sem concorrentes diretos no mercado. O Azure Arc também traz uma série de funcionalidades que facilitam a governança e automação de recursos híbridos e multicloud.

### LAB 11 - Ferramentas de Monitoramento do Azure

O Azure Monitor oferece insights e monitoramento de vários aspectos, como aplicações, containers, redes e VMs. Ele também inclui alertas, logs e métricas de desempenho. O Service Health informa sobre manutenções e disponibilidade de regiões. O Azure Advisor fornece recomendações para otimização de custo, segurança, excelência operacional, desempenho, entre outros. O Advisor também categoriza essas recomendações em áreas específicas, como segurança, custo e eficiência operacional.

# Anotações LABs

## LAB 1 - Localizando Serviços por Categoria

É necessário criar uma conta na Azure para poder acessar o portal

Acessar o portal pelo site: portal.azure.com

O menu de recursos é igual para todos, porém alguns recursos não são disponíveis para uma conta gratuita utilizar

É possível modificar as configurações de idioma e aparência do portal

A aba do Menu - Todos os serviços, exibe tudo que existe no Azure por categorias (Banco de dados, DevOps, Segurança, Rede, Armazenamento...)

Existe recursos em versão prévia, estes recursos não estão em garantia (não possuem o SLA - Service Level Agreement), ou seja, podem ser retirados a qualquer momento

# 

## LAB 2 - Criando máquinas Virtuais na Azure

Cada recurso na Azure possui um SLA (Service Level Agreement) que indica o quanto este dado recurso pode vir a ficar indisponível

Possui uma faixa de 99%-99.999%, quanto mais 9's menor será o tempo de indisponibilidade do recurso, entretanto se tornará mais custoso

Existe uma tabela na própria Azure que demonstra a faixa de tempo de indisponibilidade de cada SLA.

Acessar a parte de criação de uma Máquina virtual: Menu -Todos os serviços -> Computação -> Máquinas virtuais

É possível criar uma VM em até 3 zonas de disponibilidade

Existem outras formas de opções de disponibilidade além da zona de disponibilidade, porém cada opção alterará em qual faixa o SLA estará

É possível escolher a forma de redundância do armazenamento em LRS, GRS, ZRS e GZRS. Cada abordagem influencia no modo em que será armazenado e sobre sua disponibilidade, além de influenciar no valor final


## LAB 3 - Tipos de Serviços de Nuvem

A criação de uma máquina virtual demanda muitas especificações (imagem do sistema, componentes do hardware, os softwares utilizados...) da parte do cliente (quem está solicitando a criação) por conta de ser uma IaaS (Infraestrutura como Serviço). A criação de um Banco de Dados SQL na Azure demanda menos especificações (nome do banco, servidor, autenticação...).

A cada criação de recurso temos uma previsão de custo a partir da calculadora de custos do Azure.

Cada serviço terá uma certa quantidade de envolvimento do usuário e do provedor (Azure), sendo o IaaS com maior envolvimento do usuário, PaaS (Plataforma como Serviço) no intermédio, e o SaaS (Software como Serviço) com o menor envolvimento do usuário.


## LAB 4 - Componentes de arquitetura do Azure

O site Azure global infrastructure possui muitas informações sobre a infraestrutura, sustentabilidade, sobre os datacenters...

O site datacenters.microsoft.com tem muitas informações sobre a cultura e os datacenters que existem e estão a vir. Nele é possível visualizar o mapa mundi em 3D com as regiões contém muitas informações, entre elas: residência dos dados, zonas disponíveis, localização, replicação dos dados... Além disso, é possível fazer um tour nos datacenters da Azure, visualizando o ambiente em uma experiencia 3D.

Para criar um grupo de recursos e necessário uma assinatura, informar o nome do grupo e a região (dependendo da assinatura, alguma região pode ficar indisponível), inserir marcações (não é obrigatório, entretanto, é importante para ter uma melhor gestão dos custos), por fim criá-lo.

Ao criar o grupo de recurso, temos algumas opções interessantes:

Log de atividades informa o que e quando foi criado/excluído quem criou... 

IAM (Controle de Acesso) da a permissão sobre o grupo de recursos para alguém ou remove, de modo a evitar problemas em caso de exclusão/alteração acidental ou proposital

Visualizador de recursos demonstra os recursos que foram criados em forma de arvore

Eventos é possível criar eventos automatizados

Implantações mostra os recursos que foram criados, quanto tempo demorou para criá-lo, removê-lo, status...

## LAB 5 - Computação e Rede

Na área de criação de uma VM é possível criar uma especificando todas as funcionalidades do zero ou utilizar uma configuração predefinida - por fim, será necessário apenas especificar as informações que faltam e criar a VM.

Durante a criação de uma maquina virtual do zero temos algumas opções interessantes:

- Assinatura -> Assinatura do Usuário

- Grupo de Recursos -> O grupo ao qual este recurso pertencerá 

- Opções de disponibilidade 
	- Nenhuma

	- Zona de Disponibilidade
		- Determinando quantas Zonas serão utilizadas

	- Conjunto de Dimensionamento de máquinas virtuais
		- Determina quantas instancias serão utilizadas por padrão e em caso de aumento de demanda determina quantas instancias serão aumentadas (escala horizontalmente de acordo com certos eventos especificados pelo cliente)

	- Conjunto de disponibilidade

- Spot do Azure -> Ao selecionar esta opção pode-se utilizar uma VM por preços muito baixos, porém sem a certeza de ter esta VM disponível a todo instante. É uma opção interessante apenas para desenvolvimento.

- Excluir com VM -> Se selecionado, ao excluir a VM o disco será excluído junto (evitando o problema de discos órfãos)

- Excluir o IP publico e a NIC quando a VM for excluída

- Habilitar Backup

	- Subtipo de política -> Padrão ou Avançado (determina a quantidade de backup por dia, nível operacional...)

- Alertas -> informa via email sobre níveis críticos do sistema

- Extensões -> É possível instalar extensões na VM

- Marcas -> Adicionas as marcas (tags)

- Revisar + criar -> Área que informa tudo que foi alocado na VM, informa o preço do recurso e finaliza a criação


Durante a criação de uma Área de Trabalho Virtual do Azure temos algumas opções interessantes:

Tipo de Pool de hosts -> Em pool ou Pessoal (o pool é utilizado quando inúmeros terão acesso, enquanto o pessoal somente um)

Limite máximo de sessão -> Quantos usuários por host de sessão

Durante a criação de uma Aplicativo de Funções temos algumas opções interessantes:

Pilha de runtime -> dependendo da linguagem de programação escolhida não será possível fazer uma escolha de sistema operacional, pois só haverá um sistema operacional disponível para tal linguagem

## LAB 6 - Armazenamento

### Conta de Armazenamento 

Uma conta de armazenamento (storage account) pode receber dados de vários tipos (blobs, files, tabelas...). Deve ser exclusivo globalmente. É possível escolher entre Standard e Premium (o Premium e recomendado para baixas latências, só que é mais custoso). É necessário dizer qual será a redundância de armazenamento (LRS, GRS, ZRS ou GZRS)

Cada componente criado tem a sua url própria seguindo o padrão: https://<nome-da-conta>.<tipo-do-dado>.core.windows.net/<nome-do-dado>

Ex. - Para uma fila com nome teste inserida na conta stocanaldacloud01: https://stocanaldacloud01.queue.core.windows.net/teste

### Migrações para Azure

Ambiente destinado a especificar qual será a forma de migração dos dados para a Azure (também é possível realizar a exportação dos dados da Azure). Contem algumas formas de migrações como o Data Box Disk (35TB) Data Box (80TB), Databox Heavy (800TB) e Import/Export Job (1TB), cada um com as suas especificações.

### Opções de Gerenciamento de Arquivos

É possivel utilizar o AzCopy (**Utilitário de linha de comando) para copiar os blobs ou arquivos para sua conta de armazenamento de forma unidirecional

É possivel,  também, utilizar o Gerenciador de Armazenamento do Azure (Interface Grafica do Usuário - que utiliza o AzCopy por debaixo dos panos), compatível com o Windows, MacOS e Linux

## LAB 7 - Identidade, Acesso e Segurança

### Microsoft Entra ID

É possivel criar e gerenciar usuários e é possível covidar um usuário externo. Os usuários podem vir de um ambiente on-premisse e serem sincronizados. É possível deletar um usuário e ele permanecerá "congelado" por 30 dias, sendo possível restaurar esta conta até este tempo.

É possível colocar o Self-Service Password Reset (O próprio usuário reseta a sua senha, contudo, é necessário comprar esta feature)

É possível criar um domínio personalizado para adicionar a um grupo de usuários.

É possível realizar um Bulk invite (convite em massa - basta fazer upload de um arquivo csv, do template da Azure, com os dados)

A parte de Roles and administrators relaciona o permissionamento que uma conta terá em relação entre outras contas e não em relação a criação/exclusão de recursos

### Microsoft Defender for Cloud

É o verificador de segurança da nuvem. É possível verificar tanto na Azure quanto em outras clouds como está a segurança. Possui recomendações de segurança.

## LAB 8 - Gerenciamento de custos

### Calculadora do TCO (Custo Total de Propriedade)

Utilizada para calcular o custo de migração para nuvem

Informa-se o que será utilizado para realizar a migração

Por fim, demonstra uma estimativa do valor de custo, em 3 anos, no ambiente on-premisse (atual) e no ambiente da nuvem

### Calculadora de Preço do Azure

Utilizada para calcular o custo da alocação dos recursos na nuvem

É necessário informar as especificações do recurso (por exemplo, sistema operacional, tempo de execução...)

Por fim teremos o valor estimado de quanto custará este recurso por mês 

Cada especificação do recurso pode modificar o valor de custo tanto para mais quanto para menos

É necessário avaliar qual a melhor especificação para a empresa e para o custo total do recurso

### Gerenciamento de Custo (Cost Management)

É possível determinar um alerta de custo para que caso passe de um certo valor um email seja enviado informando que o custo ultrapassou o estipulado

É possível analisar o custo dos recursos

Possui sugestões de melhorias em relação a custos

É possível criar um budget de custo, para que o recurso não ultrapasse um custo predeterminado na hora da sua criação

### Marcas (Tags)

É possível adicionar marcas a um grupo de recursos

De modo a especificar, e melhorar, a visualização sobre o que é o grupo de recursos


## LAB 9 - Governança e Conformidade

### Portal de Confiança do Serviço

É um ambiente que possui os regulamentos, certificações padrões, entre outros que a Microsoft aplica

### Microsoft Purview

É necessário criar um e adicioná-lo a um grupo de recursos

Trabalha em conjunto com o 365

Contem inúmeras funcionalidades

Ajuda na coleta de dados e a validação de informações destes

Faz uma analise dos dados e traz um report destes dados

É free-trial por 90 dias

### Políticas (Policy)

Mostra as políticas existentes

Mostra se as políticas estão sendo satisfeitas (compliant) ou não (non-compliant)

É possível criar políticas personalizadas utilizando uma politica existente ou fazendo uma do zero

Policy enforcement seta a politica como inativa (útil para casos em que a política esta em testes), se for colocada como disabled (por padrão fica ativa)

## LAB 10 - Ferramentas de Gerenciamento e Implantação

### Azure CLI (Command Line Interface)

No portal do Azure possui um botão para o CLI do PowerShell ou Bash

Utilizado para executar comandos, seja para a criação ou para o ajuste de recursos

Util para não ser dependente do Portal do Azure para a criação dos recursos

### Azure Arc

É uma ferramenta de gerenciamento multicloud

Necessita ser configurada com diversos padrões e recursos

É uma ferramenta poderosa na questão de gestão e centralização de recursos

Traz uma serie de funcionalidades

Não há um concorrente para o Azure Arc atualmente

## LAB 11 - Ferramentas de Monitoramento do Azure

### Monitor

Possui algumas formas de insight como o Application, Container, Network, VM...

Possui métricas, alertas, logs

Traz uma visão de tudo que o usuário possui no Azure

O Service Health que está presente no Azure Monitor, é um local que demonstra se há alguma região com disponibilidade afetada, manutenção programada, recomendações de saúde e recomendações de produto de segurança

### Advisor

É o centro de recomendações

É capaz de trazer insights (ideias) para ajustar um problema

Traz recomendações de custo, segurança, exlencia operacional, performance...
