---
title: Compreender alertas e problemas no gerenciamento de privacidade
f1.keywords:
- CSH
ms.author: v-jgriffee
author: jmgriffee
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- M365-security-compliance
- M365-privacy-management
search.appverid:
- MOE150
- MET150
description: Saiba como gerenciar alertas e problemas gerados por políticas no gerenciamento de privacidade.
ms.openlocfilehash: a5dcdc78484f664249578475326ad9d39c1cd381
ms.sourcegitcommit: 85e085eb17af8b4efd1f45207445e1b3c3679600
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/19/2021
ms.locfileid: "60478079"
---
# <a name="understand-policy-alerts-and-issues-in-privacy-management"></a>Entender os alertas de política e os problemas no gerenciamento de privacidade

O gerenciamento de privacidade pode ajudar a fornecer visibilidade sobre descobertas importantes de suas políticas de sobreexposure de dados, minimização de dados ou transferência de dados. Na solução de gerenciamento de privacidade, os administradores podem revisar **alertas sobre** o conteúdo que corresponde às suas condições de política. A revisão de alertas permite identificar casos que precisam de acompanhamento. Você pode fazer isso criando **problemas.** Os problemas dão aos usuários uma maneira estruturada de revisar o conteúdo, atribuir a gravidade do problema e trabalhar colaborativamente para resolver problemas.

Se sua política tiver sido configurada para enviar notificações aos usuários, os proprietários de conteúdo também poderão tomar determinadas ações corretivas diretamente desses emails ou de Teams. Para saber mais, confira [Enviar notificações de política de usuários.](privacy-management-policies-notifications.md)

## <a name="view-current-alerts-and-issues"></a>Exibir alertas e problemas atuais

A página  Visão geral do gerenciamento de privacidade fornece uma visão sobre as descobertas recentes com atualizações sobre as principais áreas de preocupação, como as políticas com mais combinações e seus alertas de política ativos no momento. Para saber mais sobre as informações que essa exibição fornece, consulte [Find and visualize your data](privacy-management-data-profile.md).

Você também pode acessar visualizações e detalhes sobre seus alertas e problemas por meio da página **principal Políticas.** Selecione **Exibir alertas e** Exibir **problemas** para ver detalhes.

## <a name="manage-alerts"></a>Gerenciar alertas

Para avaliar seus alertas ativos e especificar quais exigem acompanhamento, acesse a página **Alertas.** Ele fornece uma lista filtrada de alertas gerados por suas políticas. Você pode revisá-los individualmente para determinar as circunstâncias em que elas foram disparadas.

A seleção de qualquer alerta abrirá um painel de sobrevoo com detalhes adicionais, como o número de itens correspondentes e a gravidade conforme as configurações de política. Na guia **Conteúdo,** você pode revisar quais arquivos estão envolvidos neste alerta. Essas informações podem fornecer informações adicionais sobre o evento específico que disparou o alerta, onde os arquivos residem e quais tipos de dados pessoais estão envolvidos. Os gatilhos para alertas são determinados pelas condições específicas de cada política. Por exemplo, um alerta pode ser disparado em uma política de transferência de dados se o gerenciamento de privacidade detectar uma transferência entre os departamentos ou regiões especificados da política.

Depois de avaliar qualquer alerta na lista, você pode selecionar **Criar problema** para solicitar mais investigação e ação por parte dos usuários. Você será solicitado a nomear o problema e adicionar quaisquer comentários relevantes para o contexto. Você também pode descartar alertas aqui se eles não exigirem um acompanhamento.

## <a name="manage-issues"></a>Gerenciar problemas

Os problemas são criados pelos administradores ao avaliar alertas sobre as combinações de política. Para acompanhar e resolver as preocupações indicadas, os usuários podem visitar a página **Problemas.** A partir daqui, você pode revisar problemas individuais, investigar as condições instigantes, revisar os dados e tomar as etapas necessárias para fechar o caso.

Esta página fornece uma lista de todos os problemas abertos. Eles são listados por nome e organizados por gravidade para ajudar você a priorizar casos, incluindo categorias altas, médias e baixas, juntamente com não atribuídos. Selecione qualquer problema na lista para revisar seu conteúdo e tomar medidas para resolvê-lo. Você pode dar a problemas não atribuídos uma classificação de gravidade durante a revisão.

### <a name="review-issue-details"></a>Revisar detalhes do problema

Páginas de detalhes de edição ajudam a orientá-lo pelo processo de endereçamento dos riscos de privacidade identificados e manipulação dos arquivos indicados.

As guias nas páginas de detalhes do problema fornecem informações sobre os alertas e conteúdo associados, incluindo:

- **Visão** geral : mostra informações essenciais sobre o problema. Consulte o status atual do problema e as próximas ações recomendadas a seguir. Você também pode ver uma visão geral do conteúdo, da política associada, dos detalhes sobre o alerta e da linha do tempo. A linha do tempo mostrará onde você está recuperando conteúdo. O conteúdo baixado será mantido temporariamente para revisão.
- **Alertas**: uma lista detalhada de alertas associados ao problema.
- **Conteúdo**: uma lista filtrada de itens de conteúdo associados. Selecione qualquer item para exibir detalhes sobre ele, incluindo todas as atividades que ocorreram e seu histórico de correção, se alguém já tiver tomado ações no gerenciamento de privacidade para gerenciar os dados. Você também pode optar por realizar novas ações de correção.
- **Observações**: selecione adicionar ou exibir quaisquer anotações para sua equipe sobre o problema.
- **Colaboradores**: Exibir e gerenciar a lista de colaboradores que podem contribuir para resolver esse problema.

### <a name="share-the-issue"></a>Compartilhar o problema

Adicionar pessoas como colaboradores permite compartilhar o problema com membros adicionais da sua empresa por meio de um canal seguro Microsoft Teams, email da empresa ou compartilhando um link diretamente para a página do problema no gerenciamento de privacidade. Essas opções estão disponíveis no botão **Compartilhar.** Ao compartilhar por Teams, você será solicitado a selecionar entre as equipes disponíveis em sua organização, selecionar o canal específico e deixar uma mensagem sobre o problema, que será compartilhada com o canal especificado.

## <a name="review-content-and-remediate-issues"></a>Revisar conteúdo e resolver problemas

Para revisar o conteúdo associado a um problema, escolha a ação Revisar **conteúdo** se solicitado ou abra a **guia** Conteúdo. Selecione qualquer arquivo na lista para exibi-lo na íntegra. Aqui você pode ver detalhes sobre o arquivo, todas as atividades no registro e seu histórico de correção, se as etapas anteriores foram tomadas para gerenciar esse arquivo.

Use o **botão Correção para** tomar suas próprias decisões de tratamento de dados para esse conteúdo no gerenciamento de privacidade. Selecionar o botão permite escolher entre uma ou mais ações de correção. As opções são:

**Todas as políticas**

- **Notificar proprietário**: Notificar o proprietário do conteúdo sobre o problema detectado.
- **Aplicar rótulo de retenção**: adicione um rótulo sobre a retenção de dados para este item. [Saiba mais sobre rótulos de retenção.](/microsoft-365/compliance/create-apply-retention-labels)
- **Aplicar rótulo de sensibilidade**: adicione um rótulo sobre a sensibilidade dos dados deste item. [Saiba mais sobre rótulos de sensibilidade.](/microsoft-365/compliance/sensitivity-labels)
- **Marcar como não uma combinação**: Identifique um resultado de pesquisa como um falso positivo para remover o item de conteúdo da consideração.

**Minimização de dados**

- **Excluir**: use essa opção para uma exclusão suave dos dados. O conteúdo é movido para a pasta de itens excluídos ou para a lixeira (Exchange, SharePoint, OneDrive) ou excluído com uma opção de recuperação (Teams mensagens). A exclusão pode ser revertida dentro de um período de tempo definido, dependendo das configurações do serviço.

**Sobreexposure de dados e transferência de dados**

- **Tornar privado**: Remover o acesso aberto para este item de conteúdo.

Cada opção solicitará que você deixe comentários e quaisquer outras informações de suporte necessárias para o proprietário do conteúdo antes de confirmar sua escolha.

Depois que todas as etapas de correção foram tomadas (incluindo todas as ações que você considera aconselháveis, além das opções disponíveis para você no gerenciamento de privacidade) e o problema está pronto para ser fechado, use o botão **Resolver** e adicione seus comentários finais antes de enviar.

## <a name="legal-disclaimer"></a>Aviso de isenção de responsabilidade legal

[Aviso de isenção de responsabilidade legal de gerenciamento de privacidade](privacy-management-disclaimer.md)
