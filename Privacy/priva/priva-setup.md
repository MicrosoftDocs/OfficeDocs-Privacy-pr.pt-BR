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
ms.openlocfilehash: e88145dc999e210f36a8dc82e1bc9996bc15bb88
ms.sourcegitcommit: 09ecdaded9a9f8f79587f2acb978dc53b83e5c01
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/19/2022
ms.locfileid: "64930552"
---
# <a name="get-started-with-priva"></a>Introdução ao Priva

Se você estiver pronto para começar a usar o Microsoft Priva para obter assistência na identificação e redução de riscos de privacidade, siga estas etapas para configurar os pré-requisitos e começar a explorar os insights de privacidade.

## <a name="step-1-confirm-subscriptions-and-licensing"></a>Etapa 1: Confirmar assinaturas e licenciamento

Priva está disponível no [portal de conformidade do Microsoft Purview](https://compliance.microsoft.com/) e pode ser comprado por organizações com as seguintes licenças:

- Microsoft 365 E3, E5, A3, A5
- Office 365 E1, E3, E5, A1, A3, A5

Priva oferece opções de licenciamento para duas soluções diferentes: Priva Privacy Risk Management e Priva Subject Rights Requests. Eles podem ser comprados individualmente ou juntos. Ao obter licenças para solicitações de direitos de entidade, você pode escolher a camada de licenciamento apropriada para quantas solicitações você precisa lidar. Você pode comprar solicitações adicionais a qualquer momento.

Para obter orientações de licenciamento detalhadas, confira as [orientações de licenciamento do Microsoft 365 para segurança e conformidade](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance#microsoft-priva).

> [!Note]
> Priva não está disponível para clientes do Community (GCC) Moderado, GCC Alto ou Departamento de Defesa (DoD).

### <a name="get-free-trial-license"></a>Obter licença de avaliação gratuita

Uma licença de avaliação gratuita está disponível para começar a usar Priva. Para saber mais sobre elegibilidade e como ingressar, confira [Saiba mais sobre a avaliação gratuita priva](priva-trial.md).

## <a name="step-2-enable-the-microsoft-365-audit-log"></a>Etapa 2: Habilitar o Microsoft 365 de auditoria

Microsoft 365 logs de auditoria são um resumo de todas as atividades em sua organização. As políticas de Gerenciamento de Riscos de Privacidade podem usar essas atividades para gerar insights de política.

Sua organização pode já ter os logs de auditoria ativados. Se você precisar começar a usá-los pela primeira vez, consulte Ativar ou desativar a pesquisa de [log](/microsoft-365/compliance/turn-audit-log-search-on-or-off) de auditoria para obter instruções passo a passo para ativar a auditoria. Após a ativação, será exibida uma mensagem informando que o log de auditoria está sendo preparado e que você poderá executar uma pesquisa dentro algumas horas quando a preparação estiver concluída. Você só precisa fazer essa ação uma vez. Para obter mais informações sobre como usar Microsoft 365 log de auditoria, consulte [Pesquisar o log de auditoria](/microsoft-365/compliance/search-the-audit-log-in-security-and-compliance).

## <a name="step-3-set-user-permissions-and-assign-roles"></a>Etapa 3: Definir permissões de usuário e atribuir funções

Priva usa um modelo de permissão de RBAC (controle de acesso baseado em função). Somente os usuários que recebem uma função podem acessar Priva e as ações permitidas por cada usuário são restritas por tipo de função.

Seu administrador global tem permissões para acessar Priva e atribuir outros usuários a funções. Eles podem entrar e definir permissões de usuário no [portal de conformidade do Microsoft Purview](https://compliance.microsoft.com/) para Priva. Para um início rápido, o grupo de função Gerenciamento de Privacidade tem permissões para acessar todos os recursos de Priva. Esse grupo pode ser uma boa opção para organizações em que o mesmo indivíduo pode executar todas as tarefas. Outras funções de privacidade permitem que você tenha um controle mais granular e atribua usuários a recursos ou funções selecionados.

Para saber mais sobre grupos de funções e como conceder acesso, consulte Definir permissões de usuário [e atribuir funções em Priva](priva-permissions.md).

## <a name="step-4-start-finding-and-visualizing-your-data"></a>Etapa 4: Começar a localizar e visualizar seus dados

Depois de entrar no Priva, você verá a página **Visão** geral. Esta página fornece insights dinâmicos sobre como os dados pessoais estão evoluindo em seu ambiente Microsoft 365 para ajudá-lo a identificar rapidamente problemas, identificar indicadores de risco e tomar medidas para corrigir problemas. Sua Visão geral deve ser preenchida com insights iniciais nas primeiras 24 horas após a inscrição. À medida que você continuar a usar Priva, a página de visão geral será atualizada para continuar a fornecer informações atuais.

Para obter mais informações sobre seus dados ao longo do  tempo, sua página de perfil de dados fornecerá mais visualizações e análises e fornecerá uma visão holística dos dados da sua organização por localização geográfica e por Microsoft 365 local.

Para saber mais sobre essas páginas, [consulte Localizar e visualizar dados pessoais em Priva](priva-data-profile.md).

## <a name="step-5-start-managing-risks-with-default-policies"></a>Etapa 5: Começar a gerenciar riscos com políticas padrão

O Gerenciamento de Riscos de Privacidade começará a avaliar seus dados e fornecerá uma olhada nos principais cenários de risco para minimização de dados, superexposição de dados e transferências de dados. Essas políticas são ativadas por padrão. Você pode usar essas políticas para avaliar onde estão seus riscos e, em seguida, ativar as notificações por email do usuário para que os usuários acionem os problemas e guiem a correção desses riscos. Além disso, você pode criar e personalizar suas próprias políticas com base nos modelos de política fornecidos. Você pode adaptar suas políticas para atender às necessidades de conformidade legal e regulatória da sua organização, conforme pode ser identificado em consulta com o advogado. Para saber mais, confira [Criar políticas no Gerenciamento de Riscos de Privacidade](risk-management-policies.md).

## <a name="step-6-get-started-with-subject-rights-requests"></a>Etapa 6: Introdução com solicitações de direitos de entidade

Priva Subject Rights Requests automatiza o processo de cumprimento de solicitação de direitos de entidade, fornecendo acesso fácil a dados e fluxos de trabalho personalizáveis que se ajustam aos processos de negócios existentes. Você pode encontrar facilmente os dados relevantes, examinar as descobertas e produzir relatórios. Ao longo do caminho, você pode colaborar com segurança com outros especialistas em sua organização para concluir a solicitação de direitos do assunto. Você também pode gerenciar e personalizar seus fluxos de trabalho de negócios com modelos internos. Para saber mais sobre como usar esses recursos, consulte [Saiba mais sobre solicitações de direitos de assunto priva](subject-rights-requests.md).

## <a name="legal-disclaimer"></a>Aviso de isenção de responsabilidade legal

[Aviso de isenção de responsabilidade legal da Microsoft Priva](priva-disclaimer.md)
