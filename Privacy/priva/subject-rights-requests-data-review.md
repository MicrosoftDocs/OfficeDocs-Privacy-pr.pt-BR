---
title: Revisar dados para uma solicitação de direitos de assunto
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
description: Saiba como revisar os dados de solicitação de direitos de assunto coletados pelo Microsoft Priva e colaborar na conclusão da solicitação.
ms.openlocfilehash: 5a72208894ff699675dcde230a7413b20c0b0a1e
ms.sourcegitcommit: a9ad5185174a9e8a7eea7583d257e8535c96a2ed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63746768"
---
# <a name="review-data-for-a-subject-rights-request"></a>Revisar dados para uma solicitação de direitos de assunto

Depois de criar uma solicitação de direitos de [assunto (saiba](subject-rights-requests-create.md) mais) no Microsoft Priva, a solução Solicitações de Direitos de Assunto usará suas entradas para procurar combinações sobre seu assunto de dados no ambiente de Microsoft 365 da sua organização. Depois que esses dados são compilados, você pode revisar as descobertas, fazer escolhas sobre o que incluir e rediscar informações conforme necessário. Essas etapas podem ser colaboradas por vários usuários por meio da interface Priva.

## <a name="step-1-review-request-details-and-monitor-progress"></a>Etapa 1: revisar detalhes da solicitação e monitorar o andamento

Para ver os resultados iniciais de sua pesquisa, vá para a área Priva do [Centro de conformidade do Microsoft 365 e abra](https://compliance.microsoft.com/) **Solicitações de direitos de assunto**. Uma lista de todas as solicitações de direitos de assunto abertas pode ser encontrada nesta página principal.

Selecione sua solicitação na lista para ver detalhes da solicitação. Aqui você pode saber mais sobre as propriedades da solicitação, os resultados da pesquisa e o status da solicitação. Esta página se tornará seu hub para trabalhar e colaborar no gerenciamento dos arquivos encontrados, na criação de relatórios e exportações e na conclusão da solicitação.

Os blocos na página de detalhes da solicitação incluem:

- **Detalhes**: os detalhes essenciais sobre a solicitação, incluindo seu prazo e data de solicitação, sua descrição e a regulamentação de privacidade relacionada.
- **Progresso**: uma linha do tempo indicando etapas concluídas e todas as tarefas ainda a serem concluídas.
- Estatísticas sobre o estágio de progresso atual. Esse item pode mostrar informações como um resumo de estimativa de dados, quantos itens foram encontrados em sua pesquisa e seus locais no Microsoft 365 ou o status de suas exportações.
- **Itens de prioridade a serem revisados**: este item mostrará informações sobre todos os itens importantes que Priva detectou para você. Por exemplo, isso pode incluir informações confidenciais que já têm um rótulo de confidencialidade da Microsoft ou itens com dados sobre vários indivíduos que podem exigir redação. Isso ajudará os administradores a saber por onde começar na revisão. Os itens de prioridade podem ser encontrados em Dados coletados pela filtragem pela coluna "Tipos de Prioridade".

### <a name="understand-progress-stages"></a>Compreender estágios de progresso

As solicitações de direitos de assunto passam por vários estágios. Alguns estados progridem automaticamente e outros estágios avançam quando os administradores de solicitação de direitos de assunto e colaboradores concluem etapas essenciais, como revisar arquivos.

Como as solicitações podem precisar ser trabalhadas ao longo do tempo ou por vários colaboradores, Priva fornece atualizações contínuas sobre o status e orientações sobre as próximas etapas a serem tomadas. Essas atualizações podem ser exibidas na guia **Visão** geral da página de detalhes de uma solicitação de direitos de assunto.

#### <a name="data-estimate"></a>Estimativa de dados
Depois de criar uma solicitação, Priva imediatamente começa a procurar possíveis combinações com o assunto de dados em seu Microsoft 365 ambiente. Depois de identificarmos todos os itens que acreditamos corresponder aos seus critérios, você verá a estimativa no cartão de  resumo de estimativa de dados na página Visão geral **da** solicitação. A quantidade de dados dentro do escopo da pesquisa afetará o tempo que levará para concluir a estimativa.

Sua solicitação será automaticamente para o próximo estágio de recuperação de dados, onde todos os itens de conteúdo são reunidos para que as partes interessadas possam colaborar na revisão de dados. Em algumas instâncias, vamos pausar a estimativa de dados antes de ir para recuperação e notificá-lo das próximas etapas a serem seguidas antes de continuar.

Você também pode optar por pausar automaticamente no estágio de estimativa de dados quando criar uma solicitação de direitos de assunto pela primeira vez. Durante o processo de criação, selecione **a opção Obter uma primeira** estimativa durante a **etapa De configurações de** Pesquisa. Revise detalhes sobre a [etapa de configurações de pesquisa](subject-rights-requests-create.md#define-search-settings).

#### <a name="pause-in-data-estimate-for-large-search-results"></a>Pausar na estimativa de dados para grandes resultados de pesquisa

Priva notará se sua estimativa de dados for projetada para retornar um grande número de itens a serem revisados (mais de 10 mil itens). A estimativa pausa para que você possa visualizar os resultados e decidir se editará [](subject-rights-requests-create.md#refine-your-search) a consulta de pesquisa para direcionar locais ou condições mais específicas ou continuar a recuperar os itens identificados.  Mostraremos na tela o número de itens e o volume de dados que corresponderão à sua pesquisa. Você terá uma ou ambas as opções a seguir em uma barra de mensagens na parte superior da tela:

- Um **botão Editar consulta de** pesquisa o levará diretamente às configurações de pesquisa da solicitação para definir parâmetros mais estritos e gerar uma nova estimativa.
- Desde que sua consulta de pesquisa não seja mais de 300 mil itens, você também verá uma opção para **Recuperar dados**. Isso permite que você escolha não editar sua pesquisa e continuar coletando os dados.

#### <a name="retrieve-data"></a>Recuperar dados
O estágio de recuperação de dados é quando todos os arquivos, emails, chats, imagens e outros itens de conteúdo que contêm os dados pessoais do sujeito de dados são recuperados e colocados juntos em um contêiner de armazenamento de blob do Azure para revisão. A recuperação de dados pode demorar alguns minutos ou significativamente mais, dependendo do volume de dados. Quando esse estágio for concluído, a solicitação será automaticamente deslocada para o próximo estágio dos **dados de Revisão**.

#### <a name="review-data"></a>Revisar dados
 Neste estágio, seus colaboradores devem revisar as descobertas na guia  Dados coletados e executar todas as tarefas aplicáveis, como redação, aplicação de marcas e a adição de anotações. Quando terminar a revisão, selecione **Concluir revisão**.

#### <a name="generate-reports"></a>Gerar relatórios
Seus relatórios estão sendo gerados neste estágio. Quando concluídas, elas podem ser encontradas na **guia Relatórios** . Seus arquivos concluídos podem ser exportados para revisão final e entrega para o assunto de dados que fez a solicitação.

#### <a name="close-the-request"></a>Fechar a solicitação
Uma solicitação fechada indica que todo o trabalho foi concluído para atender a essa solicitação de direitos de assunto. Todos os dados coletados e relatórios serão mantidos de acordo com suas [configurações de retenção de dados](priva-settings.md#data-retention-periods).

## <a name="step-2-optional-view-and-edit-search-queries"></a>Etapa 2 (opcional): Exibir e editar consultas de pesquisa

Para ver informações detalhadas sobre a pesquisa de dados por trás de uma solicitação de direitos de assunto, selecione **Exibir detalhes da consulta de pesquisa**. Isso abre um painel resumindo a consulta e mostrando mais detalhes sobre o que foi encontrado.

Você tem a opção aqui para **Visualizar resultados de** pesquisa para ver qual tipo de conteúdo será retornado para essa consulta. Se você quiser alterar as propriedades dessa pesquisa e ainda não iniciou a fase Recuperar Dados, pode usar a opção **Editar consulta de** pesquisa.

O processo de consulta de pesquisa de edição permite alterar ou adicionar propriedades para a identificação do assunto de dados, seus filtros e condições de pesquisa e os locais nos quais procurar dados (incluindo Exchange, SharePoint, OneDrive e/ou Teams). Use essas opções para alcançar o nível de especificidade desejado. Você pode revisar a versão final da nova consulta antes de atingir **Salvar**.

Quando você terminar de editar a consulta de pesquisa, uma nova pesquisa será executado para substituir os resultados da pesquisa anterior. Isso redefine seu status na seção **Progresso** para a primeira etapa, **Estimativa de dados**. A nova pesquisa pode levar até 60 minutos para ser concluída. Depois de terminar, você verá os resultados atualizados na página de detalhes da solicitação.

## <a name="step-3-review-data"></a>Etapa 3: Revisar dados

Neste estágio, seus colaboradores devem revisar as descobertas na **guia Dados coletados**. Um Teams canal será automaticamente definido para facilitar a revisão de conteúdo por todas as partes interessadas. Confira [Colaborar na revisão de dados](#collaborate-on-data-review) para obter mais detalhes. As tarefas essenciais para a etapa de revisão de dados são descritas abaixo.

#### <a name="mark-items-as-include-or-exclude-and-add-notes"></a>Marcar itens como Incluir ou Excluir e adicionar anotações

Revise a lista de itens identificados para determinar se os dados pessoais do assunto de dados estão em cada item. Se o item contiver as informações do assunto de dados e pertencer como parte do relatório final de volta ao assunto de dados, marque o  item como Incluir  selecionando Incluir na barra de comandos na parte superior da lista de itens. Você também pode selecionar o botão **incluir** azul na área de revisão de conteúdo à direita da lista de itens. Quando você seleciona **Incluir**, um painel de sobrevoo aparece com uma opção para adicionar anotações. Quando terminar, selecione **Enviar** para salvar o status de revisão do item como **Include**.

Se você não precisar incluir um item como parte da solicitação, selecione **Excluir** na barra de comandos ou no botão **Excluir** na área de revisão de conteúdo. Excluir um item significa que não é relevante para a solicitação de direitos de assunto e o item não será incluído nos relatórios finais gerados para o [assunto de dados](subject-rights-requests-reports.md).

> [!NOTE]
> Se você marcar um item **Exclude**, será necessário adicionar uma nota como justificativa para o motivo pelo qual ele não pertence à solicitação de direitos de assunto. As anotações são para fins internos e não estão incluídas nos relatórios finais.

Se o conteúdo parece ser um falso positivo, selecione Não  uma combinação para excluir o arquivo de seus relatórios finais e sinalizar o item como algo que não deveria ter sido detectado na pesquisa. No painel **Marcar como não uma combinação de** flyout, selecione **Confirmar** para nos dizer que o item não combina com seus critérios de pesquisa.

#### <a name="apply-tags"></a>Apply tags

As marcas podem ser usadas para ajudá-lo a identificar itens que precisam de mais atenção. Priva fornece três marcas padrão - **Acompanhamento**, **Exclusão** e **Atualização** - para as quais você pode definir uma descrição. Priva também fornece duas marcas personalizadas que você pode nomear e descrever.

Por exemplo, se você determinar durante a revisão de dados que um item de conteúdo não precisa ser mantido pela sua organização, você pode aplicar a marca **Excluir** e exportar uma lista de todos os arquivos marcados para que você possa voltar e excluir os itens identificados quando terminar com a solicitação.

As cinco marcas que você definir e gerenciar em [Configurações se aplicam](priva-settings.md#data-review-tags) a todas as suas solicitações de direitos de assunto.

**Para adicionar ou remover marcas:**

- Selecione o item na lista na guia **Dados coletados** da solicitação.
- Na área de visualização do item à direita da lista, selecione o botão **Aplicar marcas** na linha inferior. Você também pode selecionar os três pontos à direita do nome do item e selecionar a **opção Aplicar marcas** .
- Um painel de sobrevoo aparece com a lista de marcas. Marque a caixa ao lado de qualquer uma das marcas que você deseja aplicar ao item. Desinchando uma caixa de verificação removerá a marca.
- Quando você estiver satisfeito com suas seleções, selecione **Salvar**, que salva suas seleções de marca e fecha o painel de flyout.

**Para adicionar marcas personalizadas ou atualizar descrições de marca:**
- Na página Solicitações de Direitos de Assunto, selecione **Configurações** no canto superior direito da tela para chegar às configurações priva.
- Vá para a **página Marcas de revisão de** dados e selecione a marca para inserir uma descrição e, para as marcas personalizadas, um nome. Saiba mais sobre [as configurações de marca](priva-settings.md#data-review-tags).

**Para exportar uma lista de itens marcados:**
- Vá para a **página Dados coletados** em uma solicitação de direitos de assunto.
- Acima da lista de itens, selecione o ícone de seta para baixo que diz **Exportar** quando você passar o mouse sobre ele.
- Um Excel será baixado. Abra o arquivo quando terminar de baixar.

O arquivo Excel baixado mostra as propriedades de todos os itens coletados pela pesquisa para a solicitação. Encontre a **coluna Marcas** para identificar e classificar os itens por marca.

#### <a name="use-the-annotate-command-to-redact-text"></a>Use o comando Anotação para rediscar o texto
Use **Annotate** para criar marcações em linha ou redactar dados em um arquivo selecionado. Por exemplo, se você precisar incluir um arquivo para um indivíduo que também contém as informações pessoais de outras pessoas, você pode usar a **redação** área (no botão Desenho na barra de comandos) para excluir todas as informações que não pertencem à pessoa que fez a solicitação. Quando suas edições são concluídas, selecione **Incluir** para adicionar o arquivo redacted à solicitação. A anotação cria uma cópia do arquivo, para que nada no arquivo original seja alterado e permaneça em seu local original. A cópia é armazenada no blob do Azure.

#### <a name="enter-notes-about-a-file"></a>Inserir anotações sobre um arquivo
Para adicionar ou revisar anotações em um item, selecione o item de sua linha e vá para  a guia Anotações de Arquivo na área de revisão de conteúdo à direita. Você também pode usar a **opção Adicionar nota de arquivo** para criar um novo comentário. Para revisar ou adicionar anotações em um nível geral de caso, vá para a guia **Principal Notas** acima e use **a observação Adicionar caso**. Essas anotações estarão visíveis para os usuários que trabalham na solicitação, mas não serão incluídas no relatório final ou compartilhadas com o assunto dos dados.

#### <a name="complete-the-review"></a>Concluir a revisão

Quando todos os itens foram revisados e você definiu seu status como **Include**, **Exclude** ou **Not a match,** é hora de fechar a etapa de revisão selecionando o botão Concluir revisão no  canto superior direito da solicitação. Um painel de sobrevoo mostrará um resumo dos dados e adicionará quaisquer anotações relacionadas. Essas anotações são para a manutenção de registros internos e não são compartilhadas com o assunto dos dados.

Selecione **Concluir revisão** no painel de sobrevoos para concluir a etapa de revisão. Os resumos de suas decisões serão fornecidos posteriormente na **guia Relatórios** .

### <a name="collaborate-on-data-review"></a>Colaborar na revisão de dados

Priva dá suporte à colaboração Microsoft Teams para permitir que seu grupo trabalhe em conjunto em solicitações de direitos de assunto. Quando você cria uma nova solicitação, um canal Teams é criado automaticamente e associado à sua solicitação por padrão. Aqui você pode discutir a solicitação e compartilhar com segurança as entradas e as contribuições. Para participar da conversa, abra sua solicitação e use a **opção Chat com colaboradores** . Isso abrirá Microsoft Teams e o colocará no canal Geral para o site de Equipe da sua solicitação de direitos de assunto.

Para revisar a lista de colaboradores ativos que podem exibir e contribuir com seu site de Equipe, dentro da solicitação de direitos de assunto, abra a guia **Colaboradores** . Para adicionar usuários adicionais para colaborar nessa solicitação, selecione a opção **Adicionar um colaborador**.

Para alterar o comportamento padrão de gerar Teams sites ao criar uma solicitação de direitos de assunto, acesse Configurações  na nav superior e selecione Teams colaboração para modificar **a** configuração.

Você também pode usar a opção **Compartilhar** na parte superior direita dentro de uma solicitação de assunto correta para fazer loop nas pessoas por meio de Teams ou email, ou para copiar o link para a página em Priva. O compartilhamento Teams permite selecionar um site e canal de Teams existentes disponíveis para sua conta, onde ele postará um link para esse caso juntamente com qualquer mensagem que você fornecer.

## <a name="step-4-close-the-request"></a>Etapa 4: Fechar a solicitação

Quando você tiver executado todas as ações necessárias para resolver sua solicitação de direitos de assunto, selecione **Fechar a solicitação**. Isso cria o relatório final, que pode ser encontrado na **guia Relatórios**. A conclusão pode demorar um pouco, dependendo do número de arquivos na solicitação.

## <a name="next-steps"></a>Próximas etapas
Para saber mais sobre como trabalhar com relatórios e concluir solicitações de direitos de assunto, consulte [Gerar relatórios e atender a uma solicitação de direitos de assunto](subject-rights-requests-reports.md).

## <a name="legal-disclaimer"></a>Aviso de isenção de responsabilidade legal

[Aviso de isenção de responsabilidade legal da Microsoft Priva](priva-disclaimer.md)
