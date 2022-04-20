---
title: Definir permissões de usuário e atribuir funções no Microsoft Priva
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
description: Saiba como configurar permissões do Microsoft Priva e atribuir usuários a grupos de funções.
ms.openlocfilehash: 14ae1b1b9ee1f1ccc8d3a1914f0d7308a8467f23
ms.sourcegitcommit: 09ecdaded9a9f8f79587f2acb978dc53b83e5c01
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/19/2022
ms.locfileid: "64930612"
---
# <a name="set-user-permissions-and-assign-roles-in-microsoft-priva"></a>Definir permissões de usuário e atribuir funções no Microsoft Priva

Para conceder aos membros da sua organização permissões para usar o Microsoft Priva, atribua-os aos grupos de funções apropriados no portal de conformidade do Microsoft Purview.

> [!NOTE]
> No momento, a maioria das funções Priva é designada como "gerenciamento de privacidade". Veja abaixo uma lista completa. Funções específicas de Priva não aparecerão no Azure Active Directory.

## <a name="sign-in-and-set-permissions"></a>Entrar e definir permissões

1. Acesse o [portal de conformidade do Microsoft Purview](https://compliance.microsoft.com/) e selecione **Permissões** no painel de navegação esquerdo.  
2. Na lista **suspensa Centro de conformidade** , selecione **Funções**. A lista completa de grupos de funções será exibida.
3. Localize o grupo de funções ao qual você deseja adicionar um ou mais usuários e marque a caixa à esquerda do nome do grupo.
4. No painel de submenu desse grupo, selecione **Editar** **no cabeçalho Membros** .  
5. Selecione **Escolher membros**. Outra janela de submenu será exibida.
6. Selecione **+ Adicionar** para escolher um ou mais usuários para adicionar ao grupo.  
7. Marque a caixa de seleção ao lado dos nomes que você deseja adicionar e, em seguida, selecione o **botão** Adicionar na parte inferior.  
8. Quando terminar de atribuir usuários, selecione **Concluído****, Salve e** **Feche**.

## <a name="learn-more-about-role-groups-and-roles"></a>Saiba mais sobre grupos de funções e funções

Dependendo da estrutura da sua equipe, você tem opções para atribuir usuários a grupos de funções específicos para gerenciar diferentes conjuntos de recursos priva. Os membros devem ser atribuídos a grupos de funções dependendo de quais tarefas precisam realizar e qual nível de acesso a arquivos é apropriado. Cada grupo de funções inclui uma ou mais funções. Essas funções podem pertencer a tarefas Específicas priva ou funções-chave que estão habilitadas ou restritas para os membros desse grupo. Diferentes usuários podem, portanto, ter diferentes níveis de visibilidade e acesso a determinados recursos priva.

Os grupos de funções podem ser personalizados, se necessário. Para evitar a perda acidental de acesso, é recomendável criar uma cópia do grupo de funções existente que você deseja personalizar, dando à cópia um nome identificável, fazendo e verificando suas alterações no novo grupo e atribuindo pessoas a ele conforme apropriado.

## <a name="privacy-management-role-group"></a>Grupo de funções de Gerenciamento de Privacidade

Esse grupo contém todas as funções de permissão Priva em um único grupo. Esse grupo de funções pode ser uma boa opção para organizações em que o mesmo indivíduo pode executar todas as tarefas. Fornecer associação a esse grupo de funções concederá a essa conta acesso completo a todos os recursos do Priva para os quais você tem uma licença.

É recomendável garantir que sempre haja pelo menos um membro ativo desse grupo.

As funções incluem:

- Gerenciamento de Casos  
- Visualizador de Conteúdo de Classificação de Dados  
- Visualizador de Lista de Classificação de Dados  
- Administrador de Gerenciamento de Privacidade  
- Análise de Gerenciamento de Privacidade  
- Investigação de Gerenciamento de Privacidade  
- Contribuição Permanente do Gerenciamento de Privacidade  
- Contribuição Temporária do Gerenciamento de Privacidade  
- Visualizador de Gerenciamento de Privacidade  
- Administrador de Solicitação de Direitos de Entidade  
- View-Only caso

## <a name="privacy-management-administrators-role-group"></a>Grupo de função Administradores de Gerenciamento de Privacidade

Os membros desse grupo de funções têm amplo acesso às funções Priva, incluindo a criação, leitura, atualização e exclusão de políticas de gerenciamento de risco de privacidade, solicitações de direitos de entidade, permissões e configurações.

As funções incluem:

- Gerenciamento de Casos  
- Administrador de Gerenciamento de Privacidade  
- View-Only caso

## <a name="privacy-management-analysts-role-group"></a>Grupo de função Analistas de Gerenciamento de Privacidade

Os membros desse grupo de funções atuam como analistas de caso. Eles podem investigar as correspondentes à política, exibir metadados de arquivo e executar ações de correção. Esse grupo não pode acessar arquivos completos por meio do Explorador de Conteúdo.

As funções incluem:

- Gerenciamento de Casos  
- Visualizador de Lista de Classificação de Dados  
- Análise de Gerenciamento de Privacidade  
- View-Only caso

### <a name="privacy-management-investigators-role-group"></a>Grupo de função Investigadores de Gerenciamento de Privacidade

Os membros desse grupo atuam como investigadores de dados. Eles podem investigar as correspondentes à política, exibir o conteúdo do arquivo associado e executar ações de correção. Esse grupo pode acessar arquivos por meio do Explorador de Conteúdo.

As funções incluem:

- Gerenciamento de Casos  
- Visualizador de Conteúdo de Classificação de Dados  
- Visualizador de Lista de Classificação de Dados  
- Investigação de Gerenciamento de Privacidade  
- View-Only caso

## <a name="privacy-management-viewer-role-group"></a>Grupo de funções do Visualizador de Gerenciamento de Privacidade

Os membros desse grupo podem exibir informações analíticas em Priva, como a visão geral, o perfil de dados e os relatórios de solicitação de assunto.

As funções incluem:

- Visualizador de Gerenciamento de Privacidade

## <a name="subject-rights-request-administrators-role-group"></a>Grupo de função Administradores de Solicitação de Direitos de Entidade

Os membros desse grupo têm acesso completo para administrar e criar solicitações de direitos de entidade.

As funções incluem:

- Administrador de Solicitação de Direitos de Entidade

## <a name="privacy-management-contributors-role-group"></a>Grupo de função Colaboradores do Gerenciamento de Privacidade

Os membros desse grupo têm acesso a solicitações de direitos de entidade para as quais foram adicionados como colaboradores.  

As funções incluem:

- Contribuição Temporária do Gerenciamento de Privacidade  
- Contribuição Permanente do Gerenciamento de Privacidade

## <a name="legal-disclaimer"></a>Aviso de isenção de responsabilidade legal

[Aviso de isenção de responsabilidade legal da Microsoft Priva](priva-disclaimer.md)