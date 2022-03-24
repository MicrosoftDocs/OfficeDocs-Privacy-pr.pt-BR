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
ms.openlocfilehash: a72dfb53e4f642cd2c567896c854af2beaedd416
ms.sourcegitcommit: beeb693075ef692e95d679f366301df8517b2ac3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63765514"
---
# <a name="generate-reports-and-fulfill-a-subject-rights-request"></a>Gerar relatórios e atender a uma solicitação de direitos de assunto

Depois de concluir sua revisão de dados para uma solicitação de direitos de assunto no Microsoft Priva, você pode seguir em frente para atender à solicitação. Priva criará relatórios e coletará os arquivos marcados como **Include** durante o processo de revisão de dados. Os arquivos selecionados desses pacotes de dados podem ser enviados ao seu assunto de dados para concluir a solicitação. Priva também dá suporte ao uso da API de solicitações Microsoft 365 direitos de assunto para introduzir recursos de automação.

## <a name="understanding-reports"></a>Noções básicas sobre relatórios

Depois de selecionar **Concluir revisão** no estágio **Revisar** dados da solicitação de direitos de assunto, os relatórios finais da solicitação começarão a gerar automaticamente. Na guia **Relatórios da** página detalhes de solicitações de direitos de assunto, a coluna **Status** indica quando a geração  do relatório está em andamento e quando um relatório está **pronto para download**. Pode levar até 30 minutos para concluir a criação dos relatórios.

Os relatórios são divididos em duas seções:
1. **Relatórios para o assunto de dados**: Esses relatórios contêm informações que podem ser retornadas ao assunto dos dados como parte do atendimento da solicitação. É aqui que você encontrará o pacote **de dados** que contém arquivos para você enviar para o assunto de dados.
   > [!IMPORTANT]
   > Um pacote de dados só será gerado se você marcar itens como **Include** durante a revisão de dados.

   > [!IMPORTANT]
   > Um pacote de dados só será gerado para tipos **de solicitações de Exportação** **e Acesso** . Um pacote de dados não será gerado para uma lista **marcada para solicitação de acompanhamento** . Revise detalhes sobre tipos [de solicitação de direitos de assunto](subject-rights-requests-create.md#use-the-subject-rights-request-creation-wizard).

2. **Relatórios para uso interno**: esses relatórios são para os registros internos da sua organização relacionados à solicitação de direitos de entidade. Eles incluem um log de auditoria e uma lista de todos os arquivos aos que você aplicou marcas durante a revisão de dados para acompanhar ou realizar outras ações.

> [!NOTE]
> Quando os relatórios são gerados, a organização conclui a solicitação enviando os relatórios apropriados de forma segura para o assunto dos dados para atender à solicitação de direitos do assunto. Se o entidade de dados solicitou a exclusão de seus dados, é responsabilidade da organização identificar itens para exclusão e realizar a exclusão.

## <a name="data-package"></a>Pacote de dados

O pacote de dados de solicitação de direitos de assunto contém itens marcados como **Include** durante o estágio de revisão de dados do processo. O pacote de dados é gerado como um arquivo zip. Quando estiver pronto para download, selecione a linha do relatório na guia Relatórios da página  detalhes da solicitação de direitos de assunto. Um painel de sobrevoo será aberto com um botão para **Baixar** o relatório. As **instruções O que fazer em** seguida no painel de sobrevoo fornecem uma referência rápida sobre como trabalhar com o conteúdo.

Quando estiver pronto para baixar o pacote de dados, selecione **Baixar**, encontre o download e abra o arquivo zip baixado.

### <a name="contents-of-the-data-package"></a>Conteúdo do pacote de dados

O arquivo zip do pacote de dados contém os seguintes itens:

- Uma pasta chamada **Azure**: esta pasta contém os materiais-chave para seu titular de dados. Consulte a explicação detalhada abaixo.
- Arquivos fora da pasta **do Azure** : eles podem incluir duas planilhas denominadas **Resultados** e **Resumo**. Esses arquivos fora da pasta do Azure são fornecidos para referência e devem ser usados principalmente pelos administradores da sua organização.

Quando Priva identifica e recupera arquivos para uma solicitação de direitos de assunto, os arquivos exportados nesse processo são renomeados usando identificadores exclusivos para ajudar a proteger dados pessoais. Você pode fazer referência cruzada aos nomes exclusivos com os nomes de arquivo originais usando o **Export_load_file.csv** arquivo. Como os nomes de arquivo originais podem incluir informações confidenciais, você deve seguir suas políticas que se aplicam a essas informações.

> [!NOTE]
> Recomendamos analisar cuidadosamente o conteúdo dessa pasta e enviar apenas os arquivos necessários ao titular dos dados. Você deve avaliar sua resposta para garantir que ela seja adaptada para atender aos requisitos da lei aplicável.

### <a name="azure-folder-contents"></a>Conteúdo da pasta do Azure

Abra a **pasta do Azure** e abra o arquivo **AEDExport.zip** , que contém outra pasta de arquivo com um nome longo composto por números e letras. Abra a pasta com o nome longo para revelar o conteúdo descrito abaixo:

- **Extracted_text_files** : contém texto extraído dos arquivos nativos (onde há suporte).
- **Pasta NativeFiles** : contém todos os itens marcados durante a revisão de dados como **Incluídos**, no formato de arquivo nativo. Cada item nesta pasta recebe um nome de arquivo exclusivo para proteger dados pessoais. Você pode fazer referência cruzada a esses nomes exclusivos com o nome de arquivo original usando o arquivo Export_load_file.csv, explicado abaixo.
  - Os arquivos que foram redacionados usando a função **Anotação** durante o processo de revisão de dados estão na pasta **NativeFiles** e têm o sufixo "_burn.pdf".
- **Export_load_file.csv** : contém os nomes de arquivo originais para que você possa fazer referência cruzada com os nomes de arquivo exclusivos fornecidos na pasta NativeFiles.
- **Arquivo** de texto de resumo: fornece um resumo dos tipos de arquivos no pacote de dados, o número de arquivos e seu tamanho.

##### <a name="what-to-do-with-the-folder-contents"></a>O que fazer com o conteúdo da pasta

Abra a **pasta do Azure** e os arquivos zip conforme explicado acima. Sua próxima tarefa é revisar os itens, determinar o que enviar para o assunto dos dados e modificar o conteúdo do arquivo zip, se necessário.

Por exemplo, para uma solicitação de exportação em que o titular dos dados deseja receber uma cópia de todos os itens que contêm seus dados pessoais mantidos pela organização, você vai querer revisar de perto os itens na pasta **NativeFiles** e remover qualquer item que você não queira enviar de volta ao titular dos dados.

Para uma solicitação de acesso em que o entidade de dados deseja receber um resumo de todas as suas informações pessoais mantidas pela organização, você vai querer se concentrar **no arquivo de** texto Resumo.

Modifique o arquivo zip para remover qualquer conteúdo que você não queira incluir no pacote final. Depois de concluir, envie o arquivo zip de forma segura para o assunto de dados que fez a solicitação de direitos de assunto.

## <a name="audit-log"></a>Log de auditoria

O log de auditoria é um arquivo CSV que fornece um registro da progressão de estágios para cada solicitação de direitos de assunto. Ele lista cada estágio do processo juntamente com a data e a hora concluídas e o nome de usuário do indivíduo que concluiu a etapa.

## <a name="tagged-files-reports"></a>Relatórios de arquivos marcados

Os relatórios rotulados como **Arquivos marcados como...** são arquivos CSV que listam os itens de conteúdo aos quais as marcas foram aplicadas durante o processo de revisão de dados. As marcas são usadas para sinalizar itens de conteúdo para maior atenção ou ação da organização. Saiba mais sobre [configurações para marcas](priva-settings.md#data-review-tags).

## <a name="retention-periods-for-reports-and-data"></a>Períodos de retenção para relatórios e dados

Relatórios gerados por Solicitações de Direitos de Assunto e dados associados, como arquivos anotados salvos no Azure, são armazenados por um período de tempo especificado. O período de retenção padrão é de 30 dias a partir da data em que uma solicitação de direitos de assunto é fechada.

O período de retenção de dados é definido em Priva **Configurações** e se aplica a todas as solicitações de direitos de assunto. Para exibir ou alterar o período de retenção de dados, siga as etapas abaixo:

1. Em qualquer lugar em Priva Subject Rights Requests, **selecione Configurações** (o ícone de engrenagem) no canto superior direito da tela.
2. Selecione **Períodos de retenção de dados** na navegação à esquerda.
3. No menu **suspenso Dados coletados e** relatórios, selecione 30 ou 90 dias como o período de retenção.
4. Selecione **Salvar** para salvar suas configurações.

Verifique se os períodos de retenção de dados escolhidos estão em conformidade com as políticas e obrigações legais da sua organização.

## <a name="integrate-with-partner-solutions"></a>Integrar com soluções de parceiros

Você pode integrar a solução Priva Subject Rights Requests com seus processos e ferramentas de negócios existentes aproveitando a API de solicitação de direitos de assunto Microsoft 365 assunto. Isso oferece uma maneira simples, porém poderosa, de introduzir a automação em sua estratégia de direitos de assunto.

Quando os titulares de dados solicitam informações da sua organização, você pode aproveitar nossas APIs para criar essas solicitações dentro Microsoft 365 com base nos critérios personalizados para essa solicitação. Você pode criar a solicitação de direitos de assunto no Microsoft 365, acompanhar o andamento da solicitação por meio de suas etapas e confirmar quando a solicitação tiver concluído o processamento e o conteúdo estiver pronto para ser recuperado. Nossas APIs estão disponíveis para qualquer pessoa usar para tornar suas soluções mais extensíveis: seja para ISVs, parceiros para acomodar para Microsoft 365 em suas soluções ou para que as organizações usem com seus aplicativos de linha de negócios.

Para saber mais, confira [Usar a API de solicitação Graph direitos de assunto da Microsoft](/graph/api/resources/subjectrightsrequest-subjectrightsrequestapioverview).

## <a name="legal-disclaimer"></a>Aviso de isenção de responsabilidade legal

[Aviso de isenção de responsabilidade legal da Microsoft Priva](priva-disclaimer.md)
