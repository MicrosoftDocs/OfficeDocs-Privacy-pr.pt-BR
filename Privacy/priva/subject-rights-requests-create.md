---
title: Criar uma solicitação de direitos de assunto
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
description: Saiba como criar uma nova solicitação de direitos de assunto no Microsoft Priva.
ms.openlocfilehash: 9de1047950a556b4456fd4453ea8d860a0a01c38
ms.sourcegitcommit: 16dd1c0320bf1c58ad75edbbe2113fc79013f504
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64404605"
---
# <a name="create-a-subject-rights-request"></a>Criar uma solicitação de direitos de assunto

Os administradores de gerenciamento de direitos de assunto podem abrir novas solicitações por meio da página principal solicitações de direitos de assunto de Priva. Um assistente o orientará durante o processo de encontrar dados pessoais sobre um titular de dados e iniciar o processo de atendimento de sua solicitação.

Você também pode optar por carregar material adicional para permitir que Priva identifique titulares de dados com base nos valores de dados fornecidos exatos. Para saber mais, confira [Correspondência de dados para Solicitações de Direitos de Assunto](subject-rights-requests-data-match.md).

## <a name="request-types"></a>Tipos de solicitação

As Solicitações de Direitos de Assunto Priva suportam três tipos diferentes de solicitações:

1. **Access**: fornece um resumo das informações pessoais do entidade de dados mantidas pela sua organização em Microsoft 365.

2. **Exportar**: fornece um resumo e um arquivo exportado de itens de conteúdo que contêm as informações pessoais do assunto de dados. Esses são os itens revisados e marcados como **Incluídos** durante a revisão dos dados coletados por suas configurações de pesquisa.

3. **Lista marcada para** acompanhamento: gera um resumo de todos os arquivos que foram marcados durante a revisão de dados que podem exigir ações adicionais fora de Priva. Por exemplo, talvez seja necessário facilitar a exclusão das informações pessoais do assunto de dados de acordo com a solicitação. Você pode exibir as marcas incluídas e configurar marcas personalizadas para sua organização nas [configurações priva](priva-settings.md).

## <a name="use-the-subject-rights-request-creation-wizard"></a>Usar o assistente de criação de solicitação de direitos de assunto

1. Na [Centro de conformidade do Microsoft 365,](https://compliance.microsoft.com/) selecione **Priva Subject Rights Requests** na navegação à esquerda.

2. No canto superior direito, selecione **Criar uma solicitação**.

3. Na página **Informações do assunto dados** , adicione o nome e sobrenome do assunto de dados, o endereço de email, o país de residência e especifique sua relação com sua empresa. Em seguida, selecione **Avançar**.

4. Na página **Locais**, escolha os Microsoft 365 locais onde você deseja procurar os dados pessoais do assunto de dados. Obter detalhes sobre [as configurações de local](#choose-locations). Quando terminar de escolher locais, selecione **Próximo.**

5. Na página **Configurações de** Pesquisa, você pode alterar as configurações de pesquisa para refinar sua pesquisa e escolher se deve primeiro obter uma estimativa antes de recuperar dados. Você não precisa escolher nenhuma opção nesta página, o que resulta em uma pesquisa padrão com base nos locais especificados na etapa anterior. Para obter mais informações sobre suas opções aqui, consulte [Definir configurações de pesquisa](#define-search-settings). Quando estiver pronto para continuar, selecione **Avançar**.

6. Na página **Tipo de** solicitação, escolha [](#request-types) um tipo de solicitação com base no que o assunto dos dados deseja que você faça com seus dados: **Access**, **Export** ou **Tagged list para acompanhamento**. Se a solicitação estiver relacionada a uma regulamentação específica de privacidade de dados, você também poderá selecioná-la em uma lista fornecida para adicionar mais contexto. Definir um prazo (obrigatório) facilita a classificação para solicitações de aproximação ou atraso e resolvê-las em tempo hábil. Quando terminar, selecione **Next**.

7. No nome **da solicitação**, confirme ou edite o nome dessa solicitação e adicione uma descrição opcional para referência. Em seguida, selecione **Avançar**.

8. Na página **Revisar e** concluir, revise suas seleções. Qualquer seção pode ser editada. Quando terminar, selecione **Criar solicitação**.

Sua solicitação terá sua própria página de detalhes e será listada na página principal solicitação de direitos de assunto. Depois de criar sua solicitação, Priva começará a procurar por corresponde às informações do assunto de dados fornecidas nos locais especificados. Pode levar vários minutos para mostrar uma estimativa de dados na página de detalhes da solicitação, dependendo do escopo da pesquisa.

## <a name="choose-locations"></a>Escolher locais

Para cada solicitação de direitos de assunto, você pode definir sua pesquisa para procurar dados em todos ou locais específicos no Exchange e no Sharepoint. Escolha um local movendo sua opção de alternância para a **posição On** . Você pode optar por pesquisar todas as contas e sites ou designar contas ou sites específicos em cada local. Leia detalhes abaixo sobre o que é abordado em cada local.

- **Exchange**: essa opção procurará dados em caixas de correio Exchange e em chats individuais ou Teams grupo. Você pode optar por pesquisar todas as Exchange em sua organização ou selecionar Escolher contas para  selecionar usuários individuais no painel de Exchange  de caixas de correio.

- **SharePoint**: essa opção procurará dados em sites SharePoint, sites OneDrive for Business sites e Teams canais. Você pode optar por pesquisar todos os SharePoint em sua organização ou selecionar Escolher **sites** para selecionar usuários individuais no painel de SharePoint **de sites**.

Para ajudar a identificar os termos de pesquisa apropriados, consulte os seguintes tópicos:

- **SharePoint e URLs**: Gerenciar sites no centro de administração do [SharePoint](/sharepoint/manage-sites-in-new-admin-center) fornece orientações sobre como classificar e filtrar sites e como pesquisar um site SharePoint. Use isso para encontrar URLs para inserir no campo de pesquisa no painel de SharePoint **de sites**.

- **Teams chats e canais**: [Get-Team](/powershell/module/teams/get-team) mostra como encontrar equipes no Microsoft Teams fornecendo propriedades ou informações específicas.

- **OneDrive e URLs**: Sobre OneDrive [URLs](/onedrive/list-onedrive-urls#about-onedrive-urls) fornece informações sobre o formato e as propriedades apropriados para a URL de OneDrive do usuário. Use isso para ajudá-lo a identificar OneDrive sites em sua pesquisa.

Recomendamos revisar cuidadosamente suas seleções para garantir que você identifique o assunto de dados correto. Por exemplo, se você pesquisar caixas de correio pelo nome e encontrar vários indivíduos com nomes semelhantes, verifique a correta antes de adi adiá-las à sua solicitação.

## <a name="define-search-settings"></a>Definir configurações de pesquisa

Quando você cria uma solicitação de direitos de assunto, uma pesquisa padrão será executado com base em suas seleções na página **Locais** do assistente de criação. Se você quiser conduzir uma pesquisa mais direcionada ou se quiser obter uma estimativa dos dados antes que os itens de conteúdo sejam recuperados, você pode fazer essas seleções na página Configurações de  Pesquisa do assistente de criação de solicitação.

### <a name="advanced-search-options"></a>Opções avançadas de pesquisa

- **Refine sua pesquisa**: essa opção permite especificar propriedades adicionais para ajudar a identificar o titular dos dados entre os dados da sua organização. Depois de escolher essa opção, você será solicitado a adicionar mais parâmetros de pesquisa, explicados abaixo [em Refinar sua pesquisa](#refine-your-search).
- **Incluir conteúdo de autoria do assunto de** dados: essa opção procurará conteúdo que tenha sido de autoria do assunto de dados. Exemplos incluem arquivos criados ou carregados SharePoint, o assunto de dados. Selecionar essa opção pode aumentar significativamente a quantidade de dados retornados.
- **Inclua todas as** versões de itens: se você selecionou SharePoint como um local de pesquisa, a consulta de pesquisa padrão retornará apenas a versão atual dos SharePoint itens. A verificação dessa caixa retornará as versões atuais e todas as versões anteriores de itens SharePoint, o que gerará uma quantidade significativamente maior de dados para você revisar.

### <a name="data-estimate"></a>Estimativa de dados

A **opção Obter uma primeira** estimativa apresentará uma estimativa de quantos dados esperamos encontrar antes que seus dados são recuperados automaticamente. Quando sua estimativa é exibida na página de detalhes da solicitação, você pode optar por exibir os resultados da pesquisa e visualizar uma amostra de itens que foram descobertos. Se os itens representarem os resultados esperados, você precisará selecionar **Recuperar** dados para continuar com a recuperação real de itens de conteúdo.

## <a name="refine-your-search"></a>Refinar sua pesquisa

Se você escolher **Refinar** sua pesquisa na página  Configurações de Pesquisa, ao selecionar **Avançar**, você será solicitado a fornecer detalhes para atributos pessoais e condições para direcionar ainda mais seus resultados de pesquisa. Você pode fazer adições em ambas as categorias. Quando você terminar de fazer seleções nesta seção, a recuperação de dados para a solicitação será baseada em suas configurações de pesquisa.

#### <a name="add-personal-attributes"></a>Adicionar atributos pessoais

Insira valores nos campos de texto para os nomes, apelidos, endereços de email e endereço do assunto de dados. Você pode adicionar outros identificadores, como data de nascimento ou número de telefone, e campos de texto suportam várias entradas separadas por um ponto e vírgula. Quando terminar, selecione **Próximo** para continuar na **página Condições** .

#### <a name="conditions"></a>Condições

Selecione o **botão Adicionar condição** para escolher entre um intervalo de condições para direcionar ainda mais sua pesquisa, incluindo nome do item, nomes de remetente e destinatário, tipo de dados pessoais e se o item foi compartilhado externamente fora da sua organização. Os campos de texto suportam várias entradas separadas por um ponto e vírgula. Quando terminar, selecione **Avançar** para salvar suas configurações de pesquisa e progredir para a configuração de tipo de solicitação.

## <a name="next-steps"></a>Próximas etapas

Depois de criar sua solicitação, você a verá listada na página de solicitação de direitos de assunto. Para saber mais sobre como prosseguir com a revisão, consulte [Revisar dados e colaborar em solicitações](subject-rights-requests-data-review.md).

## <a name="legal-disclaimer"></a>Aviso de isenção de responsabilidade legal

[Aviso de isenção de responsabilidade legal da Microsoft Priva](priva-disclaimer.md)
