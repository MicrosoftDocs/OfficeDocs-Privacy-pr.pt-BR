---
title: 'Automatizar tarefas em solicitações de direitos de entidade '
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
search.appverid:
- MOE150
- MET150
description: Saiba como usar o Microsoft Power Automate para ajudá-lo a automatizar tarefas essenciais para solicitações de direitos de assunto em Priva.
ms.openlocfilehash: ec9edde16b60c2326ca899e587dfe5dc7a1e32f5
ms.sourcegitcommit: 09ecdaded9a9f8f79587f2acb978dc53b83e5c01
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/19/2022
ms.locfileid: "64930492"
---
# <a name="automate-tasks-in-subject-rights-requests"></a>Automatizar tarefas em solicitações de direitos de entidade 

O Microsoft Power Automate é um serviço de fluxo de trabalho que automatiza ações entre aplicativos e serviços. Ao habilitar Power Automate fluxos para Solicitações de Direitos de Entidade da Microsoft Priva, você pode automatizar tarefas importantes para casos e usuários, como criar tíquetes no ServiceNow ou adicionar lembretes de calendário sobre datas de conclusão. Para saber mais sobre o Power Automate, visite o [site de documentação.](/power-automate/getting-started)

Os clientes com assinaturas de Solicitações de Direitos de Entidade não precisam de outra Power Automate para usar os modelos de Power Automate recomendados para Priva. Esses modelos podem ser personalizados para dar suporte à sua organização e abranger os principais cenários de solicitação de direitos de entidade. Se você optar por usar recursos premium do Power Automate nesses modelos, crie um modelo personalizado usando o conector de conformidade do Microsoft 365 ou use modelos do Power Automate para outras áreas de conformidade no Microsoft 365, talvez você precise de mais Power Automate licenças.

## <a name="create-a-new-power-automate-flow-from-a-template"></a>Criar um novo fluxo Power Automate de um modelo

1. No [portal de conformidade do Microsoft Purview](https://compliance.microsoft.com/), acesse a seção Priva da navegação e selecione **Priva Subject Rights Requests**.
1. Abra a solicitação de direitos de assunto com a qual você deseja trabalhar na lista e selecione **Automatizar** e, em seguida, **gerenciar Power Automate fluxos**. Isso abre o painel submenu Fluxos.
1. Use a **opção** Nova e escolha o modelo que você deseja usar nas opções disponíveis. A partir daqui, siga os prompts no assistente para concluir a instalação. As opções variam dependendo do tipo de modelo.

Depois de salvar uma instância do modelo, você deve executá-la na página de detalhes da solicitação de direitos de entidade para que a instância de fluxo tenha o contexto e a ID corretos. Abra a solicitação, retorne ao menu **Automatizar** , selecione o modelo e selecione **Executar fluxo**. Você pode ver suas atividades anteriores selecionando **Ver atividade de execução de fluxo**.

### <a name="power-automate-templates-in-priva"></a>Power Automate modelos em Priva

- **Criar um registro para o caso de gerenciamento de privacidade no ServiceNow**: esse modelo é para organizações que querem usar sua solução do ServiceNow para acompanhar casos de solicitação de direitos de entidade. Você será solicitado a inserir os detalhes da instância do ServiceNow, incluindo uma conta para se conectar ao ServiceNow. Essa conta deve ter a capacidade de criar um incidente no ServiceNow e preencher os detalhes do incidente. Depois de conectados à sua instância, os administradores de solicitações de direitos de entidade poderão criar um registro para o caso no ServiceNow e, se necessário, pode personalizar o que o modelo preencherá nos campos selecionados. Para obter mais informações sobre o conector, consulte a [página de referência do Conector do ServiceNow](/connectors/service-now/).
- **Criar um lembrete de calendário**: este modelo é para definir lembretes de data de conclusão em seu Outlook calendário para solicitações de direitos de entidade. A ferramenta preencherá determinados detalhes das propriedades da solicitação, como o nome da solicitação e sua data de conclusão. Você pode adicionar detalhes descritivos, especificar destinatários e ajustar outras configurações avançadas.
- **Obter arquivos por marca para uma solicitação** de direitos de entidade: esse modelo permite que você pesquise arquivos para sua solicitação de direitos de entidade que recebeu uma marca específica. Você pode editar o fluxo para executar ações personalizadas ou exibir a lista de arquivos retornados para aproveitar processos ou ferramentas internos.

## <a name="share-a-power-automate-flow"></a>Compartilhar um Power Automate fluxo

Ao compartilhar um Power Automate, você pode adicionar outro proprietário e permitir que ele edite, atualize e exclua o fluxo. Todos os proprietários também podem acessar o histórico de execuções e adicionar ou remover outros proprietários. Para compartilhar um fluxo, abra a solicitação de direitos de assunto com a qual você deseja trabalhar, selecione Automatizar **e, em** seguida, selecione **Gerenciar Power Automate fluxos**. Nesse painel, você pode selecionar um fluxo existente e, em seguida, usar a opção Compartilhar para adicionar um usuário ou um grupo.

Esse painel também oferece a opção de gerenciar as conexões inseridas aos serviços que estão sendo usados no Power Automate fluxo. Alterar essas configurações pode afetar sua capacidade de executar o fluxo.

## <a name="edit-or-delete-power-automate-flow"></a>Editar ou excluir Power Automate fluxo

Para ajustar os detalhes de um Power Automate, abra a solicitação de direitos de entidade, selecione Automatizar e selecione Gerenciar **Power Automate fluxos**. Nesse painel, você pode selecionar um fluxo existente para exibir detalhes. Use Editar em qualquer seção para alterar as propriedades e salvar.

Para remover totalmente o fluxo, use a **opção** Excluir. Ele removerá o fluxo de todos os proprietários e o desinstalará para todos os usuários. As instâncias de fluxo anteriores continuarão a ser executadas para evitar a perda de dados. Você pode confirmar sua escolha antes que a exclusão seja final.

## <a name="legal-disclaimer"></a>Aviso de isenção de responsabilidade legal

[Aviso de isenção de responsabilidade legal da Microsoft Priva](priva-disclaimer.md)
