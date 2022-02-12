---
title: Definir configurações do Priva
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
- MET150
description: Saiba mais sobre as opções de configurações globais do Microsoft Priva.
ms.openlocfilehash: a621102db2a421cbda0c8d7298c30cede102f13e
ms.sourcegitcommit: 875a7df5c2562eac6395e71c5bf83ba1d0a067d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62768435"
---
# <a name="configure-priva-settings"></a>Definir configurações do Priva

Você pode gerenciar as configurações do Microsoft Priva selecionando o ícone de engrenagem no canto superior direito da tela. As opções aqui permitem definir preferências de alto nível e personalizar propriedades principais. Esta página fornece uma visão geral das principais Configurações categorias.

## <a name="anonymization"></a>Anonimização

Esse recurso permite que você mostre versões anonimizadas de nomes de usuário nos recursos de Gerenciamento de Risco de Privacidade para usuários em determinadas funções. Ele substituirá nomes de exibição identificáveis por um rótulo genérico para ajudar a mascarar as identidades dos usuários ao revisar dados confidenciais. Essa opção não se aplica à solução Solicitações de Direitos de Assunto.

## <a name="user-notification-emails"></a>Emails de notificação do usuário  

As políticas no Gerenciamento de Riscos de Privacidade permitem definir parâmetros para avaliar possíveis riscos de privacidade em seu ambiente. Quando detectamos uma combinação de política, o Gerenciamento de Risco de Privacidade pode enviar um email para seus usuários com recomendações sobre ações corretivas a tomar e um link para treinamento de privacidade. Em Configurações, você pode habilitar ou desabilitar o recurso de notificação de email do Gerenciamento de Risco de Privacidade como um todo. Se o recurso de notificação estiver desativado Configurações, todos os emails serão desabilitados. Para saber mais sobre políticas, consulte [Create policies in Privacy Risk Management](risk-management-policies.md).

## <a name="teams-collaboration"></a>Colaboração em equipes  

Integre Microsoft Teams recursos com Solicitações de Direitos de Assunto Priva para aprimorar a colaboração com as partes interessadas. Sempre que uma solicitação de direitos de assunto é criada, uma equipe associada será criada em Teams. Os usuários podem ser adicionados a uma equipe na guia Colaboradores da solicitação. Para saber mais sobre solicitações de direitos de assunto, [consulte Learn about Priva Subject Rights Requests](subject-rights-requests.md).

## <a name="data-matching"></a>Correspondência de dados  

Use esta seção para carregar esquemas de dados que descrevem atributos de seus titulares de dados, que ajudarão a identificar o titular de dados correto ao pesquisar dados pessoais em seu ambiente Microsoft 365. Esquemas e pacotes de regras são criados e carregados no formato XML. Em **Upload de dados pessoais**, você também pode enviar dados pessoais que corresponde a um esquema fornecido. Você pode criar e carregar seu próprio arquivo ou optar por carregar dados pessoais do Azure. Para saber mais sobre solicitações de direitos de assunto, [consulte Learn about Priva Subject Rights Requests](subject-rights-requests.md).

## <a name="data-retention-periods"></a>Períodos de retenção de dados

Essa configuração está relacionada a Solicitações de Direitos de Assunto Priva. Ele permite controlar sua preferência por quanto tempo deseja reter dados coletados e relatórios gerados após o fechamento da solicitação. Isso pode ser definido como 30 ou 90 dias e se aplica a todas as solicitações de direitos de assunto que você criar. Recomendamos verificar se os períodos de retenção de dados estão em conformidade com as políticas e obrigações legais da sua organização. Saiba mais sobre como [definir a retenção de dados para solicitações de direitos de assunto](subject-rights-requests-reports.md#manage-data-retention).

## <a name="data-review-tags"></a>Marcas de revisão de dados

Gerencie as marcas que você usará para marcar arquivos recuperados em uma solicitação de direitos de assunto. Essas marcas podem ser usadas para indicar conteúdo que precisará de mais atenção, como conteúdo que pode precisar ser excluído manualmente. Nesta seção de configurações, você pode editar os nomes e descrições para marcas personalizadas. Você também pode editar descrições de marca para as marcas criadas fornecidas pelo sistema. Os nomes das marcas do sistema não podem ser alterados. Para saber mais sobre solicitações de direitos de assunto, consulte [Review data for a subject rights request](subject-rights-requests-data-review.md#step-3-review-data).
