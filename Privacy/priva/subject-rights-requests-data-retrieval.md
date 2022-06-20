---
title: Estimativa e recuperação de dados em solicitações de direitos de entidade
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
description: Entenda como os dados são recuperados e como modificar as configurações de pesquisa Solicitações de direitos do titular Microsoft Priva.
ms.openlocfilehash: a2586e987f7a03905feedfd587aab43dba3d9e6b
ms.sourcegitcommit: 8cbafebb1a1b26a0bd92e500a1e6d6c60243c64b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/20/2022
ms.locfileid: "66166660"
---
# <a name="data-estimate-and-retrieval"></a>Estimativa e recuperação de dados

**Neste artigo**: entenda os estágios de estimativa de dados e recuperação de dados de uma solicitação de direitos de entidade. Saiba como exibir a consulta de pesquisa de uma solicitação e fazer edições para refinar a pesquisa.

## <a name="data-estimate"></a>Estimativa de dados
Depois de criar uma solicitação, Priva imediatamente começa a procurar por correspondentes ao titular dos dados no conteúdo em seu Microsoft 365 ambiente. Depois de identificarmos todos os itens que achamos que correspondem aos seus critérios, você verá a estimativa no cartão  de resumo de estimativa de dados na página Visão geral **da** solicitação. A quantidade de dados dentro do escopo da pesquisa afetará o tempo necessário para concluir a estimativa.

Sua solicitação será movida automaticamente para o próximo estágio da recuperação de **dados, em** que todos os itens de conteúdo são reunidos para que os stakeholders colaborem na revisão dos dados. Em alguns casos, pausamos a estimativa de dados antes de passar para a recuperação e o notificaremos das próximas etapas a serem seguidas antes de continuar.

### <a name="pause-in-data-estimate"></a>Pausar na estimativa de dados

Há dois motivos pelos quais uma solicitação será pausada no estágio **de estimativa de** dados:

1. Ao criar uma solicitação, você pode optar por obter uma estimativa primeiro. Consulte a etapa 6 da [criação de uma solicitação personalizada](subject-rights-requests-create.md#custom-setup-guided-process-to-choose-all-settings) para obter detalhes.

2. Se a estimativa for projetar para retornar um grande número de itens a serem examinados (mais de 10 mil itens), o fluxo de trabalho será pausado. Neste ponto, você pode visualizar os resultados e decidir se deseja [editar](subject-rights-requests-create.md#refining-your-search) a consulta de pesquisa ou continuar a recuperar os itens identificados.

Quando a solicitação for pausada na estimativa de **dados, você** verá um cartão na página de detalhes da solicitação com informações resumidas sobre o número de itens, volume, sua localização e um link que permite exibir detalhes da consulta de **pesquisa.**

![Cartão de estimativa de dados.](../media/priva-srr-data-estimate.png)

## <a name="view-and-edit-search-queries"></a>Exibir e editar consultas de pesquisa

Para ver informações detalhadas sobre a pesquisa da solicitação, selecione Exibir detalhes da consulta de **pesquisa no** **cartão de resumo de estimativa de** dados. Um painel de submenu é aberto, que resume a consulta e mostra mais detalhes sobre o que foi encontrado. A partir daqui, você tem as seguintes opções:

- Selecione **Visualizar resultados** para obter uma visualização do tipo de conteúdo que será retornado nas configurações de pesquisa atuais.
- Selecione **Editar consulta de pesquisa** para alterar as configurações de pesquisa.

Ao selecionar Editar consulta de **pesquisa, você** será levado por um processo guiado para alterar ou adicionar propriedades para identificar o assunto dos dados, alterar as condições e ajustar os locais que você deseja que a pesquisa acoberte. Siga as instruções em [Refinar sua pesquisa](subject-rights-requests-create.md#refining-your-search) para obter informações mais detalhadas. Você pode examinar a versão final da nova consulta de pesquisa e, em seguida, selecionar **Salvar** para iniciar a pesquisa novamente.

Uma nova estimativa será gerada e o status da solicitação voltará para a **estimativa de dados**. A nova pesquisa pode levar até 60 minutos para ser concluída. Quando terminar, você verá os resultados atualizados na página de detalhes da solicitação.

Quando estiver pronto para continuar, selecione Recuperar dados no  canto superior direito da tela para avançar para o estágio de recuperação de dados.

## <a name="retrieve-data"></a>Recuperar dados

O estágio de recuperação de dados é quando todos os arquivos, emails, chats, imagens e outros itens de conteúdo que contêm os dados pessoais do titular dos dados são recuperados. Os itens são colocados juntos em um contêiner Armazenamento de Blobs do Azure para revisão. A recuperação de dados pode levar alguns minutos ou significativamente mais, dependendo do volume de dados.

Quando esse estágio for concluído, a solicitação passará automaticamente para o próximo estágio dos **dados de revisão**.

## <a name="next-steps"></a>Próximas etapas

Visite [Examinar dados de uma solicitação de direitos de](subject-rights-requests-data-review.md) assunto para saber mais sobre as principais tarefas e colaborar com os stakeholders para a **etapa examinar dados** .

## <a name="legal-disclaimer"></a>Aviso de isenção de responsabilidade legal

[Microsoft Priva aviso de isenção de responsabilidade legal](priva-disclaimer.md)