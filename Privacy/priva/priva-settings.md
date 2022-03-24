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
ms.openlocfilehash: 1cbb508d8c1dd98dfa846595d81e8aaeecdbaeb4
ms.sourcegitcommit: 02921b2dd438a517191522567908046b136a89e2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63758420"
---
# <a name="configure-priva-settings"></a>Definir configurações do Priva

Você pode gerenciar as configurações do Microsoft Priva selecionando o ícone de engrenagem no canto superior direito da tela. As opções aqui permitem definir preferências de alto nível e personalizar propriedades principais. Esta página fornece uma visão geral das principais Configurações categorias.

## <a name="anonymization"></a>Anonimização

Você pode mostrar versões anonimizadas de nomes de usuário nos recursos de Gerenciamento de Riscos de Privacidade para usuários em determinadas funções. O recurso de anonimização substitui nomes de exibição identificáveis por um rótulo genérico para ajudar a mascarar as identidades dos usuários ao revisar dados confidenciais. Essa opção não se aplica à solução Solicitações de Direitos de Assunto.

## <a name="user-notification-emails"></a>Emails de notificação do usuário  

As políticas no Gerenciamento de Riscos de Privacidade permitem definir parâmetros para avaliar possíveis riscos de privacidade em seu ambiente. Quando uma combinação de política é detectada, o Gerenciamento de Riscos de Privacidade pode enviar um email para seus usuários com recomendações sobre ações corretivas a tomar e um link para treinamento de privacidade. Em **Configurações**, você pode habilitar ou desabilitar o recurso de notificação de email do Gerenciamento de Risco de Privacidade como um todo. Se o recurso de notificação estiver desativado Configurações, todos os emails serão desabilitados. Para saber mais sobre políticas, consulte [Create policies in Privacy Risk Management](risk-management-policies.md).

## <a name="teams-collaboration"></a>Colaboração em equipes  

Integre Microsoft Teams com Solicitações de Direitos de Titulares priva para aprimorar a colaboração com as partes interessadas. Sempre que uma solicitação de direitos de assunto é criada, uma equipe associada será criada Teams. Os usuários podem ser adicionados a uma equipe na guia Colaboradores da solicitação. Para saber mais sobre solicitações de direitos de assunto, [consulte Learn about Priva Subject Rights Requests](subject-rights-requests.md).

## <a name="data-matching"></a>Correspondência de dados  

Use esta seção para carregar esquemas de dados que descrevem atributos de seus titulares de dados, que ajudarão a identificar o titular de dados correto ao pesquisar dados pessoais em seu ambiente Microsoft 365 de dados. Esquemas e pacotes de regras são criados e carregados no formato XML. Em **Upload de dados pessoais**, você também pode enviar dados pessoais que corresponde a um esquema fornecido. Você pode criar e carregar seu próprio arquivo ou optar por carregar dados pessoais do Azure. Para saber mais sobre solicitações de direitos de assunto, [consulte Learn about Priva Subject Rights Requests](subject-rights-requests.md).

## <a name="data-retention-periods"></a>Períodos de retenção de dados

Essa configuração está relacionada a Solicitações de Direitos de Assunto Priva. Ele permite controlar sua preferência por quanto tempo deseja reter dados coletados e relatórios gerados após o fechamento da solicitação. Isso pode ser definido como 30 ou 90 dias e se aplica a todas as solicitações de direitos de assunto que você criar. Recomendamos verificar se os períodos de retenção de dados estão em conformidade com as políticas e obrigações legais da sua organização. Saiba mais sobre como [definir a retenção de dados para solicitações de direitos de assunto](subject-rights-requests-reports.md#manage-data-retention).

## <a name="data-review-tags"></a>Marcas de revisão de dados

As marcas de revisão de dados podem ser usadas para marcar itens de conteúdo recuperados em uma solicitação de direitos de assunto. Essa área de configurações permite que você gerencie suas marcas. Priva fornece três marcas padrão: **Follow-up**, **Delete** e **Update**. Esses nomes de marca não podem ser editados, mas você pode fornecer uma descrição dessas marcas que sejam significativas para sua organização.

Priva também fornece duas marcas personalizadas que você pode nomear e definir para uso da sua organização. Você os verá listados como **Marca Personalizada 1** e **Marca Personalizada 2** até editar os nomes.

Siga as etapas abaixo para editar nomes de marcas e descrições:

- Na página Priva **Configurações**, selecione **Marcas de revisão de dados**.
- Encontre a marca na lista que você deseja editar e selecione o ícone **Editar** lápis ao lado de seu nome.
- No painel de sobrevoos, faça suas edições nos campos disponíveis. Para marcas do sistema, você só pode editar a descrição. Para marcas personalizadas, você pode editar o nome e a descrição.
- Quando terminar, selecione **Enviar para** salvar suas alterações.

As configurações de marca se aplicam a todas as solicitações de direitos de assunto.

Saiba mais sobre [como aplicar marcas ao revisar dados para uma solicitação de direitos de assunto](subject-rights-requests-data-review.md#apply-tags).