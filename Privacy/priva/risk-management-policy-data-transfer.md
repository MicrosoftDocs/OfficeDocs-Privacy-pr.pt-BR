---
title: Políticas de transferência de dados no Gerenciamento de Riscos de Privacidade
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
description: Saiba como criar uma política de tratamento de dados Gerenciamento de risco de privacidade Microsoft Priva para conter transferências de dados pessoais dentro ou fora da sua organização.
ms.openlocfilehash: eba53580365d1fee387c05a54093ab04e41cd15f
ms.sourcegitcommit: 3c83e8133a5a71f4e1d76a0b2981ab3ec9cd6602
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/13/2022
ms.locfileid: "66046645"
---
# <a name="data-transfer-policies-in-privacy-risk-management"></a>Políticas de transferência de dados no Gerenciamento de Riscos de Privacidade

## <a name="whats-new"></a>Novidades
As políticas de transferência de dados agora podem detectar quando itens que contêm dados pessoais são transferidos para fora da sua organização. Transferências externas serão o cenário de transferência padrão quando você criar uma nova política de transferência de dados usando a [opção de configuração rápida](#quick-setup-use-a-template-with-default-settings). Isso não afetará nem alterará as configurações de todas as políticas de transferência de dados que você já criou.

## <a name="overview"></a>Visão Geral

A transferência de dados pessoais apresenta riscos, especialmente quando transferidos para fora da sua organização, ou enviados entre determinados departamentos ou locais geográficos em sua organização. Por exemplo, se os dados forem enviados por meio de emails não criptografados ou para destinatários não autorizados, os dados poderão não ser mais seguros. Atividades de transferência de dados como essas podem ter impacto regulatório ou violar as práticas de privacidade organizacional estabelecidas.

As políticas de transferência de dados no Gerenciamento de Riscos de Privacidade permitem monitorar transferências de dados pessoais fora da sua organização, bem como transferências internas entre diferentes departamentos ou países ou regiões. Quando uma correspondência de política é detectada, você pode enviar notificações por email aos usuários que permitem que eles executem ações corretivas no email, como tornar os itens de conteúdo particulares, notificar os proprietários de conteúdo ou marcar itens para revisão posterior.

Nosso processo de configuração de política facilita a definição de condições de política. Você tem controle total sobre o tempo de alerta e a frequência de emails e dicas in-the-moment em Microsoft Teams que trazem a atenção dos usuários para práticas seguras de tratamento de dados.

Há duas maneiras de criar uma política: com base em um **modelo, que** é nossa opção rápida de "saída" usando as configurações padrão; ou **a opção personalizada** , que é um processo guiado para definir condições, alertas e notificações.

## <a name="quick-setup-use-a-template-with-default-settings"></a>Configuração rápida: usar um modelo com configurações padrão

A política de transferência de dados padrão detecta quando os dados pessoais são enviados para destinatários fora da sua organização. Por exemplo, ele é exibido quando um usuário em sua organização envia um email Exchange um destinatário externo nos campos **Para**, **Cc** ou **Cco**.

Siga estas etapas para criar uma política de transferência de dados padrão:

1. No [portal de conformidade do Microsoft Purview](https://compliance.microsoft.com/), localize Gerenciamento de risco de privacidade Priva navegação à esquerda e selecione **Políticas**.

2. Selecione **Criar uma política** no canto superior direito da tela, que exibe um painel de submenu listando todas as opções de criação de política.

3. Na caixa **Transferências de dados** , selecione **Criar**.

4. Um painel de submenu contém detalhes da política. Selecionar **as configurações de Exibição** mostrará [as configurações padrão](#default-data-transfer-policy-settings). Você pode editar as configurações daqui, o que o levará para o processo guiado descrito abaixo. Para continuar criando sua política usando as configurações padrão, basta inserir um nome descritivo e, em seguida, selecionar **Criar política**.

Sua política será criada e você a encontrará listada na página **Políticas** . Ele começa no modo [de teste para](risk-management-policies.md#testing-a-policy) que você possa monitorar o desempenho dele antes de ativá-lo.

#### <a name="default-data-transfer-policy-settings"></a>Configurações de política de transferência de dados padrão

Uma política de transferência de dados criada a partir do modelo detectará:
- Quando dados pessoais em sua organização são transferidos ou compartilhados com um destinatário ou local fora da sua organização.
- Quando os dados pessoais são compartilhados externamente de qualquer um desses locais em sua organização:
    - **Exchange**. Exemplo: enviar um email contendo dados pessoais para um endereço de email do destinatário que está fora da sua organização.
    - **OneDrive** e **SharePoint**. Exemplos: enviar um link para um arquivo ou site que contém dados pessoais para alguém de fora da sua organização; copiando ou movendo um arquivo para um OneDrive ou SharePoint local que fica fora da sua organização.
    - **Teams**. Exemplo: enviar uma Teams de chat que contém dados pessoais para um destinatário que está fora da sua organização.
- Tipos de dados com base nos seguintes grupos [de classificação](risk-management-policies.md#classification-groups):
    - RGPD (Regulamento Geral sobre a Proteção de Dados) da UE
    - Informações de identificação pessoal dos EUA
    - Ato Patriota dos EUA
    - Lei de notificação de violação do estado dos EUA
    - Lei Gramm-Leach-Bliley (GLBA) dos EUA
    - LEI HIPAA (Us Health Insurance Portability and Accountability Act)
    - HRIP (Australia Health Records Act)
    - Ato de Privacidade da Austrália
    - Informações de identificação pessoal do Japão
    - Proteção de Informações Pessoais do Japão

## <a name="custom-setup-guided-policy-creation-process"></a>Configuração personalizada: processo de criação de política guiada

A opção de política personalizada é um processo guiado para criar uma nova política definindo condições, designando a severidade e a frequência do alerta e ativando notificações por email do usuário.

Conclua as etapas abaixo para criar uma nova política de transferência de dados:

1. No [portal de conformidade do Microsoft Purview](https://compliance.microsoft.com/), localize Gerenciamento de risco de privacidade Priva navegação à esquerda e selecione **Políticas**.

2. Selecione o **botão Criar uma política** no canto superior direito da tela, que exibe um painel de submenu listando todas as opções de criação de política.

3. Na caixa **Personalizado** , selecione **Criar**.

4. Na página **Nome e tipo** , selecione o **modelo de política de transferências** de dados. Insira um nome de política que o ajudará a identificá-lo facilmente em sua  lista na página Políticas e insira uma descrição opcional e selecione **Avançar**.

5. Na página **Dados a serem monitorados** , escolha o tipo de dados pessoais que você deseja que sua política monitore. Há duas opções:
    - **Grupos de classificação**: agrupamentos de tipos de informações confidenciais que são usados para detectar conteúdo relacionado a dados pessoais ou regulamentos específicos. Se você selecionar essa opção, precisará selecionar **+** Adicionar grupos de classificação para escolher um ou mais grupos na lista fornecida.
    - **Tipos de informações confidenciais individuais**: selecione esta opção para escolher em uma lista de tipos de [informações confidenciais individuais](/microsoft-365/compliance/sensitive-information-type-entity-definitions).

    Saiba mais sobre como [escolher dados a serem monitorados](risk-management-policies.md#choose-data-to-monitor). Quando terminar de selecionar os dados a serem monitorados, selecione **Avançar**.

6. Na página **Usuários e grupos** , escolha a quais usuários em sua organização a política será aplicada. Você pode selecionar todos os usuários individuais e todos Office 365 grupos de distribuição ou selecionar usuários e grupos específicos. Saiba mais sobre como [escolher usuários e grupos](risk-management-policies.md#choose-users-and-groups). Quando terminar, clique em **Avançar**.

7. Na página **Locais**, selecione todos os locais de dados Microsoft 365 que você deseja que a política acoberte. Escolha entre Exchange contas de email, OneDrive contas, Teams mensagens de chat e canal e SharePoint sites.

    Dentro SharePoint você pode designar todos os sites ou sites específicos. Se você selecionar **sites SharePoint específicos**, poderá inserir a URL do site no campo URL. Você também pode selecionar **+Escolher sites** e, no painel de submenu, marcar a caixa à esquerda do nome do site que você deseja selecionar.

    Saiba mais sobre como [escolher locais](risk-management-policies.md#choose-locations). Quando terminar de selecionar locais, selecione **Avançar**.

8. Na página **Condições** , selecione qual tipo de condição de transferência de dados a política detectará:
    - **Transferências fora da sua organização**: detecta transferências de usuários ou grupos dentro de sua organização para usuários externos ou convidados fora da sua organização.
    - **Transferências entre departamentos em sua organização**: para essa opção, você selecionará um departamento de remetente e um departamento de destinatários. Escolha departamentos nas listas nos painéis de submenu que aparecem e, em seguida, selecione **Adicionar**.
    - **Transferências entre fronteiras ou regiões** do país: para essa opção, você selecionará uma região do remetente e uma região de destinatário. Escolha seus países ou regiões designados nos painéis de submenu que aparecem e, em seguida, selecione **Adicionar**.

9. Na página **Resultados** , decida se os usuários devem ser notificados quando corresponderem às condições definidas pela política. Você pode escolher uma ou ambas as opções a seguir ou não deixar as caixas de seleção em branco:
    - **Dicas enviados no Microsoft Teams**: as dicas de tratamento de dados serão exibidas na instância de um usuário do Teams quando eles executarem uma ação que corresponda às condições da política. Você precisará adicionar uma URL para seu treinamento de privacidade preferido, que também aparecerá na dica.
    - **Notificações por email**: os usuários receberão uma notificação por email quando suas ações corresponderem às condições da política. Os emails conterão instruções para executar ações de correção diretamente do email, juntamente com um link para treinamento de privacidade. Você designará a frequência de emails e a URL para seu treinamento de privacidade preferido.
     
    Saiba mais sobre como configurar [notificações do usuário](risk-management-notifications.md). Quando terminar de selecionar os resultados, selecione **Avançar**.

10. Na página **Alertas**, use o botão de alternância para ativar alertas que um administrador verá na página **Alertas** na seção Políticas do  Gerenciamento de Riscos de Privacidade. Você designará com que frequência os alertas são gerados, os limites para as correspondentes antes que os alertas sejam gerados e a severidade do alerta. Saiba mais sobre como [definir alertas para as correspondentes de política](risk-management-policies.md#set-alerts). Quando terminar, clique em **Avançar**.

11. Na página **Modo** , decida se deseja ou não executar sua política no modo de teste quando a criar pela primeira vez, o que significa que nenhum alerta ou notificação será enviado. Para manter sua política no modo de teste, o que recomendamos, selecione o botão de alternância para a **posição** Ativado. Saiba mais sobre [como testar uma política](risk-management-policies.md#testing-a-policy).

> [!NOTE]
> Se você alternar a opção **Executar** no modo de teste para  a posição *Desativada, isso* ativará sua política quando terminar de criá-la. Isso significa que todos os alertas ou notificações do usuário que você configurar começarão a gerar depois que uma correspondência for detectada.

12. Na página **Concluir** , examine suas escolhas. Selecione **Editar** abaixo de qualquer uma das seções para ajustar as configurações. Quando estiver satisfeito com as configurações da política, selecione **Enviar** para criar a política.

Após alguns segundos, você verá uma confirmação de que a política foi criada. Selecione **Concluído** na página de confirmação, que levará você para a página  Políticas, na qual você verá a nova política na parte superior da tabela.

## <a name="next-steps"></a>Próximas etapas

Visite [as políticas de Gerenciamento de Risco de](risk-management-policies.md) Privacidade para obter detalhes sobre como editar e gerenciar políticas.
