---
title: Criar políticas no Gerenciamento de Riscos de Privacidade
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
search.appverid:
- MOE150
- MET150
description: Saiba como criar e personalizar políticas de privacidade para lidar com os dados pessoais da sua organização Microsoft 365.
ms.openlocfilehash: 6a8fa5a77e681f9626bfc28e53d193986b40e0cb
ms.sourcegitcommit: 3d00addbca48a7393cf4e4b67ef24696fb9b7dd8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/15/2022
ms.locfileid: "64865770"
---
# <a name="create-policies-in-privacy-risk-management"></a>Criar políticas no Gerenciamento de Riscos de Privacidade

Você pode criar novas políticas no Gerenciamento de Riscos de Privacidade para lidar com cenários de risco importantes para sua organização. Para um início rápido, use os modelos padrão para criar novas políticas para superexposure de dados, transferências de dados e minimização de dados e cenários. Você também pode personalizar suas próprias políticas, usando qualquer um desses modelos como ponto de partida.

Ao criar ou editar políticas, você pode configurar notificações por email ou, quando disponível, dicas de política para Teams para chamar a atenção de seus usuários para correção.

## <a name="create-a-policy-from-a-template"></a>Criar uma política com base em um modelo

Siga estas etapas para criar uma política usando qualquer um dos modelos padrão.

1. No [Centro de conformidade do Microsoft 365,](https://compliance.microsoft.com/) vá para a seção Gerenciamento de Risco de Privacidade de Priva e selecione **Políticas**.
1. Selecione **Criar uma política**.
1. Escolha o tipo de modelo desejado. Isso abrirá um painel de submenu com informações sobre o modelo.
1. Para examinar as configurações padrão do modelo, incluindo tipos de dados, locais de dados e as condições que disparam correspondências de política, selecione **Exibir configurações**.
     - Você tem a opção aqui para selecionar **Editar configurações para** fazer alterações. Isso direcionará você para o assistente para personalizar as configurações.
1. Se você estiver pronto para usar as configurações padrão, dê um nome descritivo à política e selecione **Criar política.**

Ao criar uma política diretamente de um modelo, muitas configurações serão escolhidas automaticamente para você. Ele também será iniciado no modo de teste por padrão, o que significa que nenhum alerta ou notificação será gerado. Se você estiver pronto para ativar totalmente sua política depois de executá-la no modo de teste e examinar os resultados da política, poderá encontrá-la em sua lista de políticas e editar a política para ativá-la.

## <a name="create-a-custom-policy"></a>Criar uma política personalizada

Para assumir o controle granular das configurações de uma política, você pode criar uma política personalizada usando um dos modelos existentes como uma linha de base. Priva fornece um assistente para guiá-lo por estas etapas.

Todos os tipos de política seguem esse fluxo básico. Determinadas configurações e opções serão alteradas dependendo da política escolhida.

1. No [Centro de conformidade do Microsoft 365,](https://compliance.microsoft.com/) vá para a seção Gerenciamento de Risco de Privacidade de Priva e selecione **Políticas**.
1. Selecione **Criar uma política**.
1. Escolha a **opção** Personalizada para começar a usar o assistente.
1. Escolha o tipo de modelo de linha de base: **Superexposure de dados,** **transferências de dados ou** **minimização de dados**. Cada uma delas fornecerá determinadas opções durante a criação da política.
1. Nomeie e descreva sua política. Recomendamos usar nomes claros e descritivos para identificar suas políticas, pois esses nomes aparecerão posteriormente em alertas sobre as correspondentes à política.
1. Prossiga com o assistente e escolha as configurações desejadas. As opções são:
    - **Dados a serem monitorados**: selecione o tipo de dados pessoais que sua política monitorará.
    - **Usuários e grupos**: aplique sua política a todos os usuários ou usuários selecionados.
    - **Locais**: aplique sua política às áreas selecionadas no Microsoft 365.
    - **Condições**: defina as condições para sua política. Essas opções variam dependendo do tipo de política.
    - **Resultados**: defina os resultados quando uma correspondência de política for encontrada, como notificações do usuário.
    - **Alertas**: decida a frequência de alertas para administradores quando uma correspondência de política for encontrada.
    - **Modo**: escolha se deseja ou não executar sua política no modo de teste primeiro.
1. Quando todas as configurações forem concluídas, examine suas escolhas, faça as edições desejadas e selecione **Enviar para criar** a política.

## <a name="learn-about-key-settings-for-all-policies"></a>Saiba mais sobre as principais configurações para todas as políticas

### <a name="choose-data-to-monitor"></a>Escolher dados a serem monitorados

Ao editar ou configurar qualquer tipo de política personalizada, você será solicitado a selecionar quais tipos de dados sua política deve monitorar. As opções são as seguintes:

- **Grupos de classificação**: uma lista pesquisável de conjuntos de dados com base nas principais regulamentações de privacidade, como GDPR ou HIPAA. Exiba detalhes de qualquer grupo para ver quais tipos de informações confidenciais ele aborda. Selecione um ou mais desses conjuntos para usá-los como estão.
- **Tipos de informações confidenciais** individuais: ao escolher tipos de informações confidenciais específicos por conta própria, como números de seguro social ou informações de carteira de motorista, você pode personalizar seu próprio grupo ou grupos de dados para procurar. Este assistente permite que você selecione na lista completa de tipos de informações confidenciais no Gerenciamento de Riscos de Privacidade. Cada tipo de informação tem suas próprias propriedades. Use o botão de informações ao lado de qualquer um deles para obter detalhes e anotações sobre as configurações recomendadas. Se você criar mais de um grupo, o assistente permitirá que você aplique operadores boolianos para relacioná-los e definir sua ordem de operações.

Se você selecionar entre os grupos de classificação existentes, também não poderá selecionar tipos individuais ou criar seus próprios grupos. Para obter mais flexibilidade, escolha tipos de informações confidenciais individuais. Para utilizar os padrões mais comuns, escolha entre os grupos de classificação.

### <a name="set-user-email-notifications"></a>Definir notificações de email do usuário

Com [as notificações por email](risk-management-notifications.md), você pode enviar notificações sobre as correspondentes à política diretamente para seus proprietários de conteúdo. Esses emails resumem quais dados precisam ser revisados e possíveis ações a serem tomadas, como tornar documentos particulares, mantê-los no arquivo, relatar quaisquer resultados falsos positivos e adicionar anotações para referência futura. Esses emails também incluem links para destinatários de treinamento sobre como lidar com esses casos. Fornecer esses links é necessário e deve apontar para sua própria documentação interna sobre processos e práticas recomendadas.

As notificações podem ser habilitadas para políticas individuais durante a criação de política personalizada ou ao editar qualquer política. Defina suas preferências na **seção Resultados** .

As configurações necessárias incluem a frequência de suas notificações e o link para o treinamento de privacidade.

As configurações opcionais incluem determinados campos personalizáveis para seus emails. Selecione a **opção Visualizar e editar email de** notificação para abrir um painel de submenu que mostra uma notificação de exemplo. Aqui, você pode editar a linha de assunto do email, o cabeçalho e o corpo do texto e o nome de exibição e a URL do treinamento de privacidade.

Observe que a capacidade geral do Gerenciamento de Riscos de Privacidade para enviar notificações por email é **controlada Configurações.** Ele está habilitado por padrão. Desativar essa configuração interromperá todos os emails mesmo que as notificações tenham sido configuradas em um nível de política individual.

## <a name="learn-about-settings-for-data-minimization-policies"></a>Saiba mais sobre as configurações para políticas de minimização de dados

As políticas de minimização de dados se concentram na idade do conteúdo e quanto tempo passou desde a última modificação. O monitoramento de dados pessoais que ainda estão sendo retidos em conteúdo antigo e não utilizado pode ajudá-lo a gerenciar melhor os dados armazenados e reduzir os riscos. Essa configuração é tratada na **tela Condições** .

Por padrão, as políticas de minimização de dados pesquisam conteúdo que contém dados pessoais que foram criados ou modificados pela última vez há pelo menos 30 dias. Ao editar ou criar uma política personalizada, você pode selecionar entre outros períodos de tempo predefinidos.

## <a name="learn-about-settings-for-data-transfer-policies"></a>Saiba mais sobre as configurações para políticas de transferência de dados

As políticas de transferência de dados permitem monitorar transferências de dados pessoais fora da sua organização, bem como transferências internas entre diferentes departamentos ou países ou regiões. Na tela **Condições** , você pode escolher quais tipos de transferências o Gerenciamento de Riscos de Privacidade deve procurar.

Por padrão, as políticas de transferência de dados detectam quando os dados pessoais em sua organização são transferidos ou compartilhados com um destinatário ou local fora da sua organização. Ao editar ou criar uma política personalizada, você pode escolher o tipo de transferência e, em seguida, fazer seleções para as regiões ou departamentos do remetente e destinatário.

As políticas de transferência de dados também dão suporte ao fornecimento de dicas de política e recomendações aos usuários no Teams, para que eles possam se manter informados sobre as práticas recomendadas para lidar com os dados. Isso pode ser alternado na **tela Resultados** .

## <a name="learn-about-settings-for-data-overexposure-policies"></a>Saiba mais sobre as configurações para políticas de superexposição de dados

Sua organização pode armazenar conteúdo em vários níveis de acesso, incluindo áreas publicamente acessíveis e outras restritas. Na tela **Condições** , você pode optar por fazer com que o Gerenciamento de Riscos de Privacidade procure a superexposição de dados potenciais para o conteúdo armazenado em qualquer um dos seguintes níveis de acesso:

- **Público**: qualquer pessoa com um link pode exibir esse conteúdo.
- **Externo**: pessoas específicas fora da organização têm acesso.
- **Interno**: os usuários em sua organização têm acesso.

Por padrão, as políticas de superexposição de dados avaliam todos os três níveis de acesso. Ao editar ou criar uma política personalizada, você pode escolher todos ou qualquer um desses níveis.

## <a name="next-steps"></a>Próximas etapas

Para obter mais informações sobre como gerenciar suas políticas e fazer alterações depois que elas forem criadas, consulte [Gerenciar políticas](risk-management-policies-manage.md).

## <a name="legal-disclaimer"></a>Aviso de isenção de responsabilidade legal

[Aviso de isenção de responsabilidade legal da Microsoft Priva](priva-disclaimer.md)
