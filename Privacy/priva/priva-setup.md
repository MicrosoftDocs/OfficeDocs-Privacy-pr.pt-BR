---
title: Introdução ao Priva
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
- M365-priva-subject-rights-requests
- M365-priva-privacy-risk-management
search.appverid:
- MOE150
- MET150fcf
description: Saiba como configurar o Microsoft Priva para sua organização, definir funções e permissões e definir configurações importantes.
ms.openlocfilehash: 945cbfd2625be50cb89eeaa8fe09e0effaea79d5
ms.sourcegitcommit: 3c27ecf7c86c8a3db38cae8819fc090eed192b4f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2022
ms.locfileid: "65678208"
---
# <a name="get-started-with-priva"></a>Introdução ao Priva

Se você estiver pronto para começar a usar o Microsoft Priva ajudar sua organização a identificar e atenuar os riscos de privacidade, siga estas etapas para ajudar a configurar.

## <a name="confirm-subscriptions-and-licensing"></a>Confirmar assinaturas e licenciamento

Priva está disponível no [portal de conformidade do Microsoft Purview e pode](https://compliance.microsoft.com/) ser comprado por organizações com as seguintes licenças:

- Microsoft 365 E3, E5, A3, A5
- Office 365 E1, E3, E5, A1, A3, A5

Priva oferece opções de licenciamento para duas soluções diferentes: Gerenciamento de risco de privacidade Priva e Solicitações de direitos do titular Priva. Eles podem ser comprados individualmente ou juntos. Ao obter licenças para solicitações de direitos de entidade, você pode escolher a camada de licenciamento apropriada para quantas solicitações você precisa lidar. Você pode comprar solicitações adicionais a qualquer momento.

Para obter orientações de licenciamento detalhadas, confira as [orientações de licenciamento do Microsoft 365 para segurança e conformidade](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance#microsoft-priva).

> [!Note]
> Priva não está disponível para clientes moderados do Community (GCC) moderados, GCC alto ou do Departamento de Defesa (DoD).

### <a name="start-a-free-trial"></a>Comece uma avaliação gratuita

Use uma assinatura de avaliação gratuita para explorar todos os recursos e funcionalidades de ambas Priva soluções. Saiba como se inscrever para a avaliação [Priva teste](priva-trial.md).

## <a name="enable-the-microsoft-365-audit-log"></a>Habilitar o Microsoft 365 de auditoria

Microsoft 365 logs de auditoria são um resumo de todas as atividades em sua organização. As políticas de Gerenciamento de Riscos de Privacidade podem usar essas atividades para gerar insights de política.

Sua organização pode já ter os logs de auditoria ativados. Se você precisar começar a usá-los pela primeira vez, consulte Ativar ou desativar a pesquisa de [log](/microsoft-365/compliance/turn-audit-log-search-on-or-off) de auditoria para obter instruções passo a passo para ativar a auditoria. Após a ativação, será exibida uma mensagem informando que o log de auditoria está sendo preparado e que você poderá executar uma pesquisa dentro algumas horas quando a preparação estiver concluída. Você só precisa fazer essa ação uma vez. Para obter mais informações sobre como usar Microsoft 365 log de auditoria, consulte [Pesquisar o log de auditoria](/microsoft-365/compliance/search-the-audit-log-in-security-and-compliance).

## <a name="set-user-permissions-and-assign-roles"></a>Definir permissões de usuário e atribuir funções

Priva usa um modelo de permissão de RBAC (controle de acesso baseado em função). Somente usuários que recebem uma função podem acessar Priva e as ações permitidas por cada usuário são restritas por tipo de função.

O administrador global tem permissões para acessar Priva e atribuir outros usuários a funções. Eles podem entrar e definir permissões de usuário no [portal de conformidade do Microsoft Purview](https://compliance.microsoft.com/) para Priva. Para um início rápido, o grupo de função Gerenciamento de Privacidade tem permissões para acessar todos os recursos Priva. Esse grupo pode ser uma boa opção para organizações em que o mesmo indivíduo pode executar todas as tarefas. Outras funções de privacidade permitem que você tenha um controle mais granular e atribua usuários a recursos ou funções selecionados.

Para saber mais sobre grupos de funções e como conceder acesso, consulte Definir permissões de usuário e [atribuir funções no Priva](priva-permissions.md).

## <a name="start-finding-and-visualizing-your-data"></a>Comece a localizar e visualizar seus dados

Depois de entrar no Priva, você verá a página **Visão** geral. Esta página fornece insights dinâmicos sobre como os dados pessoais estão evoluindo em seu ambiente Microsoft 365 para ajudá-lo a identificar rapidamente problemas, identificar indicadores de risco e tomar medidas para corrigir problemas. Sua Visão geral deve ser preenchida com insights iniciais nas primeiras 24 horas após a inscrição. À medida que você continuar usando Priva, a página de visão geral será atualizada para continuar a fornecer informações atuais.

Para obter mais informações sobre seus dados ao longo do  tempo, sua página de perfil de dados fornecerá mais visualizações e análises e fornecerá uma visão holística dos dados da sua organização por localização geográfica e por Microsoft 365 local.

Para saber mais sobre essas páginas, consulte [Localizar e visualizar dados pessoais Priva](priva-data-profile.md).

## <a name="start-managing-risks-with-default-policies"></a>Começar a gerenciar riscos com políticas padrão

O Gerenciamento de Riscos de Privacidade começará a avaliar seus dados e fornecerá uma olhada nos principais cenários de risco para minimização de dados, superexposição de dados e transferências de dados. Essas políticas são ativadas por padrão. Você pode usar essas políticas para avaliar onde estão seus riscos e, em seguida, ativar as notificações por email do usuário para que os usuários acionem os problemas e guiem a correção desses riscos. Além disso, você pode criar e personalizar suas próprias políticas com base nos modelos de política fornecidos. Você pode adaptar suas políticas para atender às necessidades de conformidade legal e regulatória da sua organização, conforme pode ser identificado em consulta com o advogado. Para saber mais, confira [Criar políticas no Gerenciamento de Riscos de Privacidade](risk-management-policies.md).

## <a name="get-started-with-subject-rights-requests"></a>Introdução com solicitações de direitos de entidade

Solicitações de direitos do titular Priva automatiza o processo de cumprimento de solicitação de direitos de entidade, fornecendo acesso fácil a dados e fluxos de trabalho personalizáveis que se ajustam aos processos de negócios existentes. Você pode encontrar facilmente os dados relevantes, examinar as descobertas e produzir relatórios. Ao longo do caminho, você pode colaborar com segurança com outros especialistas em sua organização para concluir a solicitação de direitos do assunto. Você também pode gerenciar e personalizar seus fluxos de trabalho de negócios com modelos internos. Para saber mais sobre como usar esses recursos, [consulte Saiba mais sobre Solicitações de direitos do titular Priva](subject-rights-requests.md).

## <a name="priva-availability"></a>Priva disponibilidade

Microsoft Priva está disponível para clientes em todo o mundo. Se sua organização provisionou seu locatário em um dos data centers locais listados abaixo para atender aos requisitos de residência de dados, as soluções do Priva não estarão disponíveis para você na navegação à esquerda do portal de conformidade do Microsoft Purview:

- Noruega
- Polônia
- Catar
- Cingapura
- África do Sul
- Coreia do Sul
- Espanha
- Suécia
- Suíça
- Emirados Árabes Unidos

## <a name="legal-disclaimer"></a>Aviso de isenção de responsabilidade legal

[Microsoft Priva aviso de isenção de responsabilidade legal](priva-disclaimer.md)
