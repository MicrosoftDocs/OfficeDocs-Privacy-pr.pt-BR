---
title: Gerar relatórios e fechar uma solicitação
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
description: Saiba como gerenciar os pacotes de dados criados pelo Microsoft Priva para solicitações de direitos de entidade e atender à solicitação ao titular dos dados.
ms.openlocfilehash: 44113c480f81e6ef885de3649d9e04810c776d7c
ms.sourcegitcommit: 3c83e8133a5a71f4e1d76a0b2981ab3ec9cd6602
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/13/2022
ms.locfileid: "66046685"
---
# <a name="generate-reports-and-close-a-request"></a>Gerar relatórios e fechar uma solicitação

**Neste artigo**: entenda os tipos de relatórios gerados em Solicitações de Direitos de Entidade. Saiba mais sobre os períodos de retenção para os dados coletados e encontre instruções para fornecer resultados ao titular dos dados e fechar a solicitação.

Depois de concluir a revisão de dados para uma solicitação de direitos de entidade, o próximo estágio é gerar os relatórios necessários para atender à solicitação. Priva criará relatórios e coletará os arquivos marcados como **Incluir durante** o processo de revisão de dados. Os arquivos selecionados desses pacotes de dados podem ser enviados ao titular dos dados para concluir a solicitação.

## <a name="understanding-reports"></a>Noções básicas sobre relatórios

Depois de selecionar **Concluir revisão** **no estágio De** revisão de dados da solicitação de direitos da entidade, os relatórios finais da solicitação começarão a ser gerados automaticamente. Na guia **Relatórios da** página de detalhes de solicitações de direitos de entidade, a coluna **Status** indica quando a  geração do relatório está em andamento e quando um relatório está **Pronto para download**. Pode levar até 30 minutos para concluir a criação dos relatórios.

Os relatórios são divididos em duas seções:
1. **Relatórios para o titular dos dados**: esses relatórios contêm informações que podem ser retornadas ao titular dos dados como parte do cumprimento da solicitação. É aqui que você encontrará o pacote **de dados** que contém arquivos para enviar ao titular dos dados.
   > [!IMPORTANT]
   > Um pacote de dados só será gerado se você marcar itens como **Incluir durante** a revisão de dados.

   > [!IMPORTANT]
   > Um pacote de dados só será gerado para tipos **de solicitações de Exportação** e Acesso. Um pacote de dados não será gerado para uma lista **marcada para solicitação de** acompanhamento. Examine os detalhes sobre os [tipos de solicitação de direitos de entidade](subject-rights-requests-create.md#request-types).

2. **Relatórios para uso interno**: esses relatórios são para os registros internos da sua organização relacionados à solicitação de direitos de entidade. Eles incluem um log de auditoria e uma lista de todos os arquivos aos quais você aplicou marcas durante a revisão de dados para acompanhar ou executar outras ações.

> [!NOTE]
> Quando os relatórios são gerados, a organização conclui a solicitação enviando os relatórios apropriados de maneira segura para o titular dos dados a fim de atender à solicitação de direitos da entidade. Se o titular dos dados solicitou a exclusão de seus dados, é responsabilidade da organização identificar itens para exclusão e realizar a exclusão.

## <a name="data-package"></a>Pacote de dados

O pacote de dados de solicitação de direitos de entidade contém itens marcados como **Include** durante o estágio de revisão de dados do processo. O pacote de dados é gerado como um arquivo zip. Quando estiver pronto para download, selecione a linha do relatório na guia Relatórios da página  de detalhes da solicitação de direitos de assunto. Um painel de submenu será aberto com um botão para **Baixar** o relatório. As **próximas instruções what do do** no painel de submenu fornecem uma referência rápida sobre como trabalhar com o conteúdo.

Quando estiver pronto para baixar o pacote de dados, selecione **Baixar**, localize o download e abra o arquivo zip baixado.

### <a name="contents-of-the-data-package"></a>Conteúdo do pacote de dados

O arquivo zip do pacote de dados contém os seguintes itens:

- Uma pasta chamada **Azure**: essa pasta contém os materiais principais para o assunto dos dados. Confira a explicação detalhada abaixo.
- Arquivos fora da pasta **do Azure** : eles podem incluir duas planilhas chamadas **Resultados** e **Resumo**. Esses arquivos fora da pasta do Azure são fornecidos para referência e devem ser usados principalmente pelos administradores da sua organização.

Quando Priva identifica e recupera arquivos para uma solicitação de direitos de entidade, os arquivos exportados nesse processo são renomeados usando identificadores exclusivos para ajudar a proteger dados pessoais. Você pode fazer referência cruzada aos nomes exclusivos com os nomes de arquivo originais usando o **Export_load_file.csv** arquivo. Como os nomes de arquivo originais podem incluir informações confidenciais, você deve seguir suas políticas que se aplicam a essas informações.

> [!NOTE]
> É recomendável examinar o conteúdo dessa pasta com cuidado e enviar apenas os arquivos necessários para o titular dos dados. Você deve avaliar sua resposta para garantir que ela seja adaptada para atender aos requisitos da lei aplicável.

### <a name="azure-folder-contents"></a>Conteúdo da pasta do Azure

Abra **a pasta do Azure** e abra o arquivo **AEDExport.zip** , que contém outra pasta de arquivos com um nome longo composto por números e letras. Abra a pasta com o nome longo para revelar o conteúdo descrito abaixo:

- **Extracted_text_files** : contém texto extraído dos arquivos nativos (quando compatível).
- **Pasta NativeFiles** : contém todos os itens marcados durante a revisão de dados como **Incluídos**, em seu formato de arquivo nativo. Cada item nessa pasta recebe um nome de arquivo exclusivo para proteger dados pessoais. Você pode fazer referência cruzada a esses nomes exclusivos com o nome de arquivo original usando o arquivo Export_load_file.csv, explicado abaixo.
  - Os arquivos que foram editados usando a função **Anotação** durante o processo de revisão de dados estão na pasta **NativeFiles** e têm o sufixo "_burn.pdf".
- **Export_load_file.csv** : contém os nomes de arquivo originais para que você possa fazer referência cruzada a eles com os nomes de arquivo exclusivos fornecidos na pasta NativeFiles.
- **Arquivo** de texto de resumo: fornece um resumo dos tipos de arquivos no pacote de dados, o número de arquivos e seu tamanho.

##### <a name="what-to-do-with-the-folder-contents"></a>O que fazer com o conteúdo da pasta

Abra a **pasta do Azure** e os arquivos zip, conforme explicado acima. Sua próxima tarefa é examinar os itens, determinar o que enviar para o titular dos dados e modificar o conteúdo do arquivo zip, se necessário.

Por exemplo, para uma solicitação de exportação em que o titular dos dados deseja receber uma cópia de todos os itens que contêm seus dados pessoais mantidos pela organização, você desejará examinar de perto os itens na pasta **NativeFiles** e remover qualquer item que não deseja enviar de volta para o titular dos dados.

Para uma solicitação de acesso em que o titular dos dados deseja receber um resumo de todas as suas informações pessoais mantidas pela organização, você deve se concentrar no arquivo **de** texto Resumo.

Modifique o arquivo zip para remover qualquer conteúdo que você não queira incluir no pacote final. Depois de concluído, envie o arquivo zip de maneira segura para o titular dos dados que fez a solicitação de direitos de entidade.

## <a name="audit-log"></a>Log de auditoria

O log de auditoria é um arquivo CSV que fornece um registro da progressão de estágios para cada solicitação de direitos de entidade. Ele lista cada estágio do processo juntamente com a data e a hora concluídas e o nome de usuário do indivíduo que concluiu a etapa.

## <a name="tagged-files-reports"></a>Relatórios de arquivos marcados

Os relatórios rotulados como **Arquivos marcados como...** são arquivos CSV que listam os itens de conteúdo aos quais as marcas foram aplicadas durante o processo de revisão de dados. As marcas são usadas para sinalizar itens de conteúdo para maior atenção ou ação da organização. Saiba mais sobre [as configurações de marcas](priva-settings.md#data-review-tags).

## <a name="retention-periods-for-reports-and-data"></a>Períodos de retenção para relatórios e dados

Relatórios gerados por Solicitações de Direitos de Entidade e dados associados, como arquivos anotados salvos no Azure, são armazenados por um período de tempo especificado. O período de retenção padrão é de 30 dias a partir da data em que uma solicitação de direitos de entidade é fechada.

O período de retenção de dados é definido Priva **Configurações** aplica-se a todas as solicitações de direitos de entidade. Para exibir ou alterar o período de retenção de dados, siga as etapas abaixo:

1. Em qualquer lugar Solicitações de direitos do titular Priva, **selecione Configurações** (o ícone de engrenagem) no canto superior direito da tela.
2. Selecione **Períodos de retenção de** dados no painel de navegação esquerdo.
3. No menu **suspenso Dados coletados** e relatórios, selecione 30 dias ou 90 dias como o período de retenção.
4. Selecione **Salvar** para salvar suas configurações.

Verifique se os períodos de retenção de dados escolhidos estão em conformidade com as políticas e obrigações legais da sua organização.

## <a name="close-the-request"></a>Fechar a solicitação

Quando você tiver executado todas as ações necessárias relacionadas à solicitação de direitos de entidade, marque a solicitação como  fechada selecionando Fechar a solicitação no canto superior direito da página de detalhes da solicitação. Uma solicitação fechada significa que ela não está mais ativa e indica que nenhum trabalho adicional é necessário para atender à solicitação original do titular dos dados para sua organização.

As solicitações fechadas não podem ser reabertos, mas você pode retornar à solicitação para exibir detalhes e anotações da solicitação. Os relatórios para a solicitação são retidos de acordo com o período de [retenção estabelecido](#retention-periods-for-reports-and-data).

## <a name="legal-disclaimer"></a>Aviso de isenção de responsabilidade legal

[Microsoft Priva aviso de isenção de responsabilidade legal](priva-disclaimer.md)
