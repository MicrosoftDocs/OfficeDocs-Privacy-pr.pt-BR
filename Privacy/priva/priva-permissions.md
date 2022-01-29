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
description: Saiba como configurar permissões do Microsoft Priva e atribuir usuários a grupos de função.
ms.openlocfilehash: bcc2e108f10e427e55034621f2f8b5c40e6d9184
ms.sourcegitcommit: f145dff5e387a8e26db2f3a2c7de125978fbacc9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/28/2022
ms.locfileid: "62248830"
---
# <a name="set-user-permissions-and-assign-roles-in-microsoft-priva"></a>Definir permissões de usuário e atribuir funções no Microsoft Priva

Para dar aos membros da sua organização permissões para usar o Microsoft Priva, atribua-os aos grupos de função apropriados no Centro de conformidade do Microsoft 365.

> [!NOTE]
> A maioria das funções Priva atualmente são designadas como "gerenciamento de privacidade". Confira abaixo uma lista completa. Funções específicas de Priva não serão exibidas Azure Active Directory.

## <a name="sign-in-and-set-permissions"></a>Entrar e definir permissões

1. Vá para o [Centro de conformidade do Microsoft 365](https://compliance.microsoft.com/) e selecione **Permissões** na navegação à esquerda.  
2. Na lista **suspenso do Centro de Conformidade** , selecione **Funções**. A lista completa de grupos de funções será exibida.
3. Encontre o grupo de funções ao qual você deseja adicionar um ou mais usuários e marque a caixa à esquerda do nome do grupo.
4. No painel sublinhado para esse grupo, selecione **Editar** no header **Membros** .  
5. Selecione **Escolher membros**. Outra janela de sobrevoo aparecerá.
6. Selecione **+ Adicionar** para escolher um ou mais usuários para adicionar ao grupo.  
7. Selecione a caixa de seleção ao lado dos nomes que você deseja adicionar e selecione o botão **Adicionar** na parte inferior.  
8. Quando terminar de atribuir usuários, selecione **Feito** e **Salvar** e **Fechar**.

## <a name="learn-more-about-role-groups-and-roles"></a>Saiba mais sobre grupos de funções e funções

Dependendo da estrutura da sua equipe, você tem opções para atribuir usuários a grupos de função específicos para gerenciar diferentes conjuntos de recursos Priva. Os membros devem ser atribuídos a grupos de funções, dependendo das tarefas que precisam realizar e qual nível de acesso a arquivos é apropriado. Cada grupo de funções inclui uma ou mais funções. Essas funções podem pertencer a tarefas específicas Priva ou funções-chave que estão habilitadas ou restritas para os membros desse grupo. Os usuários diferentes podem, portanto, ter níveis diferentes de visibilidade e acesso a determinados recursos Priva.

Os grupos de funções podem ser personalizados, se necessário. Para evitar perda acidental de acesso, recomendamos criar uma cópia do grupo de funções existente que você deseja personalizar, dando à cópia um nome identificável, fazendo e verificando suas alterações no novo grupo e atribuindo as pessoas a ele conforme apropriado.

## <a name="privacy-management-role-group"></a>Grupo de função Gerenciamento de Privacidade

Este grupo contém todas as funções de permissão Priva em um único grupo. Esse grupo de funções pode ser um bom ajuste para organizações em que o mesmo indivíduo pode executar todas as funções. Fornecer associação neste grupo de funções concederá a essa conta acesso total a todos os recursos de Priva para os quais você tem uma licença.

Recomendamos garantir que sempre haja pelo menos um membro ativo desse grupo.

As funções incluem:

- Gerenciamento de Casos  
- Visualizador de Conteúdo de Classificação de Dados  
- Visualizador de Lista de Classificação de Dados  
- Administrador de Gerenciamento de Privacidade  
- Análise de Gerenciamento de Privacidade  
- Investigação de Gerenciamento de Privacidade  
- Contribuição Permanente do Gerenciamento de Privacidade  
- Contribuição Temporária de Gerenciamento de Privacidade  
- Visualizador de Gerenciamento de Privacidade  
- Administrador de Solicitação de Direitos de Assunto  
- View-Only Caso

## <a name="privacy-management-administrators-role-group"></a>Grupo de função Administradores de Gerenciamento de Privacidade

Os membros desse grupo de funções têm amplo acesso às funções Priva, incluindo a criação, leitura, atualização e exclusão de políticas de gerenciamento de riscos de privacidade, solicitações de direitos de assunto, permissões e configurações.

As funções incluem:

- Gerenciamento de Casos  
- Administrador de Gerenciamento de Privacidade  
- View-Only Caso

## <a name="privacy-management-analysts-role-group"></a>Grupo de função Analistas de Gerenciamento de Privacidade

Os membros desse grupo de funções atuam como analistas de caso. Eles podem investigar as combinações de política, exibir metadados de arquivo e realizar ações de correção. Esse grupo não pode acessar arquivos completos por meio do Explorador de Conteúdo.

As funções incluem:

- Gerenciamento de Casos  
- Visualizador de Lista de Classificação de Dados  
- Análise de Gerenciamento de Privacidade  
- View-Only Caso

### <a name="privacy-management-investigators-role-group"></a>Grupo de função Investigadores de Gerenciamento de Privacidade

Os membros desse grupo atuam como investigadores de dados. Eles podem investigar as combinações de política, exibir o conteúdo do arquivo associado e realizar ações de correção. Esse grupo pode acessar arquivos por meio do Explorador de Conteúdo.

As funções incluem:

- Gerenciamento de Casos  
- Visualizador de Conteúdo de Classificação de Dados  
- Visualizador de Lista de Classificação de Dados  
- Investigação de Gerenciamento de Privacidade  
- View-Only Caso

## <a name="privacy-management-viewer-role-group"></a>Grupo de função do Visualizador de Gerenciamento de Privacidade

Os membros desse grupo podem exibir informações analíticas em Priva, como a visão geral, o perfil de dados e os relatórios de solicitação de assunto.

As funções incluem:

- Visualizador de Gerenciamento de Privacidade

## <a name="subject-rights-request-administrators-role-group"></a>Grupo de função Administradores de Solicitação de Direitos de Assunto

Os membros desse grupo têm acesso total para administrar e criar solicitações de direitos de assunto.

As funções incluem:

- Administrador de Solicitação de Direitos de Assunto

## <a name="privacy-management-contributors-role-group"></a>Grupo de função Colaboradores de Gerenciamento de Privacidade

Os membros desse grupo têm acesso a solicitações de direitos de assunto para as quais foram adicionadas como colaboradores.  

As funções incluem:

- Contribuição Temporária de Gerenciamento de Privacidade  
- Contribuição Permanente do Gerenciamento de Privacidade

## <a name="legal-disclaimer"></a>Aviso de isenção de responsabilidade legal

[Aviso de isenção de responsabilidade legal da Microsoft Priva](priva-disclaimer.md)