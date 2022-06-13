---
title: Políticas de superexposição de dados no Gerenciamento de Riscos de Privacidade
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
description: Saiba como criar uma política de superexpover de dados Gerenciamento de risco de privacidade Microsoft Priva identificar e proteger dados pessoais que podem estar super acessíveis.
ms.openlocfilehash: 6efb92ed5d1b79b0fc69beebd5788062b5687269
ms.sourcegitcommit: 3c83e8133a5a71f4e1d76a0b2981ab3ec9cd6602
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/13/2022
ms.locfileid: "66046675"
---
# <a name="data-overexposure-policies-in-privacy-risk-management"></a>Políticas de superexposição de dados no Gerenciamento de Riscos de Privacidade

Sua organização pode armazenar conteúdo em vários níveis de acesso, incluindo áreas publicamente acessíveis e outras restritas. As políticas de superexposição de dados podem ajudá-lo a detectar e lidar com situações em que os dados armazenados por sua organização são insuficientemente seguros. Por exemplo, se o acesso a um site interno estiver aberto para muitas pessoas ou suas configurações de permissões não tiverem sido mantidas, os dados pessoais armazenados nesse site poderão ficar vulneráveis a uma violação. As políticas de superexposição de dados podem avaliar seus dados para esses riscos e alertá-lo sobre possíveis problemas.

Quando uma correspondência de política é detectada, você pode enviar notificações por email aos usuários que incluem opções de correção para resolver problemas. Para superexposição de dados, isso inclui tornar os itens de conteúdo particulares, notificar os proprietários de conteúdo ou marcar itens para revisão posterior.

Nosso processo de configuração de política facilita a definição de condições de política. Você tem controle total sobre o tempo de alerta e a frequência de emails que trazem a atenção dos usuários para práticas seguras de tratamento de dados.

Há duas maneiras de criar uma política: com base em um **modelo, que** é nossa opção rápida de "saída" usando as configurações padrão; ou **a opção personalizada** , que é um processo guiado para definir condições, alertas e notificações.

## <a name="quick-setup-use-a-template-with-default-settings"></a>Configuração rápida: usar um modelo com configurações padrão

A política de superexposição de dados padrão avalia dados pessoais em todos os três níveis de acesso: público, externo e interno.

Siga estas etapas para criar uma política de transferência de dados padrão:

1. No [portal de conformidade do Microsoft Purview](https://compliance.microsoft.com/), localize Gerenciamento de risco de privacidade Priva navegação à esquerda e selecione **Políticas**.

2. Selecione **Criar uma política** no canto superior direito da tela, que exibe um painel de submenu listando todas as opções de criação de política.

3. Na caixa **Dados sobreexpexposure** , selecione **Criar**.

4. Um painel de submenu contém detalhes da política. Selecionar **as configurações de Exibição** mostrará as configurações padrão. Você pode editar as configurações daqui, o que o levará para o processo guiado descrito abaixo. Para continuar criando sua política usando as configurações padrão, basta inserir um nome descritivo e, em seguida, selecionar **Criar política**.

Sua política será criada e você a encontrará listada na página **Políticas** . Ele começa no modo [de teste para](risk-management-policies.md#testing-a-policy) que você possa monitorar o desempenho dele antes de ativá-lo.

#### <a name="default-data-overexposure-policy-settings"></a>Configurações de política de superexposição de dados padrão

Uma política de superexposição de dados criada a partir do modelo detectará:

- Quando um usuário fornece acesso muito amplo a itens que contêm dados pessoais armazenados no OneDrive ou SharePoint. Por exemplo, a política detectará o compartilhamento de dados pessoais das seguintes maneiras:
    - Por meio de um link que qualquer pessoa no público pode acessar
    - Por meio de um link ou por causa de permissões que permitem que todos na organização acessem
    - Concedendo direitos de acesso a usuários externos ou convidados para OneDrive ou SharePoint arquivos
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

Conclua as etapas abaixo para criar uma nova política de superexposição de dados:

1. No [portal de conformidade do Microsoft Purview](https://compliance.microsoft.com/), localize Gerenciamento de risco de privacidade Priva navegação à esquerda e selecione **Políticas**.

2. Selecione o **botão Criar uma política** no canto superior direito da tela, que exibe um painel de submenu listando todas as opções de criação de política.

3. Na caixa **Personalizado** , selecione **Criar**.

4. Na página **Nome e tipo** , selecione o **modelo de política data overexposure** . Insira um nome de política que o ajudará a identificá-lo facilmente em sua  lista na página Políticas e insira uma descrição opcional e selecione **Avançar**.

5. Na página **Dados a serem monitorados** , escolha o tipo de dados pessoais que você deseja que sua política monitore. Há duas opções:
    - **Grupos de classificação**: agrupamentos de tipos de informações confidenciais que são usados para detectar conteúdo relacionado a dados pessoais ou regulamentos específicos. Se você selecionar essa opção, precisará selecionar **+** Adicionar grupos de classificação para escolher um ou mais grupos na lista fornecida.
    - **Tipos de informações confidenciais individuais**: selecione esta opção para escolher em uma lista de tipos de [informações confidenciais individuais](/microsoft-365/compliance/sensitive-information-type-entity-definitions).

    Saiba mais sobre como [escolher dados a serem monitorados](risk-management-policies.md#choose-data-to-monitor). Quando terminar de selecionar os dados a serem monitorados, selecione **Avançar**.

6. Na página **Usuários e grupos** , escolha a quais usuários em sua organização a política será aplicada. Você pode selecionar todos os usuários individuais e todos Office 365 grupos de distribuição ou selecionar usuários e grupos específicos. Saiba mais sobre como [escolher usuários e grupos](risk-management-policies.md#choose-users-and-groups). Quando terminar, clique em **Avançar**.

7. Na página **Locais**, selecione todos os locais de dados Microsoft 365 que você deseja que a política acoberte. Escolha entre OneDrive contas e SharePoint sites.

    Dentro SharePoint você pode designar todos os sites ou sites específicos. Se você selecionar **sites SharePoint específicos**, poderá inserir a URL do site no campo URL. Você também pode selecionar **+Escolher sites** e, no painel de submenu, marcar a caixa à esquerda do nome do site que você deseja selecionar.

    Saiba mais sobre como [escolher locais](risk-management-policies.md#choose-locations). Quando terminar de selecionar locais, selecione **Avançar**.

8. Na página **Condições** , selecione qual tipo de condição de superexposição de dados a política detectará:
    - **Público**: qualquer pessoa com um link pode acessar o conteúdo.
    - **Externo**: pessoas específicas fora da organização têm acesso.
    - **Interno**: todos os usuários em sua organização têm acesso.
    
    Selecionar mais de um nível de acesso ampliará o escopo dos dados e poderá gerar quantidades significativamente maiores de alertas e notificações do usuário.

    Coloque uma caixa de seleção ao lado de suas opções e selecione **Avançar**.

9. Na página **Resultados** , decida se os usuários devem ser notificados quando corresponderem às condições definidas pela política. Se você marcar a caixa de notificações por email, os usuários receberão uma notificação por email quando suas ações corresponderem às condições da política. Os emails conterão instruções para executar ações de correção diretamente do email, juntamente com um link para treinamento de privacidade. Você designará a frequência de emails e a URL para seu treinamento de privacidade preferido.
     
    Saiba mais sobre como configurar [notificações do usuário](risk-management-notifications.md). Quando terminar de selecionar os resultados, selecione **Avançar**.

10. Na página **Alertas**, use o botão de alternância para ativar alertas que um administrador verá na página **Alertas** na seção Políticas do  Gerenciamento de Riscos de Privacidade. Você designará com que frequência os alertas são gerados, os limites para as correspondentes antes que os alertas sejam gerados e a severidade do alerta. Saiba mais sobre como [definir alertas para as correspondentes de política](risk-management-policies.md#set-alerts). Quando terminar, clique em **Avançar**.

11. Na página **Modo** , decida se deseja ou não executar sua política no modo de teste quando a criar pela primeira vez, o que significa que nenhum alerta ou notificação será enviado. Para manter sua política no modo de teste, o que recomendamos, selecione o botão de alternância para a **posição** Ativado. Saiba mais sobre [como testar uma política](risk-management-policies.md#testing-a-policy).

> [!NOTE]
> Se você alternar a opção **Executar** no modo de teste para  a posição *Desativada, isso* ativará sua política quando terminar de criá-la. Isso significa que todos os alertas ou notificações do usuário que você configurar começarão a gerar depois que uma correspondência for detectada.

12. Na página **Concluir** , examine suas escolhas. Selecione **Editar** abaixo de qualquer uma das seções para ajustar as configurações. Quando estiver satisfeito com as configurações da política, selecione **Enviar** para criar a política.

Após alguns segundos, você verá uma confirmação de que a política foi criada. Selecione **Concluído** na página de confirmação, que levará você para a página  Políticas, na qual você verá a nova política na parte superior da tabela.

## <a name="next-steps"></a>Próximas etapas

Visite [as políticas de Gerenciamento de Risco de](risk-management-policies.md) Privacidade para obter detalhes sobre como editar e gerenciar políticas.