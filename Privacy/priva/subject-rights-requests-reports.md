---
title: Gerar relatórios e atender a uma solicitação de direitos de assunto
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
description: Saiba como gerenciar os pacotes de dados criados pelo Microsoft Priva para solicitações de direitos de assunto e atender à solicitação ao assunto de dados.
ms.openlocfilehash: 8a6a41188de78508401b0dfffb3d7cdefb2320a5
ms.sourcegitcommit: 4965df24fdc907f7a6e397f2c78019aaf72c7580
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/17/2022
ms.locfileid: "63564441"
---
# <a name="generate-reports-and-fulfill-a-subject-rights-request"></a>Gerar relatórios e atender a uma solicitação de direitos de assunto

Depois de concluir sua revisão de dados para uma solicitação de direitos de assunto no Microsoft Priva, você pode seguir em frente para solicitar o atendimento. Priva criará relatórios e coletará os arquivos marcados para **Incluir** durante o processo de revisão de dados. Os arquivos selecionados desses pacotes de dados podem ser enviados ao seu assunto de dados para concluir a solicitação. Priva também dá suporte ao uso da API de solicitações Microsoft 365 direitos de assunto para introduzir recursos de automação.

## <a name="understanding-reports"></a>Noções básicas sobre relatórios

Depois de selecionar **Concluir revisão** no estágio **Revisar** dados da solicitação de direitos de assunto, os relatórios finais da solicitação começarão a gerar automaticamente. Na guia **Relatórios da** página detalhes de solicitações de direitos de assunto, a coluna **Status** indica quando a geração  do relatório está em andamento e quando um relatório está **pronto para download**. Pode levar até 30 minutos para concluir a criação dos relatórios.

Os relatórios são divididos em duas seções:
1. **Relatórios para o assunto de dados**: Esses relatórios contêm informações que podem ser retornadas ao assunto dos dados como parte do atendimento da solicitação. É aqui que você encontrará o pacote **de dados** que contém arquivos para você enviar para o assunto de dados.
   > [!IMPORTANT]
   > Um pacote de dados só será gerado se você marcar itens como **Include** durante a revisão de dados.

   > [!IMPORTANT]
   > Um pacote de dados só será gerado para tipos **de solicitações de Exportação** **e Acesso** . Um pacote de dados não será gerado para uma lista **marcada para solicitação de acompanhamento** . Revise detalhes sobre tipos [de solicitação de direitos de assunto](subject-rights-requests-create.md#use-the-subject-rights-request-creation-wizard).

2. **Relatórios para uso interno**: esses relatórios são para os registros internos da sua organização relacionados à solicitação de direitos de entidade. Eles incluem um log de auditoria e uma lista de todos os arquivos aos que você aplicou marcas durante a revisão de dados para acompanhar ou realizar outras ações.

## <a name="prepare-final-reports-for-the-data-subject"></a>Preparar relatórios finais para o assunto de dados

O pacote de dados de solicitação de direitos de assunto é gerado como um arquivo zip. Pode levar até 30 minutos para gerar esse pacote. Quando estiver pronto, abra sua solicitação de direitos de assunto na página solicitações de direitos de assunto, abra a guia Relatórios, localmente o download e abra o arquivo zip.

O pacote de dados contém uma variedade de arquivos. Os arquivos fora da pasta do Azure são fornecidos para referência e devem ser usados principalmente pelos administradores. Os materiais-chave para seu titular de dados estão contidos na **pasta do Azure** .

Recomendamos analisar cuidadosamente o conteúdo dessa pasta e enviar apenas os arquivos necessários ao titular dos dados. Você deve avaliar sua resposta para garantir que ela seja adaptada para atender aos requisitos da lei aplicável.

### <a name="azure-folder-contents"></a>Conteúdo da pasta do Azure

Abra essa pasta e abra o arquivo **AEDExport.zip** . O conteúdo inclui:

- A **Extracted_text_files** contém texto extraído dos arquivos nativos (onde há suporte).
- A **pasta NativeFiles** contém todos os **itens Incluídos** no formato de arquivo nativo.
- Os arquivos redacted estão na **pasta NativeFiles** e têm o sufixo "_burn.pdf".
- Os arquivos exportados são renomeados usando identificadores exclusivos para ajudar a proteger dados pessoais. Você pode fazer referência cruzada aos nomes exclusivos com os nomes de arquivo originais usando o **Export_load_file.csv**. Como os nomes de arquivo originais podem incluir informações confidenciais, você deve seguir suas políticas que se aplicam a essas informações.

Depois de revisar o conteúdo do arquivo zip, modifique-o conforme necessário para remover qualquer conteúdo que você não queira incluir no pacote final. Depois de concluir, envie-o com segurança para seu assunto de dados.

## <a name="integrate-with-partner-solutions"></a>Integrar com soluções de parceiros

Você pode integrar a solução Priva Subject Rights Requests com seus processos e ferramentas de negócios existentes usando a API de solicitação de direitos de assunto Microsoft 365 assunto. Usar a API oferece uma maneira simples, porém poderosa, de introduzir a automação em sua estratégia de direitos de assunto.

Quando os titulares de dados solicitam informações de sua organização, nossas APIs podem ajudar a criar essas solicitações dentro Microsoft 365 com base nos critérios exclusivos da solicitação. Você pode criar a solicitação de direitos de assunto no Microsoft 365, acompanhar o andamento da solicitação por meio de suas etapas e confirmar quando a solicitação tiver concluído o processamento e o conteúdo estiver pronto para ser recuperado. Nossas APIs estão disponíveis para qualquer pessoa usar para tornar suas soluções mais extensíveis: seja para ISVs, parceiros para acomodar para Microsoft 365 em suas soluções ou para que as organizações usem com seus aplicativos de linha de negócios.

Para saber mais, confira [Usar a API de solicitação Graph direitos de assunto da Microsoft](/graph/api/resources/subjectrightsrequest-subjectrightsrequestapioverview).

## <a name="manage-data-retention"></a>Gerenciar retenção de dados

Relatórios gerados por meio dessa ferramenta e dados associados, como arquivos anotados salvos no Azure, são armazenados por um período de tempo especificado. O período de retenção de dados é definido em Priva **Configurações** e se aplica a todas as solicitações de direitos de assunto. Para exibir ou alterar seus períodos de retenção de dados, siga as etapas abaixo:

1. Em qualquer lugar em Priva Subject Rights Requests, **selecione Configurações** (o ícone de engrenagem) no canto superior direito da tela.
2. Selecione **Períodos de retenção de dados** na navegação à esquerda.
3. Usando o menu suspenso, selecione 30 ou 90 dias como o período de retenção.

Verifique se os períodos de retenção de dados escolhidos estão em conformidade com as políticas e obrigações legais da sua organização.

## <a name="legal-disclaimer"></a>Aviso de isenção de responsabilidade legal

[Aviso de isenção de responsabilidade legal da Microsoft Priva](priva-disclaimer.md)
