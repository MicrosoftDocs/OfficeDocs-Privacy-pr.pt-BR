---
title: Criar uma solicitação e definir configurações de pesquisa em Solicitações de Direitos de Entidade
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
description: Saiba como criar uma nova solicitação de direitos de entidade e definir configurações de pesquisa Solicitações de direitos do titular Microsoft Priva.
ms.openlocfilehash: 7314fefa370b24bcb215a99b67b74c13b8b27613
ms.sourcegitcommit: 3c83e8133a5a71f4e1d76a0b2981ab3ec9cd6602
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/13/2022
ms.locfileid: "66046635"
---
# <a name="create-a-request-and-define-search-settings"></a>Criar uma solicitação e definir configurações de pesquisa

**Neste artigo**: saiba como criar uma solicitação no Priva para começar a atender a uma solicitação de direitos de entidade. Entenda as configurações de pesquisa para recuperação de dados e como refinar sua pesquisa.

Os usuários que têm uma função no grupo de função Administradores de Solicitação de Direitos de Entidade que não sejam somente exibição [(consulte](priva-permissions.md) Priva permissões) podem criar uma solicitação em Solicitações de Direitos de Entidade. Um processo guiado orienta você pelas configurações para localizar dados pessoais sobre um titular de dados e iniciar o processo de atendimento à solicitação.

## <a name="request-types"></a>Tipos de solicitação

Solicitações de direitos do titular Priva dá suporte a três tipos diferentes de solicitações:

1. **Acesso**: fornece um resumo das informações pessoais do titular dos dados mantidos por sua organização em Microsoft 365.

2. **Exportação**: fornece um resumo e um arquivo exportado de itens de conteúdo que contêm as informações pessoais do titular dos dados. Esses são os itens revisados e marcados como **Incluídos** durante a revisão dos dados coletados pelas configurações de pesquisa.

3. **Lista marcada para** acompanhamento: gera um resumo de todos os arquivos que foram marcados durante a revisão de dados que podem exigir ação adicional fora do Priva. Por exemplo, talvez seja necessário facilitar a exclusão das informações pessoais do titular dos dados de acordo com sua solicitação. Você pode exibir as marcas incluídas e configurar marcas personalizadas para sua organização em Priva [configurações](priva-settings.md).

## <a name="getting-started-with-your-first-request"></a>Introdução à sua primeira solicitação

Quando você inicia uma avaliação ou assinatura de Solicitações de Direitos de Entidade, oferecemos uma configuração simples e inicial para sua primeira solicitação que usa as configurações padrão. Essa configuração pode ajudá-lo a explorar o fluxo de trabalho de solicitação de direitos de assunto e familiarizar-se com sua funcionalidade.

Na primeira vez que chegar à página Solicitações de Direitos de Entidade, você verá uma faixa na parte superior com um botão **Introdução** assunto. Quando um usuário seleciona esse botão, um painel de submenu é exibido com as informações desse usuário preenchidas previamente nos campos de nome e email e mostra todas as configurações padrão.

**Explorar a funcionalidade de solicitação** com suas informações: experimentar uma solicitação de direitos de assunto com base em suas próprias informações pode ajudá-lo a obter familiaridade e conforto ao passar por cada estágio do processo. Você verá o que uma pesquisa padrão produz e pode praticar o refinamento de resultados ajustando as configurações de pesquisa. Na guia  Dados coletados, você pode examinar itens na área de visualização à direita e praticar a reação de texto, aplicar marcas, inserir anotações e marcar itens para incluir ou excluir para o relatório final (encontre detalhes em Examinar dados para uma solicitação de direitos de [assunto).](subject-rights-requests-data-review.md)

- Você não precisa usar suas informações para criar sua primeira solicitação. Se você estiver pronto para iniciar uma solicitação para um titular dos dados, substitua seu nome e endereço de email com as informações do titular dos dados.

Para aceitar todas as configurações e criar a solicitação, selecione **Criar**. O painel será fechado e você verá sua nova solicitação listada na página **Solicitações de Direitos de** Entidade. Para alterar qualquer uma das configurações padrão antes de criar a solicitação, selecione Editar detalhes da solicitação **, o** que o coloca no assistente de criação de solicitação [de direitos de assunto](#create-a-request).

> [!NOTE]
> Qualquer solicitação que você criar contará para a sua avaliação ou a atribuição de assinatura paga, independentemente de quais informações do titular dos dados são usadas para a solicitação. O período de retenção de dados padrão de 30 dias se aplica após o fechamento da solicitação. Saiba como alterar [períodos de retenção para solicitações de direitos de entidade](subject-rights-requests-reports.md#retention-periods-for-reports-and-data).

## <a name="create-a-request"></a>Criar uma solicitação

Siga as etapas abaixo para começar a atender a uma solicitação de direitos de entidade:

1. No [portal de conformidade do Microsoft Purview](https://compliance.microsoft.com/), selecione **Solicitações de direitos do titular Priva** no painel de navegação esquerdo.

2. No canto superior direito da tela, selecione **Criar uma solicitação**.

3. Na página **Informações do titular dos** dados, insira o nome e sobrenome do titular dos dados e o endereço de email. Selecione **Adicionar residência** para escolher o país de residência do titular dos dados. Selecione a opção que identifica como o titular dos dados está relacionado à sua organização (como cliente ou funcionário atual) e selecione Avançar para  passar para a próxima etapa.

4. Na página **Locais** , decida onde você deseja pesquisar as informações do titular dos dados. Escolha um ou ambos os locais a seguir movendo o botão de alternância de status ao lado de cada opção para a **posição** Ativado:

   - **Exchange**: procure dados em caixas Exchange caixas de correio e em chats individuais ou Teams grupo. Você pode optar por pesquisar todas as Exchange em sua organização ou selecionar Escolher contas para  selecionar usuários individuais no painel de submenu Exchange **caixas** de correio.

   - **SharePoint**: procure dados em sites SharePoint, sites OneDrive for Business sites e Teams canais. Você pode optar por pesquisar todos SharePoint sites em sua organização ou selecionar Escolher **sites** para selecionar usuários individuais no painel de submenu SharePoint **sites**.

> [!TIP]
> Para obter ajuda com a identificação dos termos de pesquisa apropriados, consulte os seguintes tópicos:
> - SharePoint sites e URLs: gerenciar sites no centro de administração do [SharePoint](/sharepoint/manage-sites-in-new-admin-center) fornece diretrizes sobre como classificar e filtrar sites e como pesquisar um site SharePoint site. Use isso para localizar URLs para inserir no campo de pesquisa **no painel SharePoint submenu de sites**.
> - Teams chats e canais: [Get-Team](/powershell/module/teams/get-team) mostra como encontrar equipes no Microsoft Teams fornecendo informações ou propriedades específicas.
> - OneDrive urls e sites: sobre [OneDrive URLs do OneDrive](/onedrive/list-onedrive-urls#about-onedrive-urls) fornece informações sobre o formato e as propriedades apropriados para a URL de OneDrive usuário. Use isso para ajudá-lo a identificar OneDrive sites em sua pesquisa.

5. Na página **Definir configurações de pesquisa** , você pode optar por fazer alterações na pesquisa padrão escolhendo entre várias opções de pesquisa avançada. Aqui é onde você também pode optar por obter uma estimativa primeiro antes que os dados sejam retornados automaticamente. Se você escolher qualquer uma dessas opções, ao selecionar **Avançar** , prosseguirá para telas adicionais. Obtenha detalhes em [Definir configurações de pesquisa](#defining-search-settings) abaixo. Se você não quiser alterar a pesquisa, deixe todas as opções em branco e selecione **Avançar** para avançar para o próximo estágio.

6. Na página **Selecionar o tipo de solicitação**, escolha o tipo de solicitação: **Acesso**, **Exportação** ou Lista marcada para **acompanhamento (**[consulte as descrições acima](#request-types)). Indique se a solicitação pertence a uma regulamentação de privacidade de dados. Examine ou faça alterações no prazo de conclusão, que assume como padrão duas semanas após a data de criação da solicitação. Em seguida, selecione **Avançar**.

7. Na página **Confirmar ou editar** o nome desta solicitação, você pode manter ou editar o nome amigável fornecido para a solicitação e inserir uma descrição opcional. Em seguida, selecione **Avançar**.

8. Na página **Examinar e** concluir, examine o resumo do que você inseriu durante as etapas anteriores. Qualquer campo pode ser editado selecionando o **link Editar** em cada seção. Quando terminar, selecione Criar **solicitação**.

Você verá uma tela de confirmação depois que a solicitação for criada. Selecione **Concluído para** retornar à tela principal solicitações de direitos de entidade. A nova solicitação será listada na parte superior da lista de solicitações. Selecione-o na lista para começar a revisar e trabalhar nos estágios de progresso.

#### <a name="what-happens-after-your-request-is-created"></a>O que acontece depois que sua solicitação é criada

Calcularemos uma estimativa da quantidade de dados que ele espera encontrar com base em seus parâmetros de pesquisa começar imediatamente. Visite a página de detalhes da solicitação em alguns minutos ou uma hora para ver os resultados da estimativa e se a solicitação foi movida para o próximo estágio. Sua solicitação avançará automaticamente da estimativa **de** dados para a **recuperação de** dados, exceto nas seguintes circunstâncias:

 - Se você tiver selecionado para receber um esimtae de dados primeiro na Etapa 5, defina as configurações de pesquisa, poderá exibir detalhes sobre sua pesquisa e fazer alterações na pesquisa antes que todos os dados sejam **recuperados**. Você precisará avançar manualmente para o próximo estágio da recuperação de  dados se tiver pausado na estimativa **de dados**.
 
 - Se você não optar por parar na estimativa de dados, mas prevermos que sua pesquisa produzirá um grande volume de dados, você verá uma barra de mensagens na parte superior da solicitação com um link para editar sua pesquisa antes de prosseguir para a recuperação de **dados.**

Visite [a estimativa e a recuperação de dados](subject-rights-requests-data-retrieval.md)para saber mais sobre esses estágios.

## <a name="defining-search-settings"></a>Definindo configurações de pesquisa

Quando você cria uma solicitação de direitos de entidade, uma pesquisa padrão será executada com base em suas  seleções na página Locais do assistente de criação. Se você quiser realizar uma pesquisa mais direcionada ou se quiser optar por obter uma estimativa dos dados antes que os itens de conteúdo sejam recuperados, poderá fazer essas seleções na página De configurações de pesquisa do assistente de criação de solicitação.

### <a name="advanced-search-options"></a>Opções de pesquisa avançada

- **Refinar sua pesquisa**: essa opção permite que você especifique propriedades extras para ajudar a identificar o titular dos dados entre os dados da sua organização. Depois de escolher essa opção, você será solicitado a adicionar mais parâmetros de pesquisa, explicados abaixo [em Refinando sua pesquisa](#refining-your-search).
- **Incluir conteúdo criado pelo titular dos** dados: essa opção procurará o conteúdo que foi criado pelo titular dos dados. Os exemplos incluem arquivos criados ou carregados para SharePoint pelo titular dos dados. Selecionar essa opção pode aumentar significativamente a quantidade de dados retornados.
- **Incluir todas as** versões de itens: se você selecionou SharePoint como um local de pesquisa, a consulta de pesquisa padrão retornará apenas a versão atual SharePoint itens. A marcação dessa caixa retornará as versões atuais e todas as versões anteriores SharePoint itens, visando uma quantidade significativamente maior de dados a serem examinados.

> [!TIP]
> Você pode optar por carregar material adicional para habilitar Priva identificar titulares de dados com base em valores de dados exatos. Para saber mais, confira [Correspondência de dados para solicitações de direitos de entidade](subject-rights-requests-data-match.md).

### <a name="data-estimate"></a>Estimativa de dados

A **primeira opção Obter uma estimativa** apresentará uma estimativa de quantos dados esperamos encontrar antes que seus dados são recuperados automaticamente. Quando sua estimativa é exibida na página de detalhes da solicitação, você pode optar por exibir os resultados da pesquisa e visualizar uma amostragem de itens que foram descobertos. Se os itens representarem os resultados esperados, você precisará selecionar Recuperar  dados para continuar com a recuperação real de itens de conteúdo. Obtenha mais detalhes sobre o estágio de [estimativa de dados](subject-rights-requests-data-retrieval.md).

## <a name="refining-your-search"></a>Refinando sua pesquisa

Se você escolher Refinar sua pesquisa na página  De configurações de Pesquisa ou se tiver pausado no estágio de estimativa  de dados e optar por editar a consulta de pesquisa, será solicitado que você forneça detalhes sobre atributos pessoais e condições para direcionar ainda mais os resultados da pesquisa. Você pode fazer adições em uma ou em ambas as categorias. Quando você terminar de fazer seleções nesta seção, a recuperação de dados para a solicitação será baseada em suas configurações de pesquisa.

Os detalhes explicados abaixo também são o que você será solicitado a fornecer se tiver pausado no estágio de estimativa  de dados e optar por editar a consulta de pesquisa. 

#### <a name="add-personal-attributes"></a>Adicionar atributos pessoais

Insira valores nos campos de texto para os nomes, apelidos, endereços de email e endereço do titular dos dados. Você pode adicionar outros identificadores, como data de nascimento ou número de telefone, e os campos de texto dão suporte a várias entradas separadas por ponto e vírgula. Quando terminar, selecione Avançar **para** continuar na **página Condições** .

#### <a name="conditions"></a>Condições

Selecione o  botão Adicionar condição para escolher entre um intervalo de condições para direcionar ainda mais sua pesquisa, incluindo nome do item, nomes de remetente e destinatário, tipo de dados pessoais e se o item foi compartilhado externamente fora da sua organização. Os campos de texto dão suporte a várias entradas separadas por ponto e vírgula. Quando terminar, selecione Avançar **para salvar as** configurações de pesquisa e o progresso para a configuração do tipo de solicitação.

## <a name="next-steps"></a>Próximas etapas

Depois de criar sua solicitação, você a verá listada na página de solicitação de direitos de assunto. Para saber mais sobre como prosseguir com a revisão, consulte [Examinar dados e colaborar em solicitações](subject-rights-requests-data-review.md).

## <a name="legal-disclaimer"></a>Aviso de isenção de responsabilidade legal

[Microsoft Priva aviso de isenção de responsabilidade legal](priva-disclaimer.md)
