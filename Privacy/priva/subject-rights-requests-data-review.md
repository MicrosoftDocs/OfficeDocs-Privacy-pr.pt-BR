---
title: Examinar dados de uma solicitação de direitos de entidade
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
description: Saiba como examinar os dados de solicitação de direitos de entidade coletados pelo Microsoft Priva e colaborar na conclusão da solicitação.
ms.openlocfilehash: f417ebe6129f877c273fc2613a44e6b4a21f0be0
ms.sourcegitcommit: 09ecdaded9a9f8f79587f2acb978dc53b83e5c01
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/19/2022
ms.locfileid: "64930632"
---
# <a name="review-data-for-a-subject-rights-request"></a>Examinar dados de uma solicitação de direitos de entidade

Depois de criar uma solicitação de direitos de [entidade (saiba](subject-rights-requests-create.md) mais) no Microsoft Priva, a solução Solicitações de Direitos de Entidade usará suas entradas para procurar correspondentes sobre o assunto dos dados no ambiente de Microsoft 365 da sua organização. Depois que esses dados forem compilados, você poderá examinar as descobertas, fazer escolhas sobre o que incluir e reabilitar as informações conforme necessário. Essas etapas podem ser colaboradas por vários usuários por meio da interface Priva.

## <a name="step-1-review-request-details-and-monitor-progress"></a>Etapa 1: Examinar os detalhes da solicitação e monitorar o progresso

Para ver os resultados iniciais da pesquisa, vá para a área Priva do portal de conformidade do [Microsoft Purview](https://compliance.microsoft.com/) e abra as **solicitações de direitos de entidade**. Uma lista de todas as solicitações de direitos de entidade abertas pode ser encontrada nesta página principal.

Selecione sua solicitação na lista para ver os detalhes da solicitação. Aqui você pode saber mais sobre as propriedades da solicitação, os resultados da pesquisa e o status da solicitação. Esta página se tornará seu hub para trabalhar e colaborar no gerenciamento dos arquivos encontrados, na criação de relatórios e exportações e na conclusão da solicitação.

Os blocos na página de detalhes da solicitação incluem:

- **Detalhes**: os detalhes essenciais sobre a solicitação, incluindo sua data limite e data de solicitação, sua descrição e a regulamentação de privacidade relacionada.
- **Progresso**: uma linha do tempo que indica as etapas concluídas e todas as tarefas ainda a serem concluídas.
- Estatísticas sobre o estágio de progresso atual. Esse bloco pode mostrar informações como um resumo de estimativa de dados, quantos itens foram encontrados em sua pesquisa e seus locais em Microsoft 365 ou o status de suas exportações.
- **Itens de prioridade a serem examinados**: este bloco mostrará informações sobre todos os itens importantes que Priva detectou para você. Por exemplo, isso pode incluir informações confidenciais que já contêm um rótulo de confidencialidade da Microsoft ou itens com dados sobre vários indivíduos que podem exigir redação. Isso ajudará os administradores a saber por onde começar a revisão. Os itens de prioridade podem ser encontrados em Dados coletados pela filtragem pela coluna "Tipos de Prioridade".

### <a name="understand-progress-stages"></a>Entender os estágios de progresso

As solicitações de direitos de entidade passam por vários estágios. Alguns estados progridem automaticamente e outros estágios avançam quando os administradores e colaboradores de solicitação de direitos de entidade concluem etapas essenciais, como revisar arquivos.

Como as solicitações podem precisar ser trabalhadas ao longo do tempo ou por vários colaboradores, Priva fornece atualizações contínuas sobre o status e diretrizes sobre as próximas etapas a serem executadas. Essas atualizações podem ser exibidas na guia **Visão geral** da página de detalhes de uma solicitação de direitos de assunto.

#### <a name="data-estimate"></a>Estimativa de dados
Depois de criar uma solicitação, Priva começará imediatamente a procurar possíveis correspondências com o titular dos dados em seu Microsoft 365 ambiente. Depois de identificarmos todos os itens que achamos que correspondem aos seus critérios, você verá a estimativa no cartão  de resumo de estimativa de dados na página Visão geral **da** solicitação. A quantidade de dados dentro do escopo de sua pesquisa afetará o tempo necessário para concluir a estimativa.

Sua solicitação será movida automaticamente para o próximo estágio da recuperação de dados, em que todos os itens de conteúdo são reunidos para que os stakeholders possam colaborar na revisão de dados. Em alguns casos, vamos pausar a estimativa de dados antes de passar para a recuperação e notificá-lo das próximas etapas a serem seguidas antes de continuar.

Você também pode optar por pausar automaticamente no estágio de estimativa de dados ao criar uma solicitação de direitos de entidade pela primeira vez. Durante o processo de criação, selecione **a opção Obter uma primeira** estimativa durante a **etapa De configurações de** pesquisa. Examine os detalhes sobre a [etapa de configurações de pesquisa](subject-rights-requests-create.md#define-search-settings).

#### <a name="pause-in-data-estimate-for-large-search-results"></a>Pausar na estimativa de dados para resultados de pesquisa grandes

Priva observará se sua estimativa de dados for projetar para retornar um grande número de itens a serem examinados (mais de 10 mil itens). A estimativa será pausada para que você possa visualizar os resultados e decidir se [](subject-rights-requests-create.md#refine-your-search) deseja editar a consulta de pesquisa para direcionar locais ou condições mais específicas ou continuar a recuperar os itens identificados.  Mostraremos na tela o número de itens e o volume de dados que correspondem à sua pesquisa. Você terá uma ou ambas as opções a seguir em uma barra de mensagens na parte superior da tela:

- Um **botão Editar consulta de** pesquisa levará você diretamente para as configurações de pesquisa da solicitação para definir parâmetros mais rígidos e gerar uma nova estimativa.
- Desde que a consulta de pesquisa não tenha mais de 300 mil itens, você também verá uma opção para **recuperar dados**. Isso permite que você opte por não editar sua pesquisa e continuar coletando os dados.

#### <a name="retrieve-data"></a>Recuperar dados
O estágio de recuperação de dados é quando todos os arquivos, emails, chats, imagens e outros itens de conteúdo que contêm os dados pessoais do titular dos dados são recuperados e colocados juntos em um contêiner de armazenamento de blobs do Azure para revisão. A recuperação de dados pode levar alguns minutos ou significativamente mais, dependendo do volume de dados. Quando esse estágio for concluído, a solicitação passará automaticamente para o próximo estágio dos **dados de revisão**.

#### <a name="review-data"></a>Examinar dados
 Neste estágio, seus colaboradores devem examinar as descobertas na guia  Dados coletados e executar todas as tarefas aplicáveis, como redação, aplicação de marcas e a adição de anotações. Quando terminar a revisão, selecione **Concluir revisão**.

#### <a name="generate-reports"></a>Gerar relatórios
Seus relatórios estão sendo gerados neste estágio. Quando concluídas, elas podem ser encontradas na **guia** Relatórios. Os arquivos concluídos podem ser exportados para revisão final e entrega para o titular dos dados que fez a solicitação.

#### <a name="close-the-request"></a>Fechar a solicitação
Uma solicitação fechada indica que todo o trabalho foi concluído para atender a essa solicitação de direitos de entidade. Todos os dados coletados e relatórios serão mantidos de acordo com suas [configurações de retenção de dados](priva-settings.md#data-retention-periods).

## <a name="step-2-optional-view-and-edit-search-queries"></a>Etapa 2 (opcional): exibir e editar consultas de pesquisa

Para ver informações detalhadas sobre a pesquisa de dados por trás de uma solicitação de direitos de assunto, selecione **Exibir detalhes da consulta de pesquisa**. Isso abre um painel resumindo a consulta e mostrando mais detalhes sobre o que foi encontrado.

Você tem a opção aqui para **visualizar os resultados da** pesquisa para ver qual tipo de conteúdo será retornado para essa consulta. Se você quiser alterar as propriedades dessa pesquisa e ainda não iniciou a fase Recuperar Dados, poderá usar a opção Editar consulta **de** pesquisa.

O processo guiado de consulta de pesquisa de edição permite alterar ou adicionar propriedades para identificação do titular dos dados, seus filtros e condições de pesquisa e os locais nos quais procurar dados (incluindo Exchange, SharePoint, OneDrive e/ou Teams). Use essas opções para alcançar o nível de especificidade desejado. Você pode examinar a versão final da nova consulta antes de pressionar **Salvar**.

Quando você terminar de editar a consulta de pesquisa, uma nova pesquisa será executada para substituir os resultados da pesquisa anterior. Isso redefine seu status na seção **Progresso** para a primeira etapa, Estimativa **de dados**. A nova pesquisa pode levar até 60 minutos para ser concluída. Quando terminar, você verá os resultados atualizados na página de detalhes da solicitação.

## <a name="step-3-review-data"></a>Etapa 3: Examinar dados

Neste estágio, seus colaboradores devem examinar as descobertas na **guia Dados coletados**. Um Teams canal será configurado automaticamente para facilitar a revisão de conteúdo por todos os stakeholders. Consulte [Colaborar na revisão de dados](#collaborate-on-data-review) para obter mais detalhes. As tarefas essenciais para a etapa de revisão de dados são descritas abaixo.

#### <a name="mark-items-as-include-or-exclude-and-add-notes"></a>Marcar itens como Incluir ou Excluir e adicionar anotações

Examine a lista de itens identificados retornados pela pesquisa. Se você decidir que o item deve ser incluído como parte do relatório final de volta ao assunto dos dados, selecione  Incluir na barra de comandos na parte superior da lista de itens. Você também pode selecionar o botão **azul** Incluir na área de revisão de conteúdo à direita da lista de itens. Quando você seleciona **Incluir**, um painel de submenu é exibido com uma opção para adicionar anotações. Quando terminar, selecione Enviar **para** salvar o status de revisão do item como **Incluir**.

Se o item não pertencer como parte da solicitação, selecione Excluir na  barra de comandos ou o botão Excluir  na área de revisão de conteúdo. Excluir um item significa que ele não será incluído nos relatórios [finais gerados para o titular dos dados](subject-rights-requests-reports.md).

> [!NOTE]
> Se você marcar um item como **Exclude**, será necessário adicionar uma anotação como justificativa para o motivo pelo qual ele não pertence à solicitação de direitos do assunto. As anotações são para fins internos e não estão incluídas nos relatórios finais.

Se o conteúdo parecer ser um falso positivo, selecione Não **uma** correspondência e, no painel de submenu, selecione **Confirmar**. Essa ação excluirá o arquivo dos relatórios finais e sinalizará o item como algo que não deveria ter sido detectado na pesquisa.

#### <a name="apply-tags"></a>Apply tags

As marcas podem ser usadas para ajudá-lo a identificar itens que precisam de mais atenção. Priva fornece três marcas padrão – **Acompanhamento**, **Exclusão** e **Atualização** – para as quais você pode definir uma descrição. Priva também fornece duas marcas personalizadas que você pode nomear e descrever.

Por exemplo, se você determinar durante a revisão de dados que um item de conteúdo não precisa ser mantido pela sua organização, poderá aplicar a marca  Excluir e exportar uma lista de todos os arquivos marcados para que você possa voltar e excluir os itens identificados quando terminar a solicitação.

As cinco marcas gerenciadas **em Configurações se** aplicam a todas as suas solicitações de direitos de entidade.

**Para adicionar ou remover marcas:**

- Selecione o item na lista na guia **Dados coletados** da solicitação.
- Na área de visualização do item à direita da lista, selecione o botão Aplicar **marcas** na linha inferior. Você também pode selecionar os três pontos à direita do nome do item e selecionar a **opção Aplicar marcas** .
- Um painel de submenu é exibido com a lista de marcas. Marque a caixa ao lado de qualquer uma das marcas que você deseja aplicar ao item. Desinstalar uma caixa marcada removerá a marca.
- Quando terminar, selecione **Salvar**, que salva suas seleções de marca e fecha o painel de submenu.

**Para adicionar marcas personalizadas ou atualizar descrições de marca:**
- Na página Solicitações de Direitos de Entidade, **selecione Configurações** no canto superior direito da tela para acessar as configurações de Priva.
- Vá para a **página Marcas de revisão de** dados e selecione a marca para inserir uma descrição e, para as marcas personalizadas, um nome. Saiba mais sobre as [configurações de marca](priva-settings.md#data-review-tags).

**Para exportar uma lista de itens marcados:**
- Vá para a **página Dados coletados** em uma solicitação de direitos de entidade.
- Acima da lista de itens, selecione o ícone de seta para baixo que diz **Exportar** quando você passar o mouse sobre ele.
- Um Excel será baixado, que mostra as propriedades de todos os itens coletados pela pesquisa para a solicitação. Localize **a coluna** Marcas para identificar e classificar os itens por marca.

#### <a name="use-the-annotate-command-to-redact-text"></a>Usar o comando Anotação para reatar o texto
O **comando Anotar na** área de revisão de conteúdo permite que você crie marcações embutidas e redacte dados em um item de conteúdo. Por exemplo, se você precisar incluir um arquivo para um indivíduo que também contém as informações pessoais de um assunto de dados diferente, poderá usar a **redação** área sob o botão Desenho na barra de comandos para excluir todas as informações que não pertencem à pessoa que fez a solicitação. Quando as edições forem concluídas, selecione **Incluir** para adicionar o arquivo editado à solicitação. A anotação cria uma cópia do arquivo, que é armazenada no blob do Azure. O arquivo original permanece inalterado e armazenado em seu local original.

#### <a name="enter-notes-about-a-file"></a>Inserir anotações sobre um arquivo
Para adicionar ou revisar anotações em um item, selecione o item em sua linha e vá para  a guia Anotações de Arquivo na área de revisão de conteúdo à direita. Você também pode usar a **opção Adicionar anotação de** arquivo para criar um novo comentário. Para revisar ou adicionar anotações em um nível geral de maiúsculas e minúsculas, vá para a guia **Anotações** principal acima e use **a observação Adicionar caso**. Essas anotações estarão visíveis para os usuários que trabalham na solicitação, mas não serão incluídas no relatório final ou compartilhadas de outra forma com o titular dos dados.

#### <a name="complete-the-review"></a>Concluir a revisão

Quando todos os itens tiverem sido revisados e você tiver definido seu status como **Incluir, Excluir** ou Não uma correspondência, é hora de fechar **a** etapa de revisão selecionando o botão Concluir revisão  no canto superior direito da solicitação. Um painel de submenu mostrará um resumo dos dados e adicionará anotações relacionadas. Essas anotações são para manter registros internos e não são compartilhadas com o titular dos dados.

Selecione **Concluir revisão** no painel de submenu para concluir a etapa de revisão. Resumos de suas decisões serão fornecidos posteriormente na **guia** Relatórios.

### <a name="collaborate-on-data-review"></a>Colaborar na revisão de dados

Priva dá suporte à colaboração Microsoft Teams para permitir que seu grupo trabalhe em conjunto em solicitações de direitos de assunto. Quando você cria uma nova solicitação, um Teams é criado automaticamente e associado à sua solicitação por padrão. Aqui você pode discutir a solicitação e compartilhar com segurança entradas e contribuições. Para ingressar na conversa, abra sua solicitação e use a **opção Chat com colaboradores** . Isso abrirá Microsoft Teams e o colocará no canal Geral para o site de equipe da solicitação de direitos de assunto.

Para examinar a lista de colaboradores ativos que podem exibir e contribuir com seu site de equipe, dentro de sua solicitação de direitos de assunto, abra a guia **Colaboradores** . Para adicionar usuários adicionais para colaborar nessa solicitação, selecione a opção **para Adicionar um colaborador**.

Para alterar o comportamento padrão de gerar sites Teams ao criar uma solicitação de direitos de assunto, vá para **Configurações** na navegação superior e selecione Teams colaboração para modificar **a** configuração.

Você também pode usar a  opção Compartilhar no canto superior direito de uma solicitação de assunto para conectar as pessoas por email ou Teams ou copiar o link para a página em Priva. O compartilhamento via Teams permite que você selecione um site e um canal existentes do Teams disponíveis para sua conta, onde ele postará um link para esse caso junto com qualquer mensagem que você fornecer.

## <a name="step-4-close-the-request"></a>Etapa 4: Fechar a solicitação

Quando você tiver executado todas as ações necessárias para resolver sua solicitação de direitos de assunto, selecione **Fechar a solicitação**. Isso cria o relatório final, que pode ser encontrado na **guia Relatórios**. A conclusão pode levar algum tempo, dependendo do número de arquivos na solicitação.

## <a name="next-steps"></a>Próximas etapas
Para saber mais sobre como trabalhar com relatórios e concluir solicitações de direitos de entidade, consulte [Gerar relatórios e atender a uma solicitação de direitos de assunto](subject-rights-requests-reports.md).

## <a name="legal-disclaimer"></a>Aviso de isenção de responsabilidade legal

[Aviso de isenção de responsabilidade legal da Microsoft Priva](priva-disclaimer.md)
