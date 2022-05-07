---
title: Investigar e corrigir alertas no Gerenciamento de Riscos de Privacidade
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
description: Saiba como gerenciar alertas e problemas gerados por partidas de política no Gerenciamento de Riscos de Privacidade da Microsoft Priva.
ms.openlocfilehash: a770a7b8d77e2d7792fc4ea8c68914dc62b48a27
ms.sourcegitcommit: 0e68501654f702d8b8b694ae696bb8bd7fa7cea6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/07/2022
ms.locfileid: "65268324"
---
# <a name="investigate-and-remediate-alerts-in-privacy-risk-management"></a>Investigar e corrigir alertas no Gerenciamento de Riscos de Privacidade

O Microsoft Priva pode ajudar a fornecer visibilidade sobre descobertas importantes de suas políticas de superexposição de dados, minimização de dados ou transferência de dados. Na solução de Gerenciamento de Riscos de Privacidade, os administradores podem examinar **alertas sobre** o conteúdo que corresponde às suas condições de política. A revisão de alertas permite identificar casos que precisam de acompanhamento. Você pode fazer isso criando **problemas**. Os problemas oferecem aos usuários uma maneira estruturada de revisar o conteúdo, atribuir a gravidade do problema e trabalhar de forma colaborativa para corrigir problemas.

Se sua política tiver sido configurada para enviar notificações aos usuários, os proprietários de conteúdo também poderão executar determinadas ações corretivas diretamente desses emails ou de Teams. Para saber mais, confira [Enviar notificações do usuário no Gerenciamento de Riscos de Privacidade](risk-management-notifications.md).

## <a name="view-current-alerts-and-issues"></a>Exibir alertas e problemas atuais

A página **Visão geral da** Priva fornece uma visão geral das descobertas recentes com atualizações sobre as principais áreas de preocupação, como as políticas com mais correspondentes e seus alertas de política ativos no momento. Para saber mais sobre as informações que essa exibição fornece, [consulte Localizar e visualizar dados pessoais em Priva](priva-data-profile.md).

Você também pode acessar visualizações e detalhes sobre seus alertas e problemas por meio da página **principal políticas** . Selecione **Exibir alertas e** **exibir problemas** para ver detalhes.

## <a name="manage-alerts"></a>Gerenciar alertas

Para avaliar seus alertas ativos e especificar quais exigem acompanhamento, acesse a **página Alertas** . Ele fornece uma lista filtável de alertas gerados por suas políticas. Você pode revisá-los individualmente para determinar as circunstâncias em que elas foram disparadas.

Selecionar qualquer alerta abrirá um painel de sobreposição com detalhes adicionais, como o número de itens correspondentes e a gravidade, conforme julgado pelas configurações de política. Na guia **Conteúdo** , você pode examinar quais arquivos estão envolvidos nesse alerta. Essas informações podem fornecer informações adicionais sobre o evento específico que disparou o alerta, onde os arquivos residem e quais tipos de dados pessoais estão envolvidos. Os gatilhos para alertas são determinados pelas condições específicas de cada política. Por exemplo, um alerta pode ser disparado em uma política de transferência de dados se Priva detectar uma transferência entre os departamentos ou regiões especificados da política.

Depois de avaliar qualquer alerta na lista, você pode selecionar Criar  problema para solicitar mais investigação e ação por seus usuários. Você será solicitado a nomear o problema e adicionar comentários relevantes para o contexto. Você também poderá ignorar alertas aqui se eles não exigirem um acompanhamento.

## <a name="manage-issues"></a>Gerenciar problemas

Os problemas são criados por administradores ao avaliar alertas sobre as correspondentes à política. Para acompanhar e resolver as preocupações indicadas, os usuários podem visitar a **página** Problemas. A partir daqui, você pode examinar problemas individuais, investigar as condições de provocação, examinar os dados e tomar as etapas necessárias para fechar o caso.

Esta página fornece uma lista de todos os problemas abertos. Eles são listados por nome e classificados por gravidade para ajudá-lo a priorizar casos, incluindo categorias altas, médias e baixas, juntamente com categorias não atribuídas. Selecione qualquer problema na lista para examinar seu conteúdo e tomar medidas para resolvê-lo. Você pode fornecer a problemas não atribuídos uma classificação de severidade durante a revisão.

### <a name="review-issue-details"></a>Examinar detalhes do problema

As páginas de detalhes do problema ajudam a orientar você pelo processo de lidar com os riscos de privacidade identificados e lidar com os arquivos indicados.

As guias nas páginas de detalhes do problema fornecem informações sobre os alertas e o conteúdo associados, incluindo:

- **Visão** geral: mostra informações essenciais sobre o problema. Veja o status atual do problema e as próximas ações recomendadas a serem tomadas. Você também pode ver uma visão geral do conteúdo, da política associada, dos detalhes sobre o alerta e da linha do tempo. A linha do tempo mostrará onde você está recuperando conteúdo. O conteúdo baixado será mantido temporariamente para revisão.
- **Alertas**: uma lista detalhada de alertas associados ao problema.
- **Conteúdo**: uma lista filtável de itens de conteúdo associados. Selecione qualquer item para exibir detalhes sobre ele, incluindo todas as atividades que ocorreram e seu histórico de correção, se alguém já tiver feito ações em Priva para gerenciar os dados. Você também pode optar por executar novas ações de correção.
- **Observações**: selecione para adicionar ou exibir as anotações da sua equipe sobre o problema.
- **Colaboradores**: exiba e gerencie a lista de colaboradores que podem contribuir para resolver esse problema.

### <a name="share-the-issue"></a>Compartilhar o problema

Adicionar pessoas como colaboradores permite que você compartilhe o problema com membros adicionais da sua empresa por meio de um canal seguro do Microsoft Teams, email da empresa ou compartilhando um link diretamente para a página do problema em Priva. Essas opções estão disponíveis no botão **Compartilhar** . Ao compartilhar via Teams, você será solicitado a selecionar entre as equipes disponíveis em sua organização, selecionar o canal específico e deixar uma mensagem sobre o problema, que será compartilhada com o canal especificado.

## <a name="review-content-and-remediate-issues"></a>Examinar o conteúdo e corrigir problemas

Para examinar o conteúdo associado a um problema, escolha a ação Revisar **conteúdo** , se solicitado ou abra a **guia** Conteúdo. Selecione qualquer arquivo na lista para exibi-lo por completo. Aqui, você pode ver detalhes sobre o arquivo, todas as atividades no registro e seu histórico de correção, se as etapas anteriores foram executadas para gerenciar esse arquivo. Selecione **Corrigir para** executar uma ou mais das ações listadas abaixo.

- **Notificar o** proprietário: notifique o proprietário do conteúdo sobre o problema detectado.

- **Aplicar rótulo de retenção**: adicione um rótulo para este item que possa reter, excluir ou reter e, em seguida, excluí-lo após um tempo especificado. [Saiba mais sobre rótulos de retenção](/microsoft-365/compliance/retention).

- **Aplicar rótulo de confidencialidade**: adicione um rótulo para este item que identifique sua confidencialidade e, opcionalmente, adicione proteção que inclua marcações visuais e criptografia. [Saiba mais sobre rótulos de confidencialidade](/microsoft-365/compliance/sensitivity-labels).

- **Marcar como não uma correspondência**: identifique um resultado de pesquisa como um falso positivo para remover o item de conteúdo da consideração.

- **Excluir** (somente para políticas de minimização de dados): use essa opção para uma exclusão reversível dos dados. O item é movido para a pasta de itens excluídos ou para a lixeira (Exchange, SharePoint, OneDrive) ou excluído com uma opção para recuperar (Teams mensagens). A exclusão pode ser revertida dentro de um período de tempo definido, dependendo das configurações do serviço.

- **Torne privado** (somente para políticas de sobreexposure e transferência de dados): remova o acesso aberto para este item de conteúdo.

Cada opção solicitará que você deixe comentários e quaisquer outras informações de suporte necessárias para o proprietário do conteúdo antes de confirmar sua escolha.

Depois que todas as etapas de correção tiverem sido executadas (incluindo as ações que você julgar aconselhável, além das opções disponíveis em Priva) e o problema estiver pronto para ser fechado, use o  botão Resolver e adicione seus comentários finais antes de enviá-lo.

## <a name="legal-disclaimer"></a>Aviso de isenção de responsabilidade legal

[Aviso de isenção de responsabilidade legal da Microsoft Priva](priva-disclaimer.md)
