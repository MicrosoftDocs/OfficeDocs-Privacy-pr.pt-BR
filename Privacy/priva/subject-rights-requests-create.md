---
title: Criar uma solicitação de direitos de entidade
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
description: Saiba como criar uma nova solicitação de direitos de entidade no Microsoft Priva.
ms.openlocfilehash: b2d846aa4020be315705bbd16e00378c7514146c
ms.sourcegitcommit: 09ecdaded9a9f8f79587f2acb978dc53b83e5c01
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/19/2022
ms.locfileid: "64930602"
---
# <a name="create-a-subject-rights-request"></a>Criar uma solicitação de direitos de entidade

Os administradores de gerenciamento de direitos de entidade podem abrir novas solicitações por meio da página principal Solicitações de Direitos de Entidade da Priva. Um assistente orientará você pelo processo de encontrar dados pessoais sobre um titular de dados e iniciar o processo de atendimento à solicitação.

Você também pode optar por carregar material adicional para permitir que Priva identifique os titulares dos dados com base nos valores de dados fornecidos exatos. Para saber mais, confira [Correspondência de dados para solicitações de direitos de entidade](subject-rights-requests-data-match.md).

## <a name="request-types"></a>Tipos de solicitação

As Solicitações de Direitos de Assunto Priva dão suporte a três tipos diferentes de solicitações:

1. **Acesso**: fornece um resumo das informações pessoais do titular dos dados mantidos por sua organização em Microsoft 365.

2. **Exportação**: fornece um resumo e um arquivo exportado de itens de conteúdo que contêm as informações pessoais do titular dos dados. Esses são os itens revisados e marcados como **Incluídos** durante a revisão dos dados coletados pelas configurações de pesquisa.

3. **Lista marcada para acompanhamento**: gera um resumo de todos os arquivos que foram marcados durante a revisão de dados que podem exigir ação adicional fora de Priva. Por exemplo, talvez seja necessário facilitar a exclusão das informações pessoais do titular dos dados de acordo com sua solicitação. Você pode exibir as marcas incluídas e configurar marcas personalizadas para sua organização nas [configurações de Priva](priva-settings.md).

## <a name="use-the-subject-rights-request-creation-wizard"></a>Usar o assistente de criação de solicitação de direitos de entidade

1. No [portal de conformidade do Microsoft Purview](https://compliance.microsoft.com/), acesse a seção Priva e selecione **Priva Subject Rights Requests**.
1. Para iniciar uma nova solicitação, selecione **Criar uma solicitação**.
1. Identifique o titular dos dados que fez a solicitação e especifique sua relação com sua empresa.
1. Executaremos uma pesquisa padrão para itens relacionados ao titular dos dados. Se você quiser refinar sua pesquisa ou obter uma estimativa antes de recuperarmos dados, poderá fazer essas seleções neste estágio. Você também pode deixar todos os itens em branco e passar para a próxima etapa. Para obter mais informações sobre suas opções, consulte [Definir configurações de pesquisa](#define-search-settings) e [Refinar sua pesquisa](#refine-your-search).
1. Escolha um tipo de solicitação com base no que o titular dos dados deseja que você faça com seus dados. Se a solicitação estiver relacionada a uma regulamentação de privacidade de dados específica, você também poderá selecioná-la em uma lista fornecida para adicionar mais contexto. A definição de um prazo (obrigatório) facilita a classificação para se aproximar ou substituir solicitações e resolvê-las em tempo hábil. Os tipos de solicitação incluem:
   - **Acesso**: fornece um resumo das informações pessoais do titular dos dados mantidos por sua organização em Microsoft 365.
   - **Exportação**: fornece um resumo e uma exportação das informações pessoais do titular dos dados, conforme coletado e anotado durante a revisão.
   - **Lista marcada para acompanhamento**: gera um resumo de todos os arquivos que os usuários marcam durante a revisão que podem exigir ação adicional fora de Priva. Por exemplo, talvez seja necessário facilitar a exclusão das informações pessoais do titular dos dados de acordo com a solicitação. As marcas de revisão de dados personalizadas para solicitações de direitos de entidade podem ser gerenciadas em Configurações **.**
1. Confirme o nome dessa solicitação e adicione uma descrição opcional para referência.
1. Examine o resumo do que você inseriu durante as etapas anteriores. Qualquer campo pode ser editado antes de selecionar **Criar solicitação**.

Para cada solicitação de direitos de entidade, você pode definir sua pesquisa para procurar dados em todos os locais ou locais específicos no Exchange e no Sharepoint. Escolha um local movendo seu botão de alternância para a **posição** Ativado. Você pode optar por pesquisar todas as contas e sites ou designar contas ou sites específicos em cada local. Leia os detalhes abaixo sobre o que é abordado em cada local.

- **Exchange**: essa opção procurará dados em caixas de correio Exchange e em chats individuais ou Teams grupo. Você pode optar por pesquisar todas as Exchange em sua organização ou selecionar Escolher contas para  selecionar usuários individuais no painel de submenu Exchange **caixas** de correio.

- **SharePoint**: essa opção procurará dados em sites SharePoint, sites OneDrive for Business e Teams canais. Você pode optar por pesquisar todos SharePoint sites em sua organização ou selecionar Escolher **sites** para selecionar usuários individuais no painel de submenu SharePoint **sites**.

Para obter ajuda com a identificação dos termos de pesquisa apropriados, consulte os seguintes tópicos:

- **SharePoint sites e URLs**: gerenciar sites no centro de administração do [SharePoint](/sharepoint/manage-sites-in-new-admin-center) fornece diretrizes sobre como classificar e filtrar sites e como pesquisar um site SharePoint site. Use isso para localizar URLs para inserir no campo de pesquisa **no painel SharePoint submenu de sites**.

- **Teams chats e** canais: [Get-Team](/powershell/module/teams/get-team) mostra como encontrar equipes no Microsoft Teams fornecendo informações ou propriedades específicas.

- **OneDrive urls** e sites: sobre [urLs do OneDrive](/onedrive/list-onedrive-urls#about-onedrive-urls) fornece informações sobre o formato e as propriedades adequados para a URL de OneDrive usuário. Use isso para ajudá-lo a identificar OneDrive sites em sua pesquisa.

Recomendamos examinar cuidadosamente suas seleções para garantir que você identifique o assunto de dados correto. Por exemplo, se você pesquisar caixas de correio por nome e encontrar várias pessoas com nomes semelhantes, verifique a correta antes de adicioná-las à sua solicitação.

## <a name="define-search-settings"></a>Definir configurações de pesquisa

Quando você cria uma solicitação de direitos de entidade, uma pesquisa padrão será executada com base em suas  seleções na página Locais do assistente de criação. Se você quiser realizar uma pesquisa mais direcionada ou se quiser optar por obter uma estimativa dos dados antes que os itens de conteúdo sejam recuperados, poderá fazer essas seleções na página De configurações de pesquisa do assistente de criação de solicitação.

### <a name="advanced-search-options"></a>Opções de pesquisa avançada

- **Refinar sua pesquisa**: essa opção permite que você especifique propriedades adicionais para ajudar a identificar o titular dos dados entre os dados da sua organização. Depois de escolher essa opção, você será solicitado a adicionar mais parâmetros de pesquisa, explicados abaixo [em Refinar sua pesquisa](#refine-your-search).
- **Incluir conteúdo criado pelo titular dos** dados: essa opção procurará o conteúdo que foi criado pelo titular dos dados. Os exemplos incluem arquivos criados ou carregados para SharePoint pelo titular dos dados. Selecionar essa opção pode aumentar significativamente a quantidade de dados retornados.
- **Incluir todas as** versões de itens: se você selecionou SharePoint como um local de pesquisa, a consulta de pesquisa padrão retornará apenas a versão atual SharePoint itens. A marcação dessa caixa retornará as versões atuais e todas as versões anteriores SharePoint itens, visando uma quantidade significativamente maior de dados a serem examinados.

### <a name="data-estimate"></a>Estimativa de dados

A **primeira opção Obter uma estimativa** apresentará uma estimativa de quantos dados esperamos encontrar antes que seus dados são recuperados automaticamente. Quando sua estimativa é exibida na página de detalhes da solicitação, você pode optar por exibir os resultados da pesquisa e visualizar uma amostragem de itens que foram descobertos. Se os itens representarem os resultados esperados, você precisará selecionar Recuperar  dados para continuar com a recuperação real de itens de conteúdo.

## <a name="refine-your-search"></a>Refinar sua pesquisa

Se você escolher **Refinar** sua pesquisa na página  De configurações de pesquisa, ao selecionar  Avançar, você será solicitado a fornecer detalhes sobre atributos pessoais e condições para direcionar ainda mais os resultados da pesquisa. Você pode fazer adições em uma ou em ambas as categorias. Quando você terminar de fazer seleções nesta seção, a recuperação de dados para a solicitação será baseada em suas configurações de pesquisa.

#### <a name="add-personal-attributes"></a>Adicionar atributos pessoais

Insira valores nos campos de texto para os nomes, apelidos, endereços de email e endereço do titular dos dados. Você pode adicionar outros identificadores, como data de nascimento ou número de telefone, e os campos de texto dão suporte a várias entradas separadas por ponto e vírgula. Quando terminar, selecione Avançar **para** continuar na **página Condições** .

#### <a name="conditions"></a>Condições

Selecione o  botão Adicionar condição para escolher entre um intervalo de condições para direcionar ainda mais sua pesquisa, incluindo nome do item, nomes de remetente e destinatário, tipo de dados pessoais e se o item foi compartilhado externamente fora da sua organização. Os campos de texto dão suporte a várias entradas separadas por ponto e vírgula. Quando terminar, selecione Avançar **para salvar as** configurações de pesquisa e o progresso para a configuração do tipo de solicitação.

## <a name="next-steps"></a>Próximas etapas

Depois de criar sua solicitação, você a verá listada na página de solicitação de direitos de assunto. Para saber mais sobre como prosseguir com a revisão, consulte [Examinar dados e colaborar em solicitações](subject-rights-requests-data-review.md).

## <a name="legal-disclaimer"></a>Aviso de isenção de responsabilidade legal

[Aviso de isenção de responsabilidade legal da Microsoft Priva](priva-disclaimer.md)
