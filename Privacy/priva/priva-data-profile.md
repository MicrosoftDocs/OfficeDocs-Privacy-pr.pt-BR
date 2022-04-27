---
title: Localizar e visualizar dados pessoais no Microsoft Priva
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
- M365-priva-subject-rights-requests
search.appverid:
- MOE150
- MET150
description: Saiba mais sobre a visão geral e o perfil de dados em Priva e como obter insights sobre os dados pessoais no ambiente de Microsoft 365 da sua organização.
ms.openlocfilehash: e09becfbbd64128f44ef6d1d29fc367850f13411
ms.sourcegitcommit: bbaa4400bc9c7db9bdb2784e3af160daf5d08290
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2022
ms.locfileid: "65059745"
---
# <a name="find-and-visualize-personal-data-in-microsoft-priva"></a>Localizar e visualizar dados pessoais no Microsoft Priva

O Microsoft Priva ajuda você a entender os dados que sua organização armazena automatizando a descoberta de ativos de dados pessoais e fornecendo visualizações de informações essenciais. Essas visualizações podem ser encontradas nas páginas de visão **geral** e **perfil de** dados. Você pode agir sobre os insights aqui para fortalecer a postura de privacidade da sua organização e reduzir o risco.

Para começar, acesse a seção Priva do [portal de conformidade do Microsoft Purview](https://compliance.microsoft.com/) e exiba estas páginas:

- **Visão** geral: fornece uma visão geral dos dados da sua organização Microsoft 365. Os administradores de privacidade podem monitorar tendências e atividades, identificar e investigar possíveis riscos envolvendo dados pessoais e implantar ações importantes, como gerenciamento de políticas ou ações de solicitação de direitos de entidade.
- **Perfil de** dados: fornece um instantâneo dos dados pessoais que sua organização armazena Microsoft 365. Esta página ajuda você a visualizar onde residem os dados pessoais, quais tipos são os mais predominantes em sua organização e quantos tipos diferentes existem entre locais em seu Microsoft 365 ambiente. Você também pode explorar dados pessoais desse local.

À medida que seus dados forem alterados e Priva fizer novas descobertas, as informações mostradas nessas páginas serão atualizadas. Observe que pode levar até 24 horas para que novos dados sejam representados nos gráficos.

## <a name="explore-the-overview-page"></a>Explorar a página de visão geral

A página de visão geral consiste em três seções principais. Os blocos na parte superior da página fornecem estatísticas recentes essenciais sobre seus dados. A seção de insights principais fornece oportunidades de investigação sobre tendências e áreas de interesse principal. Para obter mais perspectiva sobre seu ambiente de dados, consulte os gráficos de linha de tendência. Para saber mais sobre essas áreas, consulte as seções abaixo.

![Página de visão geral de exemplo.](../media/priva-overview.png)

### <a name="top-tiles"></a>Blocos principais

#### <a name="policy-matches-over-past-7-days"></a>A política corresponde aos últimos 7 dias

Quando as políticas são definidas no Gerenciamento de Riscos de Privacidade de Priva, seus dados serão avaliados com base em suas políticas para determinadas condições que podem apresentar riscos de privacidade. As combinações de política indicam descobertas de dados que podem precisar de mais revisão ou correção. Este bloco mostra quantas partidas de política ocorreram nos últimos sete dias. As correspondeções serão exibidas aqui se as políticas estão ativadas ou em execução no modo de teste, para que você possa ver os resultados de todas as suas políticas ativas. Selecionar esse bloco levará você a uma exibição filtrada da página Políticas  de Gerenciamento de Risco de Privacidade, mostrando as políticas que tiveram uma correspondência nos últimos sete dias.

#### <a name="items-with-personal-data"></a>Itens com dados pessoais

Para ver os recursos de descoberta automatizada da Priva no trabalho, examine os **Itens com o bloco de dados** pessoais. Este bloco mostra quantos novos itens que contêm dados pessoais com base em suas configurações foram descobertos no ambiente de Microsoft 365 da sua organização nos últimos sete dias. Selecionar esse bloco carregará uma exibição dos 100 itens mais recentes descobertos.

#### <a name="subject-rights-requests"></a>Solicitações de direitos de entidade

A página de visão geral inclui um bloco que mostra quantas solicitações de direitos de entidade foram criadas nos últimos sete dias. Um segundo bloco, se aplicável, mostra quantas solicitações estão vencidas com base nos prazos designados e pode precisar de atenção imediata. Selecionar esses blocos levará os usuários com as permissões apropriadas para a página de solicitação de direitos de entidade de Priva.

### <a name="key-insights"></a>Principais insights

#### <a name="content-items-with-the-most-personal-data"></a>Itens de conteúdo com os dados mais pessoais

O conteúdo que contém uma grande quantidade de dados pessoais pode apresentar um risco maior de exposição. Talvez você queira examinar esses itens para garantir que eles sejam cobertos por uma política de Gerenciamento de Riscos de Privacidade. Para ajudar a chamar a atenção desses itens, a página de visão geral fornece uma exibição dos itens de conteúdo que contêm os dados mais pessoais de acordo com suas configurações. Aqui, você pode ver o número de tipos de dados pessoais exclusivos detectados, quantos proprietários de conteúdo exclusivos foram identificados e quantos titulares de dados foram identificados de acordo com as configurações de correspondência de dados para solicitações de direitos de entidade.

Selecione **Exibir resumo** para uma exibição de resumo dos itens encontrados. Você também pode optar por **Explorar essas descobertas** para visualizar arquivos individuais. Essa exibição mostra um máximo de 100 itens. Os usuários no grupo de função Gerenciamento de Privacidade podem selecionar arquivos para examinar detalhes e determinar a relevância e exportar a lista no formato .csv para referência.

#### <a name="policies-with-the-most-matches-in-the-last-week"></a>Políticas com mais partidas na última semana

Esse insight mostra quais políticas foram correspondidas com mais frequência nos últimos sete dias, seja no modo "Ativado" ou "Teste". Ele ajuda a ilustrar o desempenho de suas políticas e os efeitos do trabalho contínuo à medida que seus usuários Priva refinam seus comportamentos de privacidade.

Selecione **Exibir resumo** para obter um resumo das 10 principais políticas correspondentes e os proprietários de conteúdo do conteúdo associado. Você também verá quantas notificações de usuário foram enviadas devido a essas correspondentes de política e ao número de ações do usuário executadas. Selecione **Investigar** para exibir a página Políticas no Gerenciamento de Riscos de Privacidade, filtrada para mostrar as políticas da exibição de resumo. Essa exibição investigativa mostrará estatísticas para o tempo de vida completo da política. Selecione-o para ver detalhes, como quando itens correspondentes foram detectados inicialmente.

#### <a name="users-with-the-most-policy-matched-in-the-last-week"></a>Usuários com a política mais correspondida na última semana

Esse insight também aborda as correspondentes de políticas no modo "Testando" ou "Ativado". Ele permite exibir um resumo dos usuários com mais correspondências de política na última semana e quais políticas eles correspondem. Isso inclui totais dos proprietários de conteúdo exclusivos, notificações enviadas a esses usuários e quantas ações foram executadas dessas notificações. Selecionar **Investigar** leva você para a página de políticas, filtrada para mostrar as políticas da exibição de resumo. No modo de exibição de investigação, você não encontrará informações do usuário, mas poderá selecionar uma política para ver os detalhes da política relacionados a essas partidas.

#### <a name="items-with-the-most-data-subject-content"></a>Itens com mais conteúdo de assunto de dados

Esse insight exibe itens de conteúdo que contêm os dados pessoais da maioria dos titulares dos dados. Para receber esses insights, sua organização precisa configurar a correspondência de dados [para solicitações de direitos de entidade](subject-rights-requests-data-match.md).

Esses itens podem ajudar a confirmar a configuração de correspondência de dados e a reduzir os riscos de privacidade relacionados a esses itens. Selecione **Exibir resumo para** uma exibição de resumo. Selecione **Explorar** para obter uma exibição detalhada de até 100 desses itens. Aqui, você pode visualizar esses itens e determinar a relevância e exportar a lista .csv formato.

### <a name="trendline-graphs"></a>Gráficos de linha de tendência

Para visualizações dinâmicas de tendências encontradas nos dados da sua organização, consulte os gráficos de linha de tendência. Esses grafos podem ser filtrados por características como intervalos de tempo, tipo de dados ou locais de dados. Use as listas suspensas fornecidas para ajustar o modo de exibição. Passar o mouse sobre linhas no grafo permitirá que você veja estatísticas relacionadas a esse ponto específico no tempo.

Os resultados relacionados às políticas incluirão dados de políticas nos modos "Testando" e "Ativado". Se nenhuma política de um tipo específico estiver ativa, os grafos relacionados não mostrarão nenhum resultado.

#### <a name="active-policy-alerts"></a>Alertas de política ativa

Essa área mostra um instantâneo de alertas ativos disparados por corresponde à política. Ao longo do tempo, essa exibição pode ajudá-lo a detectar com mais facilidade anormalidades como grandes picos no volume. Selecione **Exibir alertas para** navegar até a página de políticas no Gerenciamento de Riscos de Privacidade, em que você pode investigar ainda mais os alertas e criar problemas para correção.

#### <a name="personal-data-found-in-organization"></a>Dados pessoais encontrados na organização

Esse grafo mostra tendências de quantos dados pessoais que correspondem às suas configurações foram descobertos ao longo do tempo em seu ambiente Microsoft 365 e onde estão localizados. Ele começará a ser preenchido depois que Priva estiver em execução por tempo suficiente e depois que o conteúdo com dados pessoais for encontrado em SharePoint, OneDrive, Teams e/ou Exchange.

#### <a name="data-transfers-detected-in-organization"></a>Transferências de dados detectadas na organização

Esse grafo está relacionado a políticas de transferência de dados. Ele fornece uma visão de como os dados estão se movendo em sua organização, entre departamentos ou entre regiões para organizações multigeométricas.

#### <a name="unused-personal-data"></a>Dados pessoais não utilizados

Esse grafo está relacionado às políticas de minimização de dados. Ele fornece informações sobre como sua organização está armazenando conteúdo que contém dados pessoais e como suas políticas podem melhorar a manipulação desses dados ao longo do tempo.

#### <a name="overexposed-personal-data"></a>Dados pessoais sobrepostos

Esse grafo está relacionado a políticas de superexposição de dados. Ele pode ajudá-lo a identificar comportamentos de compartilhamento ao longo do tempo em sua organização e locais em que o conteúdo com dados pessoais pode ser sobreposto, por exemplo, sendo compartilhado publicamente, compartilhado com um usuário externo ou compartilhado amplamente em sua organização.

#### <a name="subject-rights-requests-by-regulation"></a>Solicitações de direitos de entidade por regulamentação

Essa exibição fornece informações sobre quais regulamentos mais predominantemente orientam suas solicitações de direitos de assunto ao longo do tempo. A legenda desse grafo mostra os nomes dos regulamentos mais populares. Passar o mouse sobre as linhas de tendência mostrará os totais de solicitações de direitos de entidade abertas para essa regulamentação durante o tempo selecionado.

#### <a name="subject-rights-requests-by-status"></a>Solicitações de direitos de entidade por status

Esse grafo exibe como sua organização está se saindo com a conclusão de solicitações de direitos de entidade, divididas em solicitações que estão ativas **, fechadas** ou **vencidas**.  As descobertas aqui podem ajudar a indicar onde você pode se beneficiar da alocação de mais recursos para fechar suas solicitações e destinos de reunião.

### <a name="additional-data-views"></a>Exibições de dados adicionais

#### <a name="subject-rights-requests-at-a-glance"></a>Solicitações de direitos de entidade em um relance

Essa exibição fornece uma exibição de alto nível das solicitações de direitos de entidade ativas, incluindo o tempo restante para concluir solicitações até seus prazos. Ele resume quantas solicitações totais você tem, quantas estão ativas e quantas estão fechadas. Selecione **Exibir todas as solicitações** para ir para a página de solicitação de direitos de entidade, na qual você pode exibir mais detalhes e trabalhar nas solicitações ativas para progridi-las até a conclusão.

#### <a name="subject-rights-requests-by-residency"></a>Solicitações de direitos de entidade por residência

Essa exibição de mapa ajuda você a visualizar seu volume de solicitações de direitos de entidade pela residência dos titulares dos dados. Passar o mouse sobre uma bolha identificará a região e o total de solicitações de direitos de entidade abertas em nome dos moradores da região.

## <a name="explore-the-data-profile-page"></a>Explorar a página de perfil de dados

A página de perfil de dados em Priva fornece uma exibição de instantâneo dos dados pessoais que sua organização armazena Microsoft 365 e onde eles residem. Ele também fornece informações sobre os tipos de dados armazenados. Os blocos principais incluem o seguinte.

![Página de perfil de dados de exemplo.](../media/priva-dataprofile.png)

### <a name="personal-data-type-instances-detected-in-microsoft-365"></a>Instâncias de tipo de dados pessoais detectadas no Microsoft 365

Esse bloco ajuda você a visualizar a quantidade de dados pessoais existentes em seu ambiente do Microsoft 365 com base em suas configurações e como esses dados são distribuídos entre Exchange, OneDrive, SharePoint e Teams.

O gráfico de barras mostra a contagem agregada aproximada de instâncias de tipo de dados pessoais exclusivas encontradas em seu conteúdo. Exemplos de tipos de dados podem incluir itens como números de cartão de crédito e números de seguro social. Portanto, um arquivo descoberto que contém três números de cartão de crédito e um número de seguro social conteria dois tipos de dados pessoais exclusivos e quatro instâncias. A parte inferior desse bloco mostra os tipos de dados pessoais exclusivos em cada Microsoft 365 local. Ele fornece uma visão da diversidade de tipos de dados pessoais detectados no conteúdo da sua organização.

### <a name="top-personal-data-types-across-your-organization"></a>Principais tipos de dados pessoais em sua organização

Esse bloco fornece um instantâneo dos principais tipos de dados pessoais detectados em seu ambiente, juntamente com informações sobre quantos itens contêm esse tipo de dados pessoal e em quais locais.

### <a name="personal-data-type-instances-by-region"></a>Instâncias de tipo de dados pessoais por região

Para ambientes multigeográficos, esse bloco agrega regionalmente instâncias de tipo de dados pessoais encontradas em seu conteúdo, com base nas regiões em que esse conteúdo está hospedado. Para organizações de região única, esse bloco mostrará um ponto que representa seu Microsoft 365 local. Passar o mouse sobre os pontos no mapa mostrará a contagem aproximada de instâncias de tipo de dados pessoais descobertas nessa região.

### <a name="exploring-content"></a>Explorando conteúdo

Selecionar **Explorar** em qualquer bloco de perfil de dados abrirá o explorador de conteúdo. No momento, você não pode pesquisar um item de conteúdo específico e não verá Teams dados nesta exibição. Isso significa que os números no explorador de conteúdo podem não corresponder aos números mostrados na página de perfil de dados, pois a página de perfil de dados inclui Teams conteúdo. Os administradores de privacidade que desejam obter mais informações sobre seus dados de privacidade podem fazer isso aqui com base no tipo de dados pessoais (tipo de informação confidencial) ou por local (Exchange, OneDrive ou SharePoint).

## <a name="legal-disclaimer"></a>Aviso de isenção de responsabilidade legal

[Aviso de isenção de responsabilidade legal da Microsoft Priva](priva-disclaimer.md)
