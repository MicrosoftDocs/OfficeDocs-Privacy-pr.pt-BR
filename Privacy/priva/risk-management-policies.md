---
title: Políticas de Gerenciamento de Riscos de Privacidade
f1.keywords:
- CSH
ms.author: chvukosw
author: chvukosw
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- M365-security-compliance
- M365-priva-privacy-risk-management
search.appverid:
- MOE150
- MET150
description: Saiba como criar e gerenciar políticas no Gerenciamento de Riscos de Privacidade da Microsoft Priva para lidar com os dados pessoais da sua organização Microsoft 365.
ms.openlocfilehash: 87671cedc8c6cba75d5ad207b52831cdd2467187
ms.sourcegitcommit: b5f7dcb73c0e3f677981e80106769cb546d00af4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2022
ms.locfileid: "65014491"
---
# <a name="privacy-risk-management-policies"></a>Políticas de Gerenciamento de Riscos de Privacidade

As políticas de Gerenciamento de Risco de Privacidade podem ajudá-lo a lidar com cenários de risco importantes para sua organização. Nossos modelos de política são centralizados em promover práticas de tratamento de dados de som.  Os alertas permitem que os administradores saibam quando as correspondeções de política são detectadas e podem precisar de mais investigação. As notificações por email e dicas Microsoft Teams ajudar os usuários a entender quais atividades têm riscos de privacidade, permite que os usuários corrijam imediatamente os problemas e os apontem para o treinamento de privacidade.

Para um início rápido, use um modelo com configurações padrão para criar novas políticas para superexposure de dados, transferências de dados e minimização de dados e cenários. Você também pode personalizar as configurações de modelo para criar políticas que atendam às necessidades da sua organização.

## <a name="policy-template-types"></a>Tipos de modelo de política

O Gerenciamento de Riscos de Privacidade tem três modelos de política projetados para ajudá-lo a abordar as principais áreas de preocupação em relação à proteção de dados pessoais. Cada modelo tem configurações padrão que você pode aceitar no processo de configuração rápida ou personalizar usando um processo guiado. Quando você cria uma nova política, sua primeira tarefa será escolher um dos três modelos listados abaixo:

- **Superexposure de dados**: essa política identifica itens de conteúdo que contêm dados pessoais que podem ser amplamente acessíveis por outras pessoas. Quando as correspondências são encontradas, você pode configurar notificações solicitando que os proprietários de conteúdo apliquem proteção rapidamente.

- **Transferências de** dados: essa política pode detectar transferências de dados pessoais entre limites que você determina, o que pode envolver transferências fora da sua organização ou transferências internas entre departamentos ou regiões geográficas. Quando as correspondências são encontradas, você pode configurar notificações incentivando os remetentes a revogar o acesso ao conteúdo.

- **Minimização de dados**: essa política identifica itens de conteúdo que contêm dados pessoais que foram intocados por longos períodos de tempo. Quando forem encontradas correspondências, você poderá enviar notificações aos proprietários de conteúdo solicitando que eles executem uma ação rápida para manter ou excluir o item.

## <a name="quick-setup-using-a-template-with-default-settings"></a>Configuração rápida: usando um modelo com configurações padrão

Ao criar uma política diretamente de um modelo, a maioria das configurações será escolhida automaticamente para ajudá-lo a começar a trabalhar rapidamente. Siga estas etapas para criar uma política com configurações padrão usando um de nossos modelos:

1. No centro [de conformidade do Microsoft Purview](https://compliance.microsoft.com/), localize Priva Privacy Risk Management no painel de navegação esquerdo e selecione **Políticas**.

2. Selecione **Criar uma política** no canto superior direito da tela, que exibe um painel de submenu listando todas as opções de criação de política.

3. Localize o tipo de política que você deseja criar e, em seu cartão, selecione **Criar**.

4. Um painel de submenu contém detalhes da política. Selecionar **as configurações de Exibição** mostrará as configurações padrão. Você pode editar as configurações daqui, o que o levará para o processo guiado descrito abaixo. Para continuar criando sua política usando as configurações padrão, basta inserir um nome descritivo e, em seguida, selecionar **Criar política**.

Sua política será criada e você a encontrará listada na página **Políticas** .

A política começará a ser executada no modo de teste, o que significa que nenhum alerta ou notificação será gerado e você poderá monitorar seu desempenho. Quando estiver pronto para ativar a política, selecione sua política e edite-a para ativá-la.

## <a name="custom-setup-guided-process-to-choose-all-settings"></a>Configuração personalizada: processo guiado para escolher todas as configurações

A opção de política personalizada é um processo guiado para criar uma política. Você começará escolhendo um modelo e percorrerá cada configuração para personalizar sua política. As instruções a seguir fornecem detalhes sobre as configurações básicas que se aplicam a cada um dos três tipos de política. Quando as configurações diferem por tipo de política, vinculamos a instruções específicas.

Siga as etapas abaixo para criar uma política:

1. No painel [Centro de conformidade do Microsoft 365](https://compliance.microsoft.com/), localize Priva Privacy Risk Management no painel de navegação esquerdo. No menu suspenso, selecione **Políticas**.

2. Selecione **Criar uma política**.

3. Escolha a **opção Personalizada** para criar sua política usando o assistente de criação de política no Gerenciamento de Riscos de Privacidade.

4. Escolha o tipo de política: **Superexposure de dados,** **transferências de dados ou** **minimização de dados**.

5. Dê um nome descritivo à sua política para ajudá-lo a identificá-la em sua lista de políticas. Forneça uma descrição opcional e selecione **Avançar**.

6. As próximas etapas permitem definir todas as configurações de política. Você pode ir para descrições neste artigo para obter mais detalhes. As opções são:
    - [**Dados a serem monitorados**](#choose-data-to-monitor): selecione o tipo de dados pessoais que sua política monitorará.
    - [**Usuários e grupos**](#choose-users-and-groups): aplique sua política a todos os usuários ou usuários selecionados.
    - [**Locais**](#choose-locations): aplique sua política às áreas selecionadas no Microsoft 365.
    - [**Condições**](#set-conditions): defina as condições para sua política. Essas opções variam dependendo do tipo de política.
    - [**Resultados**](#define-outcomes-user-email-notifications-and-tips): defina os resultados quando uma correspondência de política for encontrada, como notificações por email do usuário.
    - [**Alertas**](#set-alerts): decida a frequência de alertas para administradores quando uma correspondência de política for encontrada.
    - [**Modo**](#testing-a-policy): escolha se deseja ou não executar sua política no modo de teste primeiro.
7. Quando todas as configurações forem concluídas, examine suas escolhas, faça as edições desejadas e selecione **Enviar para criar** a política.

Após alguns segundos, você verá uma confirmação de que a política foi criada. Selecione **Concluído** na página de confirmação, que levará você para a página  Políticas, na qual você verá a nova política na parte superior da tabela.

As seções imediatamente abaixo fornecem mais detalhes sobre cada configuração de política.

## <a name="choose-data-to-monitor"></a>Escolher dados a serem monitorados

Ao criar ou editar uma política, solicitaremos que você selecione quais tipos de dados a política deve monitorar. Há duas opções:

- **Grupos de classificação**: uma lista pesquisável de agrupamentos de tipos de informações confidenciais; por exemplo, um grupo baseado na Lei de Registros de Integridade da Austrália ou um grupo baseado em informações de identificação pessoal dos EUA, como um número de passaporte dos EUA.

- **Tipos de informações confidenciais individuais**: uma lista pesquisável de tipos de informações confidenciais; por exemplo, números de seguro social ou números de carteira de motorista.

Se você selecionar entre os grupos de classificação existentes, também não poderá selecionar tipos individuais ou criar seus próprios grupos. Para obter mais flexibilidade, escolha tipos de informações confidenciais individuais. Para utilizar os padrões mais comuns, escolha entre os grupos de classificação. Saiba mais sobre cada tipo de dados abaixo.

### <a name="classification-groups"></a>Grupos de classificação

Os grupos de classificação são agrupamentos de [tipos de informações confidenciais](/microsoft-365/compliance/sensitive-information-type-entity-definitions) que são usados para detectar conteúdo relacionado a dados pessoais ou regulamentos específicos.

Ao selecionar essa opção na página Dados a serem **monitorados** , você precisará selecionar **+** Adicionar grupos de classificação e escolher um ou mais grupos na lista que aparece em um painel de submenu.

### <a name="individual-sensitive-information-types"></a>Tipos de informações confidenciais individuais

Ao escolher tipos [de informações confidenciais](/microsoft-365/compliance/sensitive-information-type-entity-definitions) específicos, como números de seguro social ou informações de carteira de motorista, você pode personalizar seu próprio grupo ou grupos de dados para procurar. Você pode selecionar na lista completa de tipos de informações confidenciais no Gerenciamento de Riscos de Privacidade. Cada tipo de informação tem suas próprias propriedades.

Quando você seleciona essa opção na página Dados a serem **monitorados**, um seletor  é exibido com Padrão listado como um nome para o grupo de tipos de informações confidenciais que você selecionará. Mantenha ou edite esse nome de grupo e selecione **Adicionar** para selecionar um ou mais tipos de informações confidenciais na lista completa no Gerenciamento de Riscos de Privacidade. Cada tipo de informação tem suas próprias propriedades e configurações recomendadas, que você pode descobrir selecionando o ícone de informações à direita do menu suspenso de confiança depois de adicionar o tipo de informação. Você também pode alterar a contagem de instâncias para cada tipo de informação confidencial. Essa configuração designa o número de instâncias exclusivas de cada tipo de informação confidencial que você deseja que sua política detecte.

Se você criar mais de um grupo, o assistente permitirá que você selecione como os grupos devem se relacionar (uma relação "e" ou "ou" ) e defina sua ordem de operações.

## <a name="choose-users-and-groups"></a>Escolher usuários e grupos

Você tem duas opções para decidir quais usuários uma política abordará: todos os usuários e grupos ou usuários e grupos específicos.

- **Todos os usuários e grupos**: essa opção aplicará a política a todos os usuários e Office 365 grupos em sua organização.

- **Usuários ou grupos específicos**: essa opção permite selecionar usuários individuais, grupos Office 365 individuais ou uma combinação de ambos.
  - **Para escolher usuários**: selecione **Escolher** usuários e, no painel de submenu, pesquise um usuário inserindo um endereço de email na caixa de pesquisa. Ou localize o usuário na lista e marque a caixa de seleção à esquerda do nome. Você pode selecionar até 100 usuários. Quando terminar, selecione **Adicionar.**
  - **Para escolher grupos**: selecione **Escolher grupos** e, no painel de submenu, marque a caixa de seleção à esquerda de cada nome de grupo. Você pode selecionar até dez grupos. Quando terminar, selecione **Adicionar**.

Depois de designar usuários e grupos, selecione **Avançar** para avançar para a próxima etapa.

## <a name="choose-locations"></a>Escolher locais

Nesta etapa, você designará onde, em seu ambiente Microsoft 365, deseja que a política procure por correspondentes de dados pessoais. As opções de localização dependerão do tipo de política e você pode selecionar mais de um. Cada um dos locais é explicado abaixo.

- **Exchange**: a política identificará as correspondentes nas contas de Exchange dos usuários, que incluem conteúdo no corpo de emails e em anexos enviados ou recebidos por Exchange de correio.

- **OneDrive**: a política identificará as correspondentes nos arquivos armazenados na conta OneDrive for Business dos usuários.

- **Teams**: a política identificará as correspondentes nas mensagens dos usuários Teams canais e chats.

- **SharePoint**: a política identificará as correspondentes em arquivos armazenados em sites SharePoint usuários. Ao selecionar essa opção, você escolherá entre as seguintes opções:
    - **Todos SharePoint:** essa seleção abrangerá todos os sites para todos os usuários em sua organização.

    - **Sites SharePoint específicos**: essa seleção solicita que você designe sites específicos para a política a ser aplicada. Você pode inserir a URL de um site específico diretamente na caixa de URL e, em seguida, **+** selecionar o sinal para adicioná-lo à sua lista de sites. Você também pode selecionar **Escolher sites** e, no painel de submenu, pesquisar e selecionar na lista de sites aos quais você tem acesso. Marque a caixa que aparece quando você passa o mouse sobre o site que deseja selecionar. Depois de fazer suas seleções, selecione **Adicionar**.  Todos os sites escolhidos serão listados na parte inferior da página **Locais** .
    
    > [!TIP]
    > Se você precisar de ajuda para identificar os sites SharePoint em sua organização, visite Gerenciar sites no SharePoint [de administração](/sharepoint/manage-sites-in-new-admin-center).

Depois de concluir a designação de locais, selecione **Avançar**.

## <a name="set-conditions"></a>Definir condições

As condições para detectar correspondências de política diferem com base no modelo de política.

- **Superexposure de dados**: consulte a etapa de condições nas instruções de configuração personalizada da [política de exposição de dados](risk-management-policy-data-overexposure.md#custom-setup-guided-policy-creation-process).
- **Transferências de dados**: consulte a etapa de condições nas instruções de configuração personalizada [da política de transferências de dados](risk-management-policy-data-transfer.md#custom-setup-guided-policy-creation-process).
- **Minimização de dados**: consulte a etapa de condições nas instruções de configuração personalizada da política [de minimização de dados](risk-management-policy-data-minimization.md#custom-setup-guided-policy-creation-process).

## <a name="define-outcomes-user-email-notifications-and-tips"></a>Definir resultados: dicas e notificações por email do usuário

As configurações de resultados são tratadas na página **Resultados** do assistente de criação de política. Nesta página, você pode optar por enviar uma notificação por email aos usuários quando eles executarem uma ação que corresponda às condições de uma política.

As políticas de transferência de dados têm uma opção adicional para mostrar dicas aos usuários Teams quando suas ações geram uma correspondência de política. Essas dicas incluirão links para treinamento de privacidade, que você fornece, e incluirá mecanismos para corrigir possíveis riscos.

Essas notificações podem ser oportunidades úteis para impedir o escalonamento de problemas e para criar habilidades e confiança dos usuários na adoção de práticas seguras de tratamento de dados.

Visite [as notificações do usuário no Gerenciamento de Riscos de Privacidade](risk-management-notifications.md) para saber mais sobre como trabalhar com notificações do usuário.

## <a name="set-alerts"></a>Definir alertas

Os alertas ajudam os administradores a saber quando um evento de usuário corresponde às condições de uma política. A configuração de alertas é opcional e você controla com que frequência os alertas são gerados, o limite que deve ser atingido antes que um alerta seja gerado e a gravidade do alerta. Os alertas são **exibidos no cartão Alertas** na **página** Políticas. Saiba mais sobre [como exibir, investigar e corrigir alertas](risk-management-alerts.md).

#### <a name="turn-on-alerts"></a>Ativar alertas

Você pode ativar alertas ao criar uma política pela primeira vez ou editar a política mais tarde para ativá-los. Na página **Alertas** do assistente de criação de política, defina o botão de alternância Criar **alertas** para a **posição** Ativado.

#### <a name="alert-frequency-and-thresholds"></a>Frequência e limites de alerta
Depois de ativar alertas, decida com que frequência eles serão gerados.

- **Alertar sempre que ocorrer uma correspondência de política**: selecionar essa opção pode gerar um grande número de alertas.
- **Alerta quando um limite específico for atingido**: você definirá limites com base no número e na frequência de eventos de usuário detectados.

#### <a name="alert-severity-level"></a>Nível de severidade do alerta
Selecione um nível de severidade baixo, médio ou alto. Sugerimos que sua organização defina o que cada nível representa para você.

## <a name="testing-a-policy"></a>Testando uma política

Quando você cria uma política, a configuração padrão é in inicie-a no modo de teste. Isso significa que, depois que a política é criada:

- Nenhum alerta será gerado. No entanto, você verá insights na página de detalhes da política quando as correspondeções forem detectadas, incluindo os tipos de dados detectados e seus locais.

- Nenhuma notificação por email do usuário será enviada quando as correspondentes à política forem detectadas. No entanto, você verá insights na página de detalhes da política mostrando quais usuários estão associados às correspondentes à política.

O modo de teste permite que você procure por partidas dos últimos 30 dias de atividade do usuário. Usando esses insights, você pode medir o comportamento da política e examinar os tipos de alertas que podem ser gerados quando a política está ativada.

Recomendamos testar sua política por pelo menos cinco dias para ajudá-lo a entender o tipo e o volume de corresponde que ela gerará. Você pode [editar a política](#edit-a-policy) enquanto ela estiver no modo de teste para que possa monitorar como as alterações afetam seu desempenho antes de ativá-la. Por exemplo, você pode descobrir que a política é muito ampla e suas condições precisam ser ajustadas. Ou você pode perceber com base na atividade que detecta que os alertas não serão gerados em um período útil para você.

A página de detalhes da política indica quantos dias o teste está em execução. Você verá quantas correspondências foram encontradas por local, quantos eventos de usuário que correspondem às condições da política foram detectados e os tipos de dados pessoais detectados por correspondências de política.

> [!NOTE]
> Se você alternar a opção **Executar** no modo de teste para  a posição *Desativada, isso* ativará sua política quando terminar de criá-la. Isso significa que todos os alertas ou notificações do usuário que você configurar começarão a gerar quando forem detectadas correspondentes.

Quando estiver satisfeito com as configurações da política e estiver pronto para ativá-la, selecione o botão azul Ativar **política** . A política agora estará ativa e gerará todos os alertas e notificações de usuário que você configurar.

## <a name="turn-on-a-policy"></a>Ativar uma política

Você pode definir uma política para ser ativada assim que terminar de criá-la. Isso não é recomendado, pois é melhor monitorar o desempenho e as configurações colocando a política no modo de teste antes de ativá-la (consulte Testar [uma política](#testing-a-policy)).

Se você criou sua política no modo de teste, poderá ativá-la rapidamente seguindo estas etapas:

1. Na página **Políticas** , localize a política e selecione seu nome para abrir sua página de detalhes.
2. No cartão **de status Política** , selecione **Ativar política**.

A política agora estará ativa e gerará todos os alertas e notificações de usuário que você configurar.

## <a name="turn-off-a-policy"></a>Desativar uma política

Você pode desativar uma política a qualquer momento selecionando  Desativar política no canto superior direito da página de detalhes de uma política. Quando uma política estiver desativada, ela não detectará correspondentes nem gerará alertas ou notificações por email. Desativar uma política não excluirá uma política. Você pode ativar novamente uma política selecionando Ativar  política no canto superior direito da página de detalhes da política.

## <a name="view-details-and-activity-from-the-policy-details-page"></a>Exibir detalhes e atividades na página de detalhes da política

Cada política tem uma página de detalhes mostrando as atividades detectadas pela política e os insights para ajudá-lo a lidar com os riscos.

Depois que a política tiver sido criada, selecione seu nome na tabela na página **Políticas** principal. A **guia** Visão geral da página de detalhes da política informa o status da política, fornece insights sobre seus dados e realça as correspondentes à política. Aqui, você pode exibir detalhes sobre as correspondentes de política específicas e saber mais sobre as próximas etapas. Se sua política estiver em execução no modo de teste, você verá as próximas etapas recomendadas nesta página e um botão para ativar a política.

Quando a política estiver ativada, você poderá continuar a examinar sua página de detalhes de política para ver informações contínuas sobre áreas problemáticas, gravidade e tendências de alerta e ações corretivas executadas.

### <a name="overview-tab"></a>Guia Visão geral

Na guia **Visão geral** da página de detalhes da política, você encontrará detalhes sobre o que a política está detectando em relação a tipos e locais de dados e atividade do usuário. Os insights na página de detalhes da política são descritos abaixo. Depois de ativar uma política, pode levar até 48 horas para que os dados possam ser passados.

#### <a name="policy-status"></a>Status da política

O cartão de status da política indicará se a política está em um dos três estados: **Testando**, **Ativado** ou **Desativado**.

**Teste**: esta seção mostra o número de dias que sua política esteve no modo de teste, o que significa que ela está procurando correspondências de política com base nas condições definidas, mas não está gerando alertas ou notificações do usuário. Forneceremos uma recomendação quando for um bom momento para ativar sua política. Você pode ativá-lo a qualquer momento selecionando **o botão Ativar política** neste cartão.

**On**: Quando sua política está ativada, o cartão de status exibe métricas que realçam quando a ação corretiva ocorreu depois que uma política corresponde a gerar alertas e notificações do usuário.

- **Ações do usuário** executadas: essa métrica mostra o número de ações de correção executadas pelos usuários quando solicitado a partir de um email de notificação do número total de notificações enviadas. Por exemplo, 8/10 representaria que, de 10 notificações de usuário enviadas, os usuários executam uma ação de correção em 8 instâncias.

- **Taxa de resolução do** usuário: essa métrica é a taxa na qual as ações de correção são executadas pelos usuários com base no número de notificações geradas. Se o percentual for baixo, talvez você queira editar o conteúdo do [email](risk-management-notifications.md#preview-and-customize-email-content) ou examinar de perto as partidas para determinar se a política está detectando a atividade pretendida.

- **Ações de administrador** executadas: essa métrica mostra o número de ações de correção executadas pelos administradores quando um alerta é gerado pela política. Saiba mais sobre [como executar ações em alertas](risk-management-alerts.md#manage-alerts).

- **Taxa de resolução do** administrador: essa métrica é a taxa na qual as ações de correção são executadas pelos administradores com base no número de alertas.

#### <a name="matches-by-location"></a>Corresponde por local

As **Combinações por cartão** de localização exibem o número de itens de conteúdo detectados pela política de acordo com Microsoft 365 local.

#### <a name="user-notifications"></a>Notificações do usuário

O **cartão de notificações do** usuário exibe um gráfico de barras mostrando o número de emails de notificação do usuário que foram gerados pela política se você tiver esses recursos ativados.

#### <a name="matches-by-user"></a>Corresponde por usuário

As **Correspondências por cartão** de usuário listam os principais usuários cujas ações dispararam uma correspondência de política. Você verá o número de eventos detectados pela política para cada usuário, juntamente com o número de ações de correção executadas de notificações por email. Selecione **Exibir todos os** usuários neste cartão para examinar a lista completa de usuários detectados pela política.

#### <a name="matches-by-data-type"></a>Corresponde por tipo de dados

O **cartão Corresponde por tipo de** dados exibe os tipos de dados pessoais detectados por corresponde à política e a quantidade de cada tipo. O gráfico de pizza ajuda a demonstrar visualmente se um determinado tipo de dados pessoais, por exemplo, números de seguro social ou números de cartão de crédito, é representado predominantemente nos cenários de risco que você está tentando identificar.

> [!TIP]
> Ao examinar holísticamente os locais, os tipos de dados e o número de usuários envolvidos em partidas de política, você pode ter um melhor senso sobre os tipos de treinamento e medidas de proteção de dados necessários para ajudar sua organização a proteger os dados pessoais que armazena.

### <a name="matched-items-tab"></a>Guia Itens correspondentes

A **guia Itens Correspondentes** exibe uma lista de todos os itens de conteúdo correspondentes a uma condição definida na política. Nessa exibição, você pode selecionar um item em sua linha para visualiza-lo na janela à direita da lista de itens.

Na janela de visualização, você encontrará as seguintes guias que fornecem detalhes sobre cada item:
- **Fonte**: exibe os dados pessoais que dispararam a correspondência.
- **Detalhes**: exibe o proprietário do conteúdo (usuário em sua organização) para o item, o local de Microsoft 365 do item, o número de tipos de dados pessoais dentro do item e os tipos de dados pessoais específicos.
- **Atividades de** arquivo: exibe qualquer rótulo ou classificação aplicado ao item.
- **Histórico de correção**: exibe informações sobre ações de correção executadas por usuários ou administradores no item.

## <a name="edit-a-policy"></a>Editar uma política

Você pode editar as configurações de uma política a qualquer momento, seja no modo de teste ou ativado. Você pode atualizar a maioria das configurações de política, incluindo colocar uma política de volta no modo de teste depois de a ter ativado. As únicas configurações que você não pode editar são o modelo de política e o nome da política.

Para editar uma política, siga as etapas abaixo:

1. No painel [Centro de conformidade do Microsoft 365](https://compliance.microsoft.com/), localize Priva Privacy Risk Management no painel de navegação esquerdo. No menu suspenso, selecione **Políticas**.

2. Selecione a política que você deseja editar de sua linha na página  Políticas, que abre a página de detalhes dessa política.

3. Na página de detalhes da política, selecione **o comando** Editar no canto superior direito da página. Essa ação levará você para a criação de política no Gerenciamento de Riscos de Privacidade.

4. Siga as etapas para acessar as configurações que você deseja alterar. Você pode editar todas as configurações, exceto o modelo de política e o nome da política. Selecione **Avançar** para avançar para cada próxima etapa.

5. Na página **Concluir** , examine suas configurações e selecione **Enviar** para salvar as alterações feitas.

## <a name="delete-a-policy"></a>Excluir uma política

Se você precisar remover uma política de Gerenciamento de Risco de Privacidade existente, localize-a na lista  na página Políticas, selecione o menu de ação (reticências verticais)  e escolha a ação Excluir política. Você também pode abrir a página de detalhes da **política e selecionar** Excluir no canto superior direito.

Você será solicitado a confirmar sua escolha antes que a exclusão seja final e a política seja removida permanentemente. A exclusão de uma política não afetará nenhum arquivo avaliado anteriormente pela política, e os problemas e alertas gerados pela política ainda serão **listados nas páginas Alertas** **e** Problemas.

## <a name="next-steps"></a>Próximas etapas

Depois que sua política estiver ativada e começar a gerar alertas, você desejará começar a entender quais riscos eles podem apresentar à sua organização. Saiba como gerenciar alertas, investigar eventos e executar ações de correção no Gerenciamento de Riscos de Privacidade visitando Investigar e [corrigir alertas](risk-management-alerts.md).

## <a name="legal-disclaimer"></a>Aviso de isenção de responsabilidade legal

[Aviso de isenção de responsabilidade legal da Microsoft Priva](priva-disclaimer.md)
