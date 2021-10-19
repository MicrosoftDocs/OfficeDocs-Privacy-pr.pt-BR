---
title: Definir permissões do usuário e atribuir funções no gerenciamento de privacidade
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
description: Saiba como configurar permissões de gerenciamento de privacidade e atribuir usuários a grupos de função.
ms.openlocfilehash: 52ffb6ee47aea93f906e1356abf61979eca34787
ms.sourcegitcommit: 85e085eb17af8b4efd1f45207445e1b3c3679600
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/19/2021
ms.locfileid: "60478080"
---
# <a name="set-user-permissions-and-assign-roles-in-privacy-management"></a>Definir permissões do usuário e atribuir funções no gerenciamento de privacidade

Para dar aos membros da sua organização permissões para usar o gerenciamento de privacidade, atribua-os aos grupos de função apropriados no Centro de conformidade do Microsoft 365. Observe que funções específicas do gerenciamento de privacidade não aparecerão em Azure Active Directory.

## <a name="sign-in-and-set-permissions"></a>Entrar e definir permissões

1. Vá para o [Centro de conformidade do Microsoft 365](https://compliance.microsoft.com/) e selecione **Permissões** na navegação à esquerda.  
2. Na lista **suspenso do Centro de Conformidade,** selecione **Funções**. A lista completa de grupos de funções será exibida.
3. Encontre o grupo de funções ao qual você deseja adicionar um ou mais usuários e marque a caixa à esquerda do nome do grupo. Confira abaixo uma lista de funções de gerenciamento de privacidade.  
4. No painel sublinhado para esse grupo, selecione **Editar** no header **Membros.**  
5. Selecione **Escolher membros**. Outra janela de sobrevoo aparecerá.
6. Selecione **+ Adicionar** para escolher um ou mais usuários para adicionar ao grupo.  
7. Selecione a caixa de seleção ao lado dos nomes que você deseja adicionar e selecione o botão **Adicionar** na parte inferior.  
8. Quando terminar de atribuir usuários, selecione **Done**, then **Save**, then **Close**.

## <a name="learn-more-about-role-groups-and-roles"></a>Saiba mais sobre grupos de funções e funções

Dependendo da estrutura da sua equipe, você tem opções para atribuir usuários a grupos de função específicos para gerenciar diferentes conjuntos de recursos de gerenciamento de privacidade. Os membros devem ser atribuídos a grupos de funções, dependendo das tarefas que precisam realizar e qual nível de acesso a arquivos é apropriado. Cada grupo de funções inclui uma ou mais funções. Essas funções podem pertencer a tarefas específicas de gerenciamento de privacidade ou funções-chave habilitadas ou restritas para os membros desse grupo. Os usuários diferentes podem, portanto, ter níveis diferentes de visibilidade e acesso a determinados recursos de gerenciamento de privacidade.

Os grupos de funções podem ser personalizados, se necessário. Para evitar perda acidental de acesso, recomendamos criar uma cópia do grupo de funções existente que você deseja personalizar, dando à cópia um nome identificável, fazendo e verificando suas alterações no novo grupo e atribuindo as pessoas a ele conforme apropriado.

## <a name="privacy-management-role-group"></a>Grupo de função Gerenciamento de Privacidade

Esse grupo contém todas as funções de permissão de gerenciamento de privacidade em um único grupo. Esse grupo de funções pode ser um bom ajuste para organizações onde o mesmo indivíduo pode executar todas as obrigações dentro da solução de gerenciamento de privacidade. Fornecer associação nesse grupo de funções concederá a essa conta acesso total a todos os recursos da solução de gerenciamento de privacidade.

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

Os membros desse grupo de funções têm amplo acesso a funções de gerenciamento de privacidade, incluindo a criação, leitura, atualização e exclusão de políticas de gerenciamento de privacidade, solicitações de direitos de assunto, permissões de gerenciamento de privacidade e configurações de gerenciamento de privacidade.

As funções incluem:

- Gerenciamento de Casos  
- Administrador de Gerenciamento de Privacidade  
- View-Only Caso

## <a name="privacy-management-analysts-role-group"></a>Grupo de função Analistas de Gerenciamento de Privacidade

Os membros desse grupo de funções atuam como analistas de caso de gerenciamento de privacidade. Eles podem investigar as combinações de política, exibir metadados de arquivo e realizar ações de correção. Esse grupo não pode acessar arquivos completos por meio do Explorador de Conteúdo.

As funções incluem:

- Gerenciamento de Casos  
- Visualizador de Lista de Classificação de Dados  
- Análise de Gerenciamento de Privacidade  
- View-Only Caso

### <a name="privacy-management-investigators-role-group"></a>Grupo de função Investigadores de Gerenciamento de Privacidade

Os membros desse grupo atuam como investigadores de dados de gerenciamento de privacidade. Eles podem investigar as combinações de política, exibir o conteúdo do arquivo associado e realizar ações de correção. Esse grupo pode acessar arquivos por meio do Explorador de Conteúdo.

As funções incluem:

- Gerenciamento de Casos  
- Visualizador de Conteúdo de Classificação de Dados  
- Visualizador de Lista de Classificação de Dados  
- Investigação de Gerenciamento de Privacidade  
- View-Only Caso

## <a name="privacy-management-viewer-role-group"></a>Grupo de função do Visualizador de Gerenciamento de Privacidade

Os membros desse grupo podem exibir informações analíticas no gerenciamento de privacidade, como a visão geral, o perfil de dados e os relatórios de solicitação de assunto.

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

[Aviso de isenção de responsabilidade legal de gerenciamento de privacidade](privacy-management-disclaimer.md)