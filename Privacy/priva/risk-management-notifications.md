---
title: Enviar notificações do usuário no Gerenciamento de Riscos de Privacidade
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
description: Saiba como notificar os proprietários de conteúdo sobre correspondências de política encontradas pelo Gerenciamento de Risco de Privacidade da Microsoft Priva e como eles podem usar essas notificações por email para corrigir problemas.
ms.openlocfilehash: 8969e1cd4d5859102b18bd46723d1be6e85d35f6
ms.sourcegitcommit: b5f7dcb73c0e3f677981e80106769cb546d00af4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2022
ms.locfileid: "65014371"
---
# <a name="user-notifications-in-privacy-risk-management"></a>Notificações do usuário no Gerenciamento de Riscos de Privacidade

Ao configurar uma política no Gerenciamento de Riscos de Privacidade, você pode optar por notificar os usuários quando suas ações atenderem às condições definidas na política. Há dois tipos de notificações: emails, que estão disponíveis para todos os três tipos de política, e dicas que aparecem no Teams, que estão disponíveis apenas para o tipo de política de transferência de dados. Ao criar ou editar uma política, você pode decidir se deseja ativar essas notificações, com que frequência enviá-las e personalizar o conteúdo.

O envio de notificações aos usuários pode ser um componente importante para ajudar sua organização a cumprir suas metas de privacidade. As notificações foram projetadas para:

- Traga reconhecimento imediato aos usuários quando suas ações puderem expor dados pessoais a riscos de privacidade.
- Forneça métodos de correção diretamente dentro dos emails, para que os usuários possam tomar medidas rápidas para proteger os dados em risco.
- Direcione os usuários para as diretrizes de privacidade e as práticas recomendadas da sua organização.

Informar os usuários sobre possíveis problemas no momento e capacitá-los a corrigir problemas e atualizar suas habilidades pode ser ferramentas poderosas para criar práticas de tratamento de dados de som em toda a sua organização.

Examine as seções abaixo para ajudá-lo a preparar e gerenciar notificações do usuário para as correspondentes à política.

## <a name="prepare-training-content-for-notifications"></a>Preparar conteúdo de treinamento para notificações

Incluir um link para o treinamento de privacidade será necessário se você optar por enviar notificações do usuário quando forem detectadas correspondentes à política. Fornecer acesso às diretrizes de privacidade da sua organização permite que você mantenha seus usuários informados sobre suas próprias práticas e políticas recomendadas. Ele também pode fornecer contexto para as ações de correção sugeridas no email e ajudar os usuários a se prepararem para boas decisões de gerenciamento de dados no futuro.

Antes de configurar sua política, decida sobre a URL de treinamento que você deseja incluir. Um link pode ser fornecido por política, portanto, recomendamos escolher referências específicas para cada cenário.

## <a name="set-user-email-notifications"></a>Definir notificações de email do usuário

Você pode configurar notificações por email para todos os tipos de política ao criar uma nova política ou editar uma política existente. Essas configurações são encontradas na **página Resultados** do assistente de criação de política. Visite [Definir resultados: notificações do usuário e dicas](risk-management-policies.md#define-outcomes-user-email-notifications-and-tips) para as instruções completas.

> [!NOTE]
> A capacidade geral do Gerenciamento de Riscos de Privacidade para enviar notificações por email é controlada em Priva **Configurações**. Ele está habilitado por padrão. Desativar essa configuração interromperá todos os emails mesmo que as notificações tenham sido configuradas em um nível de política individual. Saiba mais sobre as [configurações de email de notificação do usuário](priva-settings.md#user-notification-emails).

## <a name="send-notifications-in-teams"></a>Enviar notificações no Teams

Para políticas de transferência de dados, você pode optar por que os usuários recebam dicas de política e recomendações em canais seguros Teams quando uma correspondência de política é detectada. Essas dicas instruem os usuários sobre o uso responsável de dados pessoais. Dicas incluirá links para treinamento relacionado.

Para saber mais sobre como configurar essas notificações, visite [Definir resultados: notificações e dicas do usuário](risk-management-policies.md#define-outcomes-user-email-notifications-and-tips).

## <a name="preview-and-customize-email-content"></a>Visualizar e personalizar o conteúdo do email

Quando os usuários recebem notificações por email sobre as correspondentes à política, eles podem seguir os prompts nos emails para tomar medidas corretivas imediatamente. Por exemplo, se uma política de superexposure de dados encontrar uma correspondência para dados pessoais que podem ser muito amplamente acessíveis, o email de notificação incluirá um link para o item de conteúdo para que o usuário possa revisá-lo e botões para o usuário marcar o item como particular ou manter seu nível de acesso atual. As ações sugeridas serão relevantes para cada tipo diferente de política.

Você pode visualizar o conteúdo do email e fazer suas próprias alterações ao ajustar essa configuração no processo de criação ou edição de política. Para visualizar e editar o conteúdo do email de notificação, siga as etapas abaixo:

1. Crie ou edite sua política iniciando as etapas descritas no processo de criação [de política guiada](risk-management-policies.md#custom-setup-guided-process-to-choose-all-settings).

2. Na etapa **Resultados do** processo, selecione a caixa ao lado de Enviar um **email de notificação aos usuários quando ocorrer uma correspondência de política**.

3. Selecione o **botão Visualizar e editar email de notificação** que aparece abaixo da caixa de seleção de email de notificação.

4. Um painel de submenu é exibido com campos de texto preenchidos previamente com o conteúdo de email padrão. Você pode editar qualquer ou todos os campos, que incluem: a linha de assunto do email, o cabeçalho do corpo, o conteúdo do corpo, o nome de exibição do treinamento de privacidade e a URL de treinamento. A visualização do email está na parte inferior do painel de submenu e será alterada à medida que você fizer edições para o texto padrão. Quando estiver satisfeito com o conteúdo do email, selecione **Salvar** para salvar suas configurações. Para descartar as alterações no email padrão, selecione **o X** no canto superior direito do painel de submenu para fechar e reverter para o conteúdo padrão.

5. De volta à **página Resultados** , selecione **Avançar**. Continue com o assistente e, quando chegar à **página Finalização** , examine suas configurações e selecione **Enviar**.

As configurações de notificação agora estarão em vigor para essa política. Se sua política estiver testando, as notificações não serão enviadas. Se a política estiver ativada, as notificações serão enviadas. Veja mais detalhes sobre como [criar e gerenciar políticas](risk-management-policies.md).


## <a name="legal-disclaimer"></a>Aviso de isenção de responsabilidade legal

[Aviso de isenção de responsabilidade legal da Microsoft Priva](priva-disclaimer.md)
