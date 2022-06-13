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
description: Saiba mais sobre as opções de configurações globais para Microsoft Priva.
ms.openlocfilehash: a6f2fe55600d6cc3018c9d15f05a6d9e459a1486
ms.sourcegitcommit: 3c83e8133a5a71f4e1d76a0b2981ab3ec9cd6602
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/13/2022
ms.locfileid: "66046595"
---
# <a name="configure-priva-settings"></a>Definir configurações do Priva

Você pode gerenciar as configurações para Microsoft Priva selecionando o ícone de engrenagem no canto superior direito da tela. As opções aqui permitem que você defina preferências de alto nível e personalize as propriedades de chave. Esta página fornece uma visão geral das principais Configurações categorias.

## <a name="anonymization"></a>Anonimização

Você pode mostrar versões anônimas de nomes de usuário nos recursos de Gerenciamento de Risco de Privacidade para usuários em determinadas funções. O recurso de anonimização substitui nomes de exibição identificáveis por um rótulo genérico para ajudar a mascarar as identidades dos usuários ao revisar dados confidenciais. Essa opção não se aplica à solução Solicitações de Direitos de Entidade.

## <a name="user-notification-emails"></a>Emails de notificação do usuário  

As políticas no Gerenciamento de Riscos de Privacidade permitem que você defina parâmetros para avaliar possíveis riscos de privacidade em seu ambiente. Quando uma correspondência de política é detectada, o Gerenciamento de Riscos de Privacidade pode enviar um email aos usuários com recomendações sobre ações corretivas a serem tomadas e um link para treinamento de privacidade. No **Configurações**, você pode habilitar ou desabilitar a funcionalidade de notificação por email do Gerenciamento de Riscos de Privacidade como um todo. Se a funcionalidade de notificação estiver desativada Configurações, todos os emails serão desabilitados. Para saber mais sobre políticas, consulte [Criar políticas no Gerenciamento de Riscos de Privacidade](risk-management-policies.md).

## <a name="teams-collaboration"></a>Colaboração em equipes  

Integre Microsoft Teams recursos com o Solicitações de direitos do titular Priva para aprimorar a colaboração com os stakeholders. Marcar a caixa de seleção para ativar Microsoft Teams para solicitações de direitos **de entidade** criará automaticamente um canal Teams associado para cada solicitação. Os usuários podem ser adicionados Teams canal da guia **Colaboradores da** solicitação.

Ativar esse recurso aplicará Teams a todas as solicitações. Desmarcar a caixa desativará esses recursos para todas as solicitações. Saiba mais sobre a [colaboração durante o processo de revisão de dados](subject-rights-requests-data-review.md#collaboration-for-data-review).

## <a name="data-matching"></a>Correspondência de dados  

Use esta seção para carregar esquemas de dados que descrevem atributos de seus titulares de dados, que ajudarão a identificar o assunto de dados correto ao pesquisar dados pessoais em seu ambiente Microsoft 365 dados. Esquemas e pacotes de regras são criados e carregados no formato XML. Em **Upload de dados pessoais**, você também pode enviar dados pessoais que correspondam a um esquema fornecido. Você pode criar e carregar seu próprio arquivo ou optar por carregar dados pessoais do Azure. Saiba mais sobre a [correspondência de dados para solicitações de direitos de entidade](subject-rights-requests-data-match.md).

## <a name="data-retention-periods"></a>Períodos de retenção de dados

Essa configuração está relacionada ao Solicitações de direitos do titular Priva. Ele permite que você controle sua preferência por quanto tempo deseja reter os dados coletados e os relatórios gerados após o fechamento da solicitação. Isso pode ser definido como 30 ou 90 dias e se aplica a todas as solicitações de direitos de entidade que você criar. Recomendamos verificar se os períodos de retenção de dados estão em conformidade com as políticas e obrigações legais da sua organização. Saiba mais sobre a [retenção de dados para solicitações de direitos de entidade](subject-rights-requests-reports.md#retention-periods-for-reports-and-data).

## <a name="data-review-tags"></a>Marcas de revisão de dados

As marcas de revisão de dados podem ser usadas para marcar itens de conteúdo recuperados em uma solicitação de direitos de entidade. Essa área de configurações permite que você gerencie suas marcas. Priva fornece três marcas padrão: **Acompanhamento**, **Exclusão** e **Atualização**. Esses nomes de marca não podem ser editados, mas você pode fornecer uma descrição para essas marcas que sejam significativas para sua organização.

Priva também fornece duas marcas personalizadas que você pode nomear e definir para uso da sua organização. Você os verá listados como **Marca Personalizada 1** e **Marca Personalizada 2** até editar os nomes.

Siga as etapas abaixo para editar nomes de marca e descrições:

- Na página Priva **Configurações**, selecione Marcas **de revisão de dados**.
- Localize a marca na lista que você deseja editar e selecione o **ícone** Editar lápis ao lado de seu nome.
- No painel de submenu, faça suas edições nos campos disponíveis. Para marcas do sistema, você só pode editar a descrição. Para marcas personalizadas, você pode editar o nome e a descrição.
- Quando terminar, selecione Enviar **para** salvar suas alterações.

As configurações de marca se aplicam a todas as solicitações de direitos de entidade.

Saiba mais sobre [como aplicar marcas ao revisar dados para uma solicitação de direitos de entidade](subject-rights-requests-data-review.md#apply-tags).