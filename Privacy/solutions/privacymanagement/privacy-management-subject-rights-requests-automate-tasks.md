---
title: Automatizar tarefas de solicitações de direitos de assunto no gerenciamento de privacidade
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
description: Saiba como usar o Microsoft Power Automate ajudar você a automatizar tarefas essenciais para solicitações de direitos de assunto no gerenciamento de privacidade.
ms.openlocfilehash: df76e87e3298b2ccc6c897d485e695d0f1ae35c9
ms.sourcegitcommit: 85e085eb17af8b4efd1f45207445e1b3c3679600
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/19/2021
ms.locfileid: "60478061"
---
# <a name="automate-subject-rights-requests-tasks"></a>Automatizar tarefas de solicitações de direitos de assunto

O Microsoft Power Automate é um serviço de fluxo de trabalho que automatiza ações entre aplicativos e serviços. Ao habilitar Power Automate fluxos para gerenciamento de privacidade para Microsoft 365, você pode automatizar tarefas importantes para casos e usuários, como criar tíquetes no ServiceNow ou adicionar lembretes de calendário sobre datas de vencimento. Para saber mais sobre Power Automate, visite seu [site de documentação](/power-automate/getting-started).

Os clientes com Microsoft 365 assinaturas que incluem gerenciamento de privacidade não precisam de outra Power Automate licenças para usar os modelos de gerenciamento de Power Automate de privacidade recomendados. Esses modelos podem ser personalizados para dar suporte à sua organização e abranger os principais cenários de gerenciamento de privacidade. Se você optar por usar recursos de Power Automate premium nesses modelos, crie um modelo personalizado usando o conector de conformidade do Microsoft 365 ou use modelos de Power Automate para outras áreas de conformidade no Microsoft 365, talvez você precise de mais Power Automate licenças.

## <a name="create-a-new-power-automate-flow-from-a-template"></a>Criar um novo fluxo Power Automate de um modelo

1. No [Centro de conformidade do Microsoft 365](https://compliance.microsoft.com/), vá para a seção gerenciamento de privacidade da navegação e selecione **Solicitações de direitos de assunto**.
1. Abra a solicitação de direitos de assunto que você deseja trabalhar na lista e selecione **Automatizar**, em seguida, **Gerenciar Power Automate fluxos**. Isso abre o painel de sobrevoos Fluxos.
1. Use a **opção Nova** e escolha o modelo que você deseja usar nas opções disponíveis. A partir daqui, siga os prompts no assistente para concluir a instalação. As opções variam dependendo do tipo de modelo.

Depois de salvar uma instância do modelo, você deve executá-la na página de detalhes da solicitação de direitos de assunto para que a instância de fluxo tenha o contexto e a ID corretos. Abra a solicitação, retorne ao menu **Automatizar,** selecione o modelo e selecione **Executar fluxo**. Você pode ver suas atividades passadas selecionando **See flow run activity**.

### <a name="power-automate-templates-in-privacy-management"></a>Power Automate modelos no gerenciamento de privacidade

- **Criar registro para caso de gerenciamento** de privacidade em ServiceNow : Este modelo é para organizações que querem usar sua solução ServiceNow para rastrear casos de solicitação de direitos de entidade. Você será solicitado a inserir os detalhes da instância serviceNow, incluindo uma conta para se conectar ao ServiceNow. Essa conta deve ter a capacidade de criar um incidente em ServiceNow e preencher detalhes de incidentes. Depois de se conectar à sua instância, os administradores de solicitações de direitos de assunto poderão criar um registro para o caso em ServiceNow e, se necessário, poderão personalizar o que o modelo preencherá em campos selecionados. Para obter mais informações sobre o conector, consulte a página de referência do [Conector serviceNow.](/connectors/service-now/)
- **Criar um lembrete de calendário**: este modelo é para definir lembretes de data de vencimento em seu calendário Outlook para solicitações de direitos de assunto. A ferramenta preencherá determinados detalhes das propriedades da solicitação, como o nome da solicitação e sua data de vencimento. Você pode adicionar detalhes descritivos, especificar destinatários e ajustar outras configurações avançadas.
- **Obter arquivos por marca para uma** solicitação de direitos de assunto : Este modelo permite que você pesquise arquivos para sua solicitação de direitos de assunto que receberam uma marca específica. Você pode editar o fluxo para executar ações personalizadas ou exibir a lista de arquivos retornados para aproveitar processos internos ou ferramentas.

## <a name="share-a-power-automate-flow"></a>Compartilhar um Power Automate fluxo

Ao compartilhar um Power Automate, você pode adicionar outro proprietário e permitir que eles editem, atualizem e excluam o fluxo. Todos os proprietários também podem acessar o histórico de executar e adicionar ou remover outros proprietários. Para compartilhar um fluxo, abra a solicitação de direitos de assunto que você deseja trabalhar, selecione **Automatizar** e selecione **Gerenciar Power Automate fluxos**. Neste painel, você pode selecionar um fluxo existente e, em seguida, usar a opção Compartilhar para adicionar um usuário ou um grupo.

Esse painel também oferece a opção de gerenciar as conexões incorporadas aos serviços que estão sendo usados no Power Automate fluxo. Alterar essas configurações pode afetar sua capacidade de executar o fluxo.

## <a name="edit-or-delete-power-automate-flow"></a>Editar ou excluir Power Automate fluxo

Para ajustar detalhes de um fluxo Power Automate, abra a solicitação de direitos de assunto, selecione **Automatizar** e selecione **Gerenciar Power Automate fluxos**. Neste painel, você pode selecionar um fluxo existente para exibir detalhes. Use Editar em qualquer seção para alterar as propriedades e salvar.

Para remover completamente o fluxo, use a **opção** Excluir. Ele removerá o fluxo para todos os proprietários e o desinstalará para todos os usuários. As instâncias de fluxo anteriores continuarão a ser executados para evitar a perda de dados. Você pode confirmar sua escolha antes que a exclusão seja final.

## <a name="legal-disclaimer"></a>Aviso de isenção de responsabilidade legal

[Aviso de isenção de responsabilidade legal de gerenciamento de privacidade](privacy-management-disclaimer.md)
