---
title: Revisar dados e colaborar em solicitações de direitos de assunto no gerenciamento de privacidade
f1.keywords:
- CSH
ms.author: v-jgriffee
author: jmgriffee
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- M365-security-compliance
- M365-privacy-management
search.appverid:
- MOE150
- MET150
description: Saiba como revisar os dados de solicitação de direitos de assunto coletados pelo gerenciamento de privacidade e colaborar na conclusão da solicitação.
ms.openlocfilehash: 7f0754007c70ef7836abf13ec0dbd50e9d9c8958
ms.sourcegitcommit: 85e085eb17af8b4efd1f45207445e1b3c3679600
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/19/2021
ms.locfileid: "60478078"
---
# <a name="review-data-and-collaborate-on-subject-rights-requests"></a>Revisar dados e colaborar em solicitações de direitos de assunto

Depois de criar uma solicitação de direitos de assunto[(](privacy-management-subject-rights-requests-create.md)saiba mais ), o gerenciamento de privacidade usará suas entradas sobre seu assunto para procurar por combinações no ambiente de Microsoft 365 da sua organização. Depois que esses dados são compilados, você pode revisar as descobertas, fazer escolhas sobre o que incluir e rediscar informações conforme necessário. Essas etapas podem ser colaboradas por vários usuários por meio da interface de gerenciamento de privacidade.

## <a name="step-1-review-request-details-and-monitor-progress"></a>Etapa 1: revisar detalhes da solicitação e monitorar o andamento

Para ver os resultados iniciais de sua pesquisa, vá para a área de gerenciamento de privacidade do Centro de conformidade do Microsoft 365 [e](https://compliance.microsoft.com/) abra **Solicitações de direitos de assunto.** Uma lista de todas as solicitações de direitos de assunto abertas pode ser encontrada nesta página principal.

Selecione sua solicitação na lista para ver detalhes da solicitação. Aqui você pode saber mais sobre as propriedades da solicitação, os resultados da pesquisa e o status da solicitação. Esta página se tornará seu hub para trabalhar e colaborar no gerenciamento dos arquivos encontrados, na criação de relatórios e exportações e na conclusão da solicitação.

Os blocos na página de detalhes da solicitação incluem:

- **Detalhes**: Os detalhes essenciais sobre a solicitação, incluindo seu prazo e data de solicitação, sua descrição e a regulamentação de privacidade relacionada.
- **Progresso**: uma linha do tempo indicando etapas concluídas e todas as tarefas ainda a serem concluídas.
- Estatísticas sobre o estágio de progresso atual. Esse item pode mostrar informações como um resumo de estimativa de dados, quantos itens foram encontrados em sua pesquisa e seus locais no Microsoft 365 ou o status de suas exportações.
- **Itens de prioridade a revisar**: Este item mostrará informações sobre todos os itens importantes que o gerenciamento de privacidade detectou para você. Por exemplo, isso pode incluir informações confidenciais que já têm um rótulo de confidencialidade da Microsoft ou itens com dados sobre vários indivíduos que podem exigir redação. Isso ajudará os administradores a saber por onde começar na revisão. Os itens de prioridade podem ser encontrados em Dados coletados pela filtragem pela coluna "Tipos de Prioridade".

### <a name="understand-progress-stages"></a>Compreender estágios de progresso

As solicitações de direitos de assunto passam por vários estágios. Alguns progridem automaticamente à medida que o gerenciamento de privacidade faz sua avaliação de dados e outros avançam quando os administradores e colaboradores de direitos de assunto solicitam que os administradores e colaboradores concluam etapas essenciais, como revisão, seleção e redactação de arquivos.

Como as solicitações podem precisar ser trabalhadas ao longo do tempo ou por vários colaboradores, o gerenciamento de privacidade fornece atualizações contínuas sobre o status e orientações sobre as próximas etapas a serem tomadas. Essas atualizações podem ser exibidas na página de visão geral da solicitação de direitos de assunto.

1. **Estimativa de** dados : após a criação de uma solicitação, o gerenciamento de privacidade identifica itens que incluem possíveis combinações com seu assunto de dados e faz anotações de seus locais no Microsoft 365. Quando a estimativa de dados for feita, você avançará automaticamente para recuperar dados **,** a menos que haja erros ou sua solicitação esteja definida para pausar aqui para revisão do administrador.
   - Sua solicitação pode ser definida para exigir revisão de administrador neste estágio. Se o administrador determinar que os resultados iniciais da consulta de pesquisa parecem satisfatórios, você pode continuar a recuperar dados. Se quiser fazer alterações antes de prosseguir, você pode optar por editar sua consulta de pesquisa primeiro. Consulte a Etapa 2 para obter detalhes. Você não poderá editar sua consulta de pesquisa depois de iniciar o estágio de recuperação de dados.
   - Se a consulta de pesquisa retornar uma grande estimativa de dados, o que significa que ela está acima do limite recomendado do gerenciamento de privacidade para tamanho ou contagem de arquivos, você pode tentar revisar sua pesquisa para refinar seu escopo. Observe que os arquivos associados a um item correspondente (por exemplo, anexos de arquivo em um email) podem contar para o total. As estimativas de dados que excedam o máximo de estimativa de dados grandes exigirão que uma revisão de pesquisa prossiga.
1. **Recuperar dados**: Este estágio indica que o gerenciamento de privacidade está em processo de recuperação de seus dados. Depois de concluído, ele avançará automaticamente para **revisar dados.**
1. **Dados de** revisão : Neste estágio, seus colaboradores devem revisar as descobertas na guia Dados coletados e executar todas as tarefas aplicáveis, como redação, aplicação de marcas e a adição de anotações.  Quando terminar a revisão, selecione **Concluir revisão**.
1. **Gerar relatórios**: seus relatórios estão sendo gerados neste estágio. Quando concluídas, elas podem ser encontradas na **guia Relatórios.** Seus arquivos concluídos podem ser exportados para revisão final e entrega para o assunto de dados que fez a solicitação.

## <a name="step-2-optional-view-and-edit-search-queries"></a>Etapa 2 (opcional): Exibir e editar consultas de pesquisa

Para ver informações detalhadas sobre a pesquisa de dados por trás de uma solicitação de direitos de **assunto,** selecione Exibir detalhes da consulta de pesquisa . Isso abre um painel resumindo a consulta e mostrando mais detalhes sobre o que foi encontrado.

Você tem a opção aqui para **Visualizar resultados de** pesquisa para ver qual tipo de conteúdo será retornado para essa consulta. Se você quiser alterar as propriedades dessa pesquisa e ainda não iniciou a fase Recuperar Dados, pode usar a opção Editar consulta **de** pesquisa.

O assistente de consulta de pesquisa de edição oferece a capacidade de alterar ou adicionar propriedades para a identificação do assunto de dados, seus filtros e condições de pesquisa e os locais nos quais procurar dados (incluindo Exchange, SharePoint, OneDrive e/ou Teams). Use essas opções para alcançar o nível de especificidade desejado. Você pode revisar a versão final da nova consulta antes de atingir **Salvar**.

Quando você terminar de editar a consulta de pesquisa, uma nova pesquisa será executado para substituir os resultados da pesquisa anterior. Isso redefine seu status na seção **Progresso** para a primeira etapa, **Estimativa de dados**. A nova pesquisa pode levar até 60 minutos para ser concluída. Depois de terminar, você verá os resultados atualizados na página de detalhes da solicitação.

## <a name="step-3-review-data"></a>Etapa 3: Revisar dados

Neste estágio, seus colaboradores devem revisar as descobertas na **guia Dados coletados.** Tarefas essenciais incluem:

1. Revise a lista de itens identificados e escolha se deve incluir cada arquivo em seus resumos e/ou exportações. Se você não precisar incluir uma combinação relatada, selecione a opção "Excluir". Se o conteúdo parece ser um falso positivo, você pode escolher "Não uma combinação" para excluir o arquivo de seus relatórios finais e sinalizar o item como algo que não deve ter sido escolhido pela solicitação. Para definir o status de um item, use o menu de ação (releitos verticais) ao lado de seu nome e selecione a escolha desejada. Se solicitado, adicione uma nota para referência interna para explicar sua decisão. As anotações são necessárias ao excluir arquivos.
1. Use a **opção Aplicar marcas** para ajudá-lo a identificar itens que precisam de atenção. As marcas disponíveis incluem opções fornecidas pelo sistema, por exemplo, marcando um item para acompanhamento e podem incluir marcas personalizadas, conforme definido em configurações globais.
1. Use **Annotate** para criar marcações em linha ou redactar dados em um arquivo selecionado. Por exemplo, se você precisar incluir um arquivo para um indivíduo que também contém as informações pessoais de outras pessoas, você pode usar a **redação** área (no botão Desenho na barra de comandos) para excluir todas as informações que não pertencem à pessoa que fez a solicitação. Quando suas edições são concluídas, selecione **Incluir** para adicionar o arquivo redacted à solicitação. A anotação cria uma cópia do arquivo, para que nada no arquivo original seja alterado e permaneça em seu local original. A cópia é armazenada no blob do Azure.
1. Para revisar anotações em um item, selecione-o e vá para a guia **Anotações de** Arquivo. Você também pode usar a **opção Adicionar nota de arquivo** para criar um novo comentário. Para revisar ou adicionar anotações em um nível geral de caso, vá para a guia **Principal notas** acima e use Add **case note**. Essas anotações estarão visíveis para os usuários que trabalham na solicitação, mas não serão incluídas no relatório final ou compartilhadas de outra forma com o assunto dos dados.
1. Quando todos os itens foram revisados e seus status definidos, selecione **Concluir revisão**. Isso abrirá um painel de sobrevoo onde você pode revisar um resumo dos dados e adicionar quaisquer anotações relevantes. Essas anotações são para a manutenção de registros internos e não são compartilhadas com o assunto dos dados.
1. Selecione Concluir revisão novamente para continuar. Os resumos de suas decisões serão fornecidos posteriormente na **guia Relatórios.**

### <a name="collaborate-on-data-review"></a>Colaborar na revisão de dados

O gerenciamento de privacidade dá suporte à colaboração Microsoft Teams para permitir que seu grupo trabalhe em conjunto em solicitações de direitos de assunto. Quando você cria uma nova solicitação, um canal Teams é criado automaticamente e associado à sua solicitação por padrão. Aqui você pode discutir a solicitação e compartilhar com segurança as entradas e as contribuições. Para participar da conversa, abra sua solicitação e use a **opção Chat com colaboradores.** Isso abrirá Microsoft Teams e o colocará no canal Geral para o site de Equipe da sua solicitação de direitos de assunto.

Para revisar a lista de colaboradores ativos que podem exibir e contribuir com seu site de Equipe, dentro da solicitação de direitos de assunto, abra a guia **Colaboradores.** Para adicionar usuários adicionais para colaborar nessa solicitação, selecione a opção **Adicionar um colaborador**.

Para alterar o comportamento padrão de Teams sites ao criar uma  solicitação de direitos de assunto, vá para Configurações na nav superior e selecione Teams colaboração para modificar **a** configuração.

Você também pode usar a opção **Compartilhar** na parte superior direita dentro de uma solicitação de assunto correta para fazer loop nas pessoas por meio de Teams ou email, ou para copiar o link para a página no gerenciamento de privacidade. O compartilhamento Teams permite selecionar um site e canal Teams existentes disponíveis para sua conta, onde ele postará um link para esse caso juntamente com qualquer mensagem que você fornecer.

## <a name="step-4-close-the-request"></a>Etapa 4: Fechar a solicitação

Quando você tiver executado todas as ações necessárias para resolver sua solicitação de direitos de assunto, selecione **Fechar a solicitação**. Isso cria o relatório final, que será criptografado e disponibilizado na guia **Relatórios.** A conclusão pode demorar um pouco, dependendo do número de arquivos na solicitação.

## <a name="next-steps"></a>Próximas etapas
Para saber mais sobre como trabalhar com relatórios e concluir solicitações de direitos de assunto, consulte [Atender solicitações de direitos de assunto](privacy-management-subject-rights-requests-fulfill.md).

## <a name="legal-disclaimer"></a>Aviso de isenção de responsabilidade legal

[Aviso de isenção de responsabilidade legal de gerenciamento de privacidade](privacy-management-disclaimer.md)
