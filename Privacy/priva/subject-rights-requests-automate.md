---
title: Integrar com o Microsoft API do Graph e Power Automate
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
description: Saiba como estender recursos Solicitações de direitos do titular Priva integrando-se ao Microsoft API do Graph e Power Automate.
ms.openlocfilehash: e4fcad2067ece3d1a6338e6d4891c59d91205a33
ms.sourcegitcommit: 9315064bf5bb9e889318e61ec5f082f36c815e1e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65851636"
---
# <a name="integrate-and-extend-through-microsoft-graph-api-and-power-automate"></a>Integrar e estender por meio do Microsoft API do Graph e Power Automate

Você pode integrar Solicitações de direitos do titular Priva com seus processos e ferramentas de negócios existentes usando a API de Solicitação de Direitos de Entidade do Microsoft Graph. Você também pode estender as funcionalidades de automação das Solicitações de Direitos de Entidade usando fluxos de Power Automate internos para tarefas como a configuração de lembretes de calendário e a criação de casos no ServiceNow.

## <a name="microsoft-graph-subject-rights-requests-api"></a>API Graph solicitações de direitos de entidade do Microsoft Graph

A MICROSOFT 365 de Solicitação de Direitos de Entidade oferece uma maneira simples, mas poderosa, de introduzir automação à sua estratégia de direitos de entidade existente. Quando uma pessoa solicita informações de sua organização, nossas APIs permitem que você crie essas solicitações em Microsoft 365 com base nos critérios para essa solicitação. Você pode criar a solicitação de direitos de entidade em Microsoft 365, acompanhar seu progresso e confirmar quando a solicitação tiver concluído o processamento e o conteúdo estiver pronto para recuperação.

Nossas APIs estão disponíveis para qualquer pessoa usar para tornar suas soluções mais extensíveis, como ISVs, parceiros que procuram acomodar o Microsoft 365 em suas soluções e organizações que procuram usar as APIs com seus aplicativos de linha de negócios.

Exiba a documentação completa [em Usar a API de solicitação Graph direitos de entidade da Microsoft](/graph/api/resources/subjectrightsrequest-subjectrightsrequestapioverview).

## <a name="power-automate-templates-for-subject-rights-requests"></a>Power Automate modelos para solicitações de direitos de entidade

O Microsoft Power Automate é um serviço de fluxo de trabalho que automatiza ações entre aplicativos e serviços. As Solicitações de Direitos de Entidade incluem modelos Power Automate internos para ajudar os usuários a gerenciar solicitações de direitos de entidade. Os usuários podem configurar fluxos de automação para processos como criar tíquetes no ServiceNow e adicionar lembretes de calendário sobre datas de conclusão. Para saber mais sobre o Power Automate, visite a [Power Automate documentação](/power-automate/getting-started).

Se você comprou uma assinatura de Solicitações de Direitos de Entidade, não precisará de uma licença de Power Automate separada para usar os modelos de Power Automate recomendados. Esses modelos podem ser personalizados para dar suporte à sua organização e abranger os principais cenários de solicitação de direitos de entidade. No entanto, talvez você precise de licenças extras para usar Power Automate recursos premium nesses modelos ou para criar seu próprio modelo.

### <a name="available-templates"></a>Modelos disponíveis

- **Criar registro para Priva** de gerenciamento de privacidade no ServiceNow: esse modelo é para organizações que querem usar sua solução do ServiceNow para acompanhar casos de solicitação de direitos de entidade. Você será solicitado a inserir os detalhes da instância do ServiceNow, incluindo uma conta para se conectar ao ServiceNow. Essa conta deve ter a capacidade de criar um incidente no ServiceNow e preencher os detalhes do incidente. Depois de conectados à sua instância, os administradores de solicitações de direitos de entidade poderão criar um registro para o caso no ServiceNow e, se necessário, pode personalizar o que o modelo preencherá nos campos selecionados. Para obter mais informações sobre o conector, consulte a [documentação do conector do ServiceNow](/connectors/service-now/).

- **Adicione um lembrete** de calendário para acompanhar um caso de gerenciamento Priva privacidade: este modelo é para definir lembretes de data de conclusão em seu calendário Outlook para solicitações de direitos de entidade. A ferramenta preencherá determinados detalhes das propriedades da solicitação, como o nome da solicitação e sua data de conclusão. Você pode adicionar detalhes descritivos, especificar destinatários e ajustar outras configurações avançadas.

- **Obter arquivos por marca para** uma Priva de direitos de entidade: este modelo permite que você pesquise arquivos para sua solicitação de direitos de entidade que recebeu uma marca específica. Você pode editar o fluxo para executar ações personalizadas ou exibir a lista de arquivos retornados a serem usados para processos ou ferramentas internos.

### <a name="create-a-new-power-automate-flow-from-a-template"></a>Criar um novo fluxo Power Automate de um modelo

1. No [portal de conformidade do Microsoft Purview,](https://compliance.microsoft.com/) selecione **Solicitações de direitos do titular Priva** no painel de navegação esquerdo.

2. Localize a solicitação de direitos de assunto na qual você deseja trabalhar e selecione-a na lista para abrir sua página de detalhes.

3. No canto superior direito, selecione **Automatizar** e, em seguida, **selecione Gerenciar Power Automate fluxos** para abrir o painel de submenu de fluxos.

4. Selecione **Novo** e escolha o modelo que você deseja usar nas opções disponíveis. A partir daqui, siga os prompts para personalizar e adicionar etapas para concluir a criação do fluxo. As opções variam dependendo do modelo usado (consulte os tipos de modelo abaixo).

5. Quando terminar, selecione **Salvar**.

Depois de salvar uma instância do modelo, execute-a na página de detalhes da solicitação para que a instância de fluxo tenha o contexto e a ID corretos. Abra a solicitação, retorne ao menu **Automatizar** , selecione o modelo e selecione **Executar fluxo**. Você pode ver suas atividades anteriores selecionando **Ver atividade de execução de fluxo**.

### <a name="share-a-power-automate-flow"></a>Compartilhar um Power Automate fluxo

O compartilhamento Power Automate fluxo permite adicionar outro proprietário e permite que ele edite, atualize e exclua o fluxo. Todos os proprietários podem acessar o histórico de execuções e adicionar ou remover outros proprietários. 

Para compartilhar um fluxo, abra a solicitação de direitos de assunto com a qual você deseja trabalhar, selecione Automatizar **e, em** seguida, selecione **Gerenciar Power Automate fluxos**. Nesse painel, você pode selecionar um fluxo existente e, em seguida, usar  a opção Compartilhar para adicionar um usuário ou um grupo.

Esse painel também oferece a opção de gerenciar as conexões inseridas aos serviços que estão sendo usados no Power Automate fluxo. Alterar essas configurações pode afetar sua capacidade de executar o fluxo.

### <a name="edit-or-delete-power-automate-flow"></a>Editar ou excluir Power Automate fluxo

Para ajustar os detalhes de um fluxo Power Automate, selecione Automatizar  no canto superior direito da página de detalhes de uma solicitação e, em seguida, selecione Gerenciar **Power Automate fluxos**.

No painel **Power Automate fluxos**, selecione o fluxo que você deseja editar e selecione **Editar** na barra de comandos para editar ou adicionar etapas. Quando terminar, selecione **Salvar**.

Para excluir um fluxo, selecione-o na lista no painel **Power Automate fluxos** e selecione **Excluir** na barra de comandos. O fluxo será removido para todos os proprietários e desinstalado para todos os usuários. As instâncias de fluxo anteriores continuarão a ser executadas para evitar a perda de dados. Você será solicitado a confirmar antes que a exclusão seja final.

## <a name="legal-disclaimer"></a>Aviso de isenção de responsabilidade legal

[Microsoft Priva aviso de isenção de responsabilidade legal](priva-disclaimer.md)
