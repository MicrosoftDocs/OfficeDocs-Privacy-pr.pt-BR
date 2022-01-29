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
ms.openlocfilehash: b906fbc3a07ac67cec2c2a4b0433065d42c665e2
ms.sourcegitcommit: f145dff5e387a8e26db2f3a2c7de125978fbacc9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/28/2022
ms.locfileid: "62248851"
---
# <a name="create-a-subject-rights-request"></a>Criar uma solicitação de direitos de assunto

Os administradores de gerenciamento de direitos de assunto podem abrir novas solicitações por meio da página principal solicitações de direitos de assunto de Priva. Um assistente o orientará durante o processo de encontrar dados pessoais sobre um titular de dados e iniciar o processo de atendimento de sua solicitação.

Você também pode optar por carregar material adicional para permitir que Priva identifique titulares de dados com base nos valores de dados fornecidos exatos. Para saber mais, confira [Correspondência de dados para Solicitações de Direitos de Assunto](subject-rights-requests-data-match.md).

## <a name="use-the-subject-rights-request-creation-wizard"></a>Usar o assistente de criação de solicitação de direitos de assunto

1. Na [Centro de conformidade do Microsoft 365,](https://compliance.microsoft.com/) vá para a seção Priva e selecione **Priva Subject Rights Requests**.
1. Para iniciar uma nova solicitação, selecione **Criar uma solicitação**.
1. Identifique o sujeito de dados que fez a solicitação e especifique sua relação com sua empresa.
1. Executaremos uma pesquisa padrão para itens relacionados ao assunto de dados. Se quiser refinar sua pesquisa ou obter uma estimativa antes de recuperarmos dados, você pode fazer essas seleções neste estágio. Você também pode deixar todos os itens em branco e ir para a próxima etapa. Para obter mais informações sobre suas opções, consulte [Definir configurações de pesquisa](#define-search-settings) e [Refinar sua pesquisa](#refine-your-search).
1. Escolha um tipo de solicitação com base no que o assunto de dados deseja que você faça com seus dados. Se a solicitação estiver relacionada a uma regulamentação específica de privacidade de dados, você também poderá selecioná-la em uma lista fornecida para adicionar mais contexto. Definir um prazo (obrigatório) facilita a classificação para solicitações de aproximação ou atraso e resolvê-las em tempo hábil. Os tipos de solicitação incluem:
   - **Access**: fornece um resumo das informações pessoais do entidade de dados mantidas pela sua organização em Microsoft 365.
   - **Exportar**: fornece um resumo e uma exportação das informações pessoais do assunto de dados, conforme coletado e anotado durante a revisão.
   - **Lista marcada para** acompanhamento: gera um resumo de todos os arquivos que os usuários marcam durante a revisão que podem exigir ações adicionais fora de Priva. Por exemplo, talvez seja necessário facilitar a exclusão das informações pessoais do assunto de dados por solicitação. Marcas de revisão de dados personalizadas para solicitações de direitos de assunto podem ser gerenciadas em um Configurações **.**
1. Confirme o nome dessa solicitação e adicione uma descrição opcional para referência.
1. Revise o resumo do que você entrou durante as etapas anteriores. Qualquer campo pode ser editado antes de selecionar **Criar solicitação**.

### <a name="define-search-settings"></a>Definir configurações de pesquisa

Ao criar uma solicitação de direitos de assunto, você pode escolher uma ou todas essas opções de pesquisa para encontrar dados sobre o assunto:

- **Inclua conteúdo de autoria do assunto de** dados: isso inclui conteúdo de autoria do assunto de dados e pode retornar um volume maior de dados.
- **Refine sua pesquisa**: isso permitirá que você especifique propriedades extras que o ajudarão a identificar o assunto dos dados. Aqui você pode fazer o escopo de sua pesquisa Microsoft 365 serviços ou recursos específicos ou selecionar outras condições para ajustar o escopo da solicitação. Depois de escolher essa opção, você será solicitado a inserir seus parâmetros de pesquisa personalizados.
- **Obter uma estimativa primeiro**: isso permite que você veja quantos dados esperamos encontrar antes que seus dados são recuperados automaticamente.

### <a name="refine-your-search"></a>Refinar sua pesquisa

Se você optar por refinar sua pesquisa ao definir suas configurações de pesquisa, será solicitado a preencher seus parâmetros de pesquisa avançados. Você pode **adicionar identificadores, definir** **condições e** escolher **locais específicos** dentro Microsoft 365 pesquisa.

- **Adicionar identificadores**: forneça mais informações de identificação sobre o assunto dos dados, como nomes, endereços de email e/ou outras opções. Separe vários valores em cada campo com um ponto e vírgula.
- **Condições**: comece a adicionar condições para sua pesquisa escolhendo um tipo no menu suspenso. Esses tipos correspondem a propriedades possíveis dos dados, como o período, o tamanho, os rótulos de retenção, os destinatários e os destinatários e muitos outros. Selecione qualquer tipo para adicioná-lo e, em seguida, de definir suas propriedades desejadas. Para entradas de campo de texto, você pode adicionar várias palavras-chave separadas por pontos-e-vírgulas. Você pode adicionar quantos tipos de conteúdo desejar.
- **Locais**: você pode escopo de sua pesquisa para direcionar sites SharePoint específicos, canais Teams e OneDrive for Business locais específicos. Para cada local, você pode selecionar todas as instâncias, como todas Exchange caixas de correio ou instâncias específicas, como a caixa de correio de um usuário. Selecione o link **Escolher...** para cada opção de local para inserir informações sobre instâncias específicas. Para ajudar a identificar os termos de pesquisa apropriados, consulte o seguinte:
  - [Gerenciar sites no novo SharePoint](/sharepoint/manage-sites-in-new-admin-center) de administração: fornece orientações sobre como classificar e filtrar sites e como pesquisar um site SharePoint site. Use isso para encontrar URLs para o campo SharePoint pesquisa.
  - [Get-Team](/powershell/module/teams/get-team): fornece informações sobre como encontrar equipes Microsoft Teams propriedades/informações específicas. Use isso para ajudá-lo a identificar Teams chats e canais.
  - [Sobre OneDrive URLs](/onedrive/list-onedrive-urls#about-onedrive-urls): fornece informações sobre o formato adequado e as propriedades para a URL de OneDrive usuário. Use isso para ajudá-lo a identificar OneDrive sites em sua pesquisa.

Recomendamos revisar cuidadosamente suas seleções para garantir que você identifique o assunto de dados correto. Por exemplo, se você pesquisar caixas de correio pelo nome e encontrar vários indivíduos com nomes semelhantes, verifique a correta antes de adi adiá-las à sua solicitação.

## <a name="next-steps"></a>Próximas etapas

Depois de criar sua solicitação, você a verá listada na página de solicitação de direitos de assunto. Para saber mais sobre como prosseguir com a revisão, consulte [Revisar dados e colaborar em solicitações](subject-rights-requests-data-review.md).

## <a name="legal-disclaimer"></a>Aviso de isenção de responsabilidade legal

[Aviso de isenção de responsabilidade legal da Microsoft Priva](priva-disclaimer.md)
