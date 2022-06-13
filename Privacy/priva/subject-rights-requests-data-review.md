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
description: Saiba como examinar os dados de solicitação de direitos de entidade coletados Microsoft Priva e colaborar na conclusão da solicitação.
ms.openlocfilehash: 0182be22efe224481625c121dc98ebe1d96a06ec
ms.sourcegitcommit: 3c83e8133a5a71f4e1d76a0b2981ab3ec9cd6602
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/13/2022
ms.locfileid: "66046625"
---
# <a name="review-data-for-a-subject-rights-request"></a>Examinar dados de uma solicitação de direitos de entidade

**Neste artigo**: saiba como examinar os dados coletados para uma solicitação de direitos de entidade usando ferramentas de redação, marcas de arquivo. Entenda como usar a funcionalidade de colaboração, que inclui um canal Teams dedicado.

Depois que os dados forem coletados para uma solicitação de direitos de entidade, o próximo estágio será examinar os itens de conteúdo, decidir quais itens incluir ou excluir como parte da solicitação e reexamá-lo, se necessário.

## <a name="tasks-for-completing-the-data-review"></a>Tarefas para concluir a revisão de dados

Neste estágio, seus colaboradores devem examinar as descobertas na **guia Dados coletados**. Um Teams canal será configurado automaticamente para facilitar a revisão de conteúdo por todos os stakeholders. Consulte [Colaboração para revisão de dados](#collaboration-for-data-review) abaixo para obter mais detalhes. As tarefas essenciais para a etapa de revisão de dados são descritas abaixo.

#### <a name="mark-items-as-include-or-exclude-and-add-notes"></a>Marcar itens como Incluir ou Excluir e adicionar anotações

Examine a lista de itens identificados retornados pela pesquisa. Se você decidir que o item deve ser incluído como parte do relatório final de volta ao assunto dos dados, selecione  Incluir na barra de comandos na parte superior da lista de itens. Você também pode selecionar o botão **azul** Incluir na área de revisão de conteúdo à direita da lista de itens. Quando você seleciona **Incluir**, um painel de submenu é exibido com uma opção para adicionar anotações. Quando terminar, selecione Enviar **para** salvar o status de revisão do item como **Incluir**.

Se o item não pertencer como parte da solicitação, selecione Excluir na  barra de comandos ou o botão Excluir  na área de revisão de conteúdo. Excluir um item significa que ele não será incluído nos relatórios [finais gerados para o titular dos dados](subject-rights-requests-reports.md).

> [!NOTE]
> Se você marcar um item como **Exclude**, será necessário adicionar uma anotação como justificativa para o motivo pelo qual ele não pertence à solicitação de direitos do assunto. As anotações são para fins internos e não estão incluídas nos relatórios finais.

Se o conteúdo parecer ser um falso positivo, selecione Não **uma** correspondência e, no painel de submenu, selecione **Confirmar**. Essa ação excluirá o arquivo dos relatórios finais e sinalizará o item como algo que não deveria ter sido detectado na pesquisa.

#### <a name="apply-tags"></a>Apply tags

As marcas podem ser usadas para ajudá-lo a identificar itens que precisam de mais atenção. Priva fornece três marcas **padrão – Acompanhamento****,** Exclusão e **Atualização – para** as quais você pode definir uma descrição. Priva também fornece duas marcas personalizadas que você pode nomear e descrever.

Por exemplo, se você determinar durante a revisão de dados que um item de conteúdo não precisa ser mantido pela sua organização, poderá aplicar a marca  Excluir e exportar uma lista de todos os arquivos marcados para que você possa voltar e excluir os itens identificados quando terminar a solicitação.

As cinco marcas gerenciadas **em Configurações se** aplicam a todas as suas solicitações de direitos de entidade.

**Para adicionar ou remover marcas:**

- Selecione o item na lista na guia **Dados coletados** da solicitação.
- Na área de visualização do item à direita da lista, selecione o botão Aplicar **marcas** na linha inferior. Você também pode selecionar os três pontos à direita do nome do item e selecionar a **opção Aplicar marcas** .
- Um painel de submenu é exibido com a lista de marcas. Marque a caixa ao lado de qualquer uma das marcas que você deseja aplicar ao item. Desmarcar uma caixa marcada removerá a marca.
- Quando terminar, selecione **Salvar**, que salva suas seleções de marca e fecha o painel de submenu.

**Para adicionar marcas personalizadas ou atualizar descrições de marca:**
- Na página Solicitações de Direitos de Entidade, **selecione Configurações** no canto superior direito da tela para acessar suas Priva configurações.
- Vá para a **página Marcas de revisão de** dados e selecione a marca para inserir uma descrição e, para as marcas personalizadas, um nome. Saiba mais sobre as [configurações de marca](priva-settings.md#data-review-tags).

**Para exportar uma lista de itens marcados:**
- Vá para a **página Dados coletados** em uma solicitação de direitos de entidade.
- Acima da lista de itens, selecione o **comando** Exportar.
- Um Excel será baixado, que mostra as propriedades de todos os itens coletados pela pesquisa para a solicitação. Localize **a coluna** Marcas para identificar e classificar os itens por marca.

#### <a name="use-the-annotate-command-to-redact-text"></a>Usar o comando Anotação para reatar o texto
O **comando Anotar na** área de revisão de conteúdo permite que você crie marcações embutidas e redacte dados em um item de conteúdo. Por exemplo, se você precisar incluir um arquivo para um indivíduo que também contém as informações pessoais de um assunto de dados diferente, poderá usar a **redação** área sob o botão Desenho na barra de comandos para excluir todas as informações que não pertencem à pessoa que fez a solicitação. Quando as edições forem concluídas, selecione **Incluir** para adicionar o arquivo editado à solicitação. A anotação cria uma cópia do arquivo, que é armazenada no blob do Azure. O arquivo original permanece inalterado e armazenado em seu local original.

#### <a name="enter-notes-about-a-file"></a>Inserir anotações sobre um arquivo
Para adicionar ou revisar anotações em um item, selecione o item em sua linha e vá para  a guia Anotações de Arquivo na área de revisão de conteúdo à direita. Você também pode usar a **opção Adicionar anotação de** arquivo para criar um novo comentário. Para revisar ou adicionar anotações em um nível geral de maiúsculas e minúsculas, vá para a guia **Anotações** principal acima e use **a observação Adicionar caso**. Essas anotações estarão visíveis para os usuários que trabalham na solicitação, mas não serão incluídas no relatório final ou compartilhadas de outra forma com o titular dos dados.

## <a name="collaboration-for-data-review"></a>Colaboração para revisão de dados

Os administradores de solicitação de direitos de entidade podem exibir todas as solicitações. Você pode adicionar outros usuários para colaborar em uma solicitação, o que dará a eles acesso para exibir essa solicitação e trabalhar com os dados coletados nela para ajudar a mover a solicitação para a conclusão.

Quando você cria uma solicitação, um canal Teams dedicado é criado automaticamente para que os stakeholders discutam a solicitação e compartilhem com segurança entradas e contribuições. A **guia Colaboradores** na página de detalhes da solicitação mostra todos os colaboradores que podem exibir e contribuir para a solicitação e para qualquer canal Teams associado.

Para adicionar mais colaboradores, selecione Adicionar **colaborador, comece** a digitar o nome do usuário, selecione o nome quando ele aparecer e, em seguida, **selecione Adicionar**.

Para iniciar um Teams chat, qualquer colaborador pode selecionar **Chat** com colaboradores no canto superior direito da página de detalhes da solicitação. Essa ação abre Teams e coloca **você no canal** Geral do site de equipe da solicitação de direitos de assunto.

Você pode alterar o comportamento padrão da criação de Teams canais para solicitações de direitos de entidade indo para Priva **Configurações** no canto superior direito da Solicitação de Direitos da Entidade. Selecione **Teams colaboração** e desmarque a caixa na página para desativar Teams recursos para todos os direitos de entidade.

O **comando** Compartilhar no canto superior direito da página de detalhes de uma solicitação cria um link compartilhável que vai diretamente para a solicitação em Priva. Forneça esse link aos colaboradores para que eles possam acessar a solicitação à qual você os adicionou.

## <a name="complete-the-review"></a>Concluir a revisão

Quando todos os itens tiverem sido revisados e você tiver definido seu status como **Incluir, Excluir** ou Não uma correspondência, é hora de fechar **a** etapa de revisão. Qualquer um dos colaboradores em uma solicitação pode concluir a revisão.

Selecione o **botão Revisão** Completa no canto superior direito da solicitação. Um painel de submenu mostrará um resumo dos dados e adicionará anotações relacionadas. Essas anotações são para manter registros internos e não são compartilhadas com o titular dos dados.

Selecione **Concluir revisão** no painel de submenu para concluir a etapa de revisão. Essa ação prepara a solicitação para os estágios finais do processo: gerar relatórios e fechar a solicitação. Resumos de suas decisões serão fornecidos posteriormente na **guia** Relatórios.

## <a name="next-steps"></a>Próximas etapas
Saiba como gerar o relatório final e trabalhar para a conclusão da solicitação em [Gerar relatórios e fechar uma solicitação](subject-rights-requests-reports.md).

## <a name="legal-disclaimer"></a>Aviso de isenção de responsabilidade legal

[Microsoft Priva aviso de isenção de responsabilidade legal](priva-disclaimer.md)
