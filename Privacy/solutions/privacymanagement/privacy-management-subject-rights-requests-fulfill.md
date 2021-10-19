---
title: Gerenciar relatórios de solicitações de direitos de assunto e atender solicitações no gerenciamento de privacidade
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
description: Saiba como gerenciar os pacotes de dados criados pelo gerenciamento de privacidade para solicitações de direitos de assunto e atender à solicitação ao assunto dos dados.
ms.openlocfilehash: 424bb4edc6ddcab86200d76cee767bc9699b281a
ms.sourcegitcommit: 85e085eb17af8b4efd1f45207445e1b3c3679600
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/19/2021
ms.locfileid: "60478063"
---
# <a name="manage-subject-rights-requests-reports-and-fulfill-requests"></a>Gerenciar relatórios de solicitações de direitos de assunto e atender solicitações

Depois de concluir sua revisão de dados para uma solicitação de direitos de assunto, você pode seguir em frente para solicitar o atendimento. O gerenciamento de privacidade criará relatórios e coletará os arquivos marcados para **Incluir** durante o processo de revisão de dados. Os arquivos selecionados desses pacotes de dados podem ser enviados ao seu assunto de dados para concluir a solicitação. O gerenciamento de privacidade também dá suporte ao uso da API de solicitações Microsoft 365 de direitos de assunto para introduzir recursos de automação.

## <a name="prepare-final-reports-for-the-data-subject"></a>Preparar relatórios finais para o assunto de dados

O pacote de dados de solicitação de direitos de assunto é gerado como um arquivo zip. Pode levar até 30 minutos para gerar esse pacote. Quando estiver pronto, abra sua solicitação de direitos de  assunto na página solicitações de direitos de assunto, abra a guia Relatórios, localmente seu download e abra o arquivo zip.

O pacote de dados contém uma variedade de arquivos. Os arquivos fora da pasta do Azure são fornecidos para referência e devem ser usados principalmente pelos administradores. Os materiais-chave para seu titular de dados estão contidos na **pasta do Azure.**

Recomendamos analisar cuidadosamente o conteúdo dessa pasta e enviar apenas os arquivos necessários ao titular dos dados. Você deve avaliar sua resposta para garantir que ela seja adaptada para atender aos requisitos da lei aplicável.

### <a name="azure-folder-contents"></a>Conteúdo da pasta do Azure

Abra essa pasta e abra o arquivo **AEDExport.zip.** O conteúdo inclui:

- A **Extracted_text_files** contém texto extraído dos arquivos nativos (onde há suporte).
- A **pasta NativeFiles** contém todos os **itens Incluídos** no formato de arquivo nativo.
- Os arquivos redacted estão na **pasta NativeFiles** e têm o sufixo "_burn.pdf".
- Os arquivos exportados são renomeados usando identificadores exclusivos para ajudar a proteger dados pessoais. Você pode fazer referência cruzada aos nomes exclusivos com os nomes de arquivo originais usando o **Export_load_file.csv**. Como os nomes de arquivo originais podem incluir informações confidenciais, você deve seguir suas políticas que se aplicam a essas informações.

Depois de revisar o conteúdo do arquivo zip, modifique-o conforme necessário para remover qualquer conteúdo que você não queira incluir no pacote final. Depois de concluir, envie-o com segurança para seu assunto de dados.

## <a name="integrate-with-partner-solutions"></a>Integrar com soluções de parceiros

Você pode integrar o módulo Microsoft 365 Solicitação de Direitos de Assunto com seus processos e ferramentas de negócios existentes aproveitando a API de solicitação de direitos de assunto Microsoft 365 assunto. Isso oferece uma maneira simples, porém poderosa, de introduzir a automação em sua estratégia de direitos de assunto.

Quando os titulares de dados solicitam informações de sua organização, você pode aproveitar nossas APIs para criar essas solicitações em Microsoft 365 com base nos critérios personalizados para essa solicitação. Você pode criar a solicitação de direitos de assunto no Microsoft 365, acompanhar o andamento da solicitação por meio de suas etapas e confirmar quando a solicitação tiver concluído o processamento e o conteúdo estiver pronto para ser recuperado. Nossas APIs estão disponíveis para qualquer pessoa usar para tornar suas soluções mais extensíveis: sejam para ISVs, parceiros para acomodar para Microsoft 365 em suas soluções ou para que as organizações usem com seus aplicativos de linha de negócios.

Para saber mais, confira Usar a API de solicitação Graph [direitos de assunto da Microsoft.](/graph/api/resources/subjectrightsrequest-subjectrightsrequestapioverview)

## <a name="manage-data-retention"></a>Gerenciar retenção de dados

Relatórios gerados por meio dessa ferramenta e dados associados, como arquivos anotados salvos no Azure, são armazenados por um período de tempo especificado. Essa duração é definida em nível global Configurações **na** seção **Períodos** de retenção de dados, que permite escolher entre 30 e 90 dias. Verifique se esses períodos de retenção de dados estão em conformidade com suas políticas e obrigações legais.

## <a name="legal-disclaimer"></a>Aviso de isenção de responsabilidade legal

[Aviso de isenção de responsabilidade legal de gerenciamento de privacidade](privacy-management-disclaimer.md)
