---
title: Fluxo de trabalho para solicitações de direitos de entidade
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
description: Entenda as etapas do fluxo de trabalho e a página de detalhes da solicitação Solicitações de direitos do titular Microsoft Priva.
ms.openlocfilehash: 794176260f6377862d34a66dc71cef1e811188b9
ms.sourcegitcommit: fe651dab4c89e67b21d37531c04e3996b7af1138
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/14/2022
ms.locfileid: "66060077"
---
# <a name="understand-the-workflow-and-request-details-pages"></a>Entender o fluxo de trabalho e as páginas de detalhes da solicitação

**Neste artigo**: saiba mais sobre as etapas de progresso conforme você cria e trabalha por meio de uma solicitação. Entenda como trabalhar com os insights e recursos na página de detalhes de cada solicitação.

Quando você [cria uma solicitação](subject-rights-requests-create.md) na solução Solicitações de Direitos de Entidade, as informações fornecidas são usadas para procurar correspondentes sobre o assunto dos dados no ambiente de Microsoft 365 da sua organização. Os itens correspondentes são cumpridos para que você examine, faça escolhas sobre o que incluir e redacte as informações conforme necessário. Vários usuários podem colaborar nessas etapas na interface Solicitações de Direitos de Entidade. A [página](#overview-tab) Visão geral da solicitação fornece status sobre os estágios de progresso e diretrizes sobre as próximas etapas a serem executadas.

## <a name="progress-stages-for-requests"></a>Estágios de progresso para solicitações

Cada solicitação passa por vários estágios. Alguns estágios progridem automaticamente e outros estágios são avançados manualmente após a conclusão de determinadas etapas, como revisar arquivos.

- **Estimativa de** dados: antes de recuperar os dados, Priva estima a quantidade de dados que espera encontrar. Dependendo da quantidade de dados, a solicitação pode ou não ser movida automaticamente para o próximo estágio da recuperação de dados. Você pode definir uma solicitação para pausar no estágio de estimativa antes de coletar dados; saiba mais em [estimativa e recuperação de dados](subject-rights-requests-data-retrieval.md).

- **Recuperar dados**: todos os arquivos, emails, chats, imagens e outros itens de conteúdo são juntos. Quando esse estágio for concluído, a solicitação passará automaticamente para o próximo estágio de revisão de dados. Saiba mais em [estimativa e recuperação de dados](subject-rights-requests-data-retrieval.md).

- **Examinar dados**: os colaboradores revisam todos os dados coletados, decidem quais pertencem à solicitação e executam tarefas como a reação de arquivos e a adição de anotações de caso. Saiba mais sobre [como revisar dados para uma solicitação de direitos de entidade](subject-rights-requests-data-review.md). Depois de concluir a revisão de dados, você avança manualmente para o próximo estágio para gerar relatórios.

- **Gerar relatórios**: quando a revisão de dados é feita, um usuário avança manualmente para esta etapa. Priva gera os relatórios finais, que incluem o pacote de dados para compartilhar com o titular dos dados e relatórios internos para os registros da sua organização. Saiba mais sobre [como gerar relatórios](subject-rights-requests-reports.md).

- **Feche a solicitação**: quando todo o trabalho for concluído, feche a solicitação para indicar que ela foi considerada concluída. Saiba mais sobre [como gerar relatórios para](subject-rights-requests-reports.md) que você possa atender e fechar a solicitação.

## <a name="understanding-the-request-details-page"></a>Noções básicas sobre a página de detalhes da solicitação

Selecione **Solicitações de direitos do titular Priva** navegação à esquerda do portal de conformidade do Microsoft Purview para acessar as solicitações criadas pela sua organização e exibir seu status. Os cartões de status na página principal Solicitações de Direitos de Entidade, exibida abaixo, mostram o número de solicitações ativas, fechadas e vencidas e os principais tipos de solicitação. A tabela abaixo dos cartões de status lista todas as solicitações criadas pela sua organização, com a solicitação criada mais recentemente na parte superior.

**Página principal solicitações de direitos de entidade:** 
![ Página principal solicitações de direitos de entidade.](../media/priva-srr-overview.png)

Para abrir a página de detalhes de uma solicitação, selecione o nome da solicitação na tabela. Aqui você pode saber mais sobre as propriedades da solicitação, os resultados da pesquisa e o status da solicitação. A página de detalhes, exibida abaixo, se tornará seu hub para trabalhar e colaborar no gerenciamento dos arquivos encontrados, na criação de relatórios e exportações e na conclusão da solicitação.

**Uma página de detalhes da solicitação:**
![ Página de detalhes da solicitação de direitos de entidade.](../media/priva-srr-detailspage.png)

### <a name="overview-tab"></a>Guia Visão geral

A **guia** Visão geral da página de detalhes da solicitação fornece detalhes sobre a solicitação, um indicador de progresso mostrando sua etapa atual e informações importantes sobre os dados encontrados. Esta página tem cartões de status individuais explicados abaixo.

##### <a name="details"></a>Detalhes

O **cartão** Detalhes exibe informações básicas para orientá-lo para a solicitação, como sua data limite, a data de criação, a descrição e a regulamentação de privacidade relacionada.

##### <a name="progress"></a>Progress

O **cartão** de progresso lista cada etapa no processo: estimativa de dados, recuperar dados, examinar dados, gerar relatórios e fechar a solicitação. Um círculo azul preenchido ao lado da etapa indica a etapa em que você está atualmente. Uma marca de seleção dentro do círculo azul significa que a etapa está concluída. Um círculo vazio em branco significa que a etapa ainda não foi iniciada.

##### <a name="data-estimate-summary"></a>Resumo da estimativa de dados

O **cartão de resumo de estimativa** de dados é exibido quando a solicitação é pausada no estágio [de estimativa de dados](subject-rights-requests-data-retrieval.md#data-estimate). Ele mostra o local e o número de itens que sua pesquisa deve recuperar.

##### <a name="total-number-of-items-found"></a>Número total de itens encontrados

O **número total de itens encontrados** no cartão exibe o número de itens de conteúdo encontrados e seus locais Microsoft 365.

##### <a name="priority-items-to-review"></a>Itens de prioridade a serem examinados

Os **itens de prioridade a serem examinados** mostram itens que talvez você queira priorizar ao iniciar a revisão. O bloco exibe uma contagem de itens que pertencem às seguintes categorias:
- **Confidencial**: esses itens têm um [rótulo de confidencialidade da Microsoft](/microsoft-365/compliance/sensitivity-labels) aplicado a eles. Por exemplo, um documento do Word com um rótulo "Altamente Confidencial". 
- **Dados de várias pessoas**: esses itens contêm os dados pessoais de mais de uma pessoa. Se você quiser incluir esses itens como parte do pacote de dados final, precisará reexamar os dados irrelevantes nos arquivos. Obtenha [detalhes sobre a revisão de dados](subject-rights-requests-data-review.md). Para que o Priva identifique itens com dados de várias pessoas, sua organização precisa configurar a correspondência de dados para solicitações [de direitos de entidade](subject-rights-requests-data-match.md).

**Como localizar seus itens de prioridade:**

Primeiro, verifique se você habilitou sua exibição deles em sua  tabela de itens de dados coletados seguindo as etapas abaixo:

- Na guia **Dados coletados** , selecione **Personalizar colunas** na parte superior da lista de itens.
- No painel **Editar colunas** do submenu, coloque uma verificação ao lado de **Tipos de prioridade**.
- Selecione **Aplicar**. Sua lista de itens agora terá uma coluna **Tipos de** prioridade.

Agora você pode identificar os itens de prioridade e encontrá-los classificando a coluna **tipo** Prioridade para agrupar tipos semelhantes.

### <a name="data-collected-tab"></a>Guia Dados coletados

Quando todos os itens que correspondem às configurações de pesquisa forem identificados, eles serão coletados e apresentados na **guia Dados coletados** . Ao lado da lista de itens, há uma tela de visualização para revisar cada item, fazer redação e marcar itens como incluídos ou excluídos como parte da solicitação. Leia mais detalhes sobre a etapa [de colaboração e revisão de dados](subject-rights-requests-data-review.md).

### <a name="notes-tab"></a>Guia Anotações

A **guia** Anotações permite que os colaboradores insiram anotações sobre o trabalho feito na solicitação. Essas anotações são visíveis para todos que trabalham na solicitação, mas não serão incluídas no relatório final ou compartilhadas de outra forma com o titular dos dados.

### <a name="collaborators-tab"></a>Guia Colaboradores

A guia Colaboradores exibe todos os usuários que foram convidados a colaborar nos dados coletados e qualquer canal Teams associado para a solicitação. O criador da solicitação é listado automaticamente como um colaborador. Convide novos colaboradores selecionando o **comando Adicionar colaborador** e inserindo o nome de um usuário para selecioná-los em uma lista. Saiba mais detalhes sobre a [colaboração para revisão de dados](subject-rights-requests-data-review.md#collaboration-for-data-review)

### <a name="reports-tab"></a>Guia Relatórios

A **guia** Relatórios exibe todos os relatórios gerados automaticamente quando você avança para o estágio **Gerar** relatórios. Os relatórios são separados em duas categorias: relatórios para você compartilhar com o titular dos dados e relatórios destinados ao uso interno da sua organização. Obtenha detalhes sobre [como trabalhar com relatórios](subject-rights-requests-reports.md).

### <a name="history-tab"></a>Guia Histórico

A **guia Histórico** resume eventos de nível superior para a solicitação, incluindo alterações de estágio de progresso e agregações para o número de itens incluídos, excluídos e redigidos.

## <a name="next-steps"></a>Próximas etapas

Visite [Criar uma solicitação de direitos de assunto](subject-rights-requests-create.md) para saber como se declarar com sua primeira solicitação.

## <a name="legal-disclaimer"></a>Aviso de isenção de responsabilidade legal

[Microsoft Priva aviso de isenção de responsabilidade legal](priva-disclaimer.md)