---
title: Correspondência de dados para solicitações de direitos de entidade
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
description: Saiba como carregar informações adicionais para o Microsoft Priva sobre seus assuntos de dados.
ms.openlocfilehash: 90ee0e8e21d25954c11113992cbb7ece847c85ab
ms.sourcegitcommit: 6b88d22d0250cbb9a4ba1f71665f29cb67939851
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/05/2022
ms.locfileid: "65059735"
---
# <a name="data-matching-for-subject-rights-requests"></a>Correspondência de dados para solicitações de direitos de entidade

Com a correspondência de dados, as organizações podem permitir que o Microsoft Priva identifique os titulares dos dados com base nos valores de dados fornecidos exatos. Isso pode ajudar a aumentar a precisão da localização do conteúdo do titular dos dados que corresponde a esses valores de dados tanto para sua equipe interna quanto para usuários externos com os quais você interage. Ele também simplifica a necessidade de fornecer campos manualmente durante a criação da solicitação de direitos de assunto e fornece contexto dentro de solicitações de direitos de assunto e para o bloco Visão geral que mostra seus itens com a maioria do conteúdo do titular dos dados. Para saber mais sobre essa exibição, [consulte Localizar e visualizar dados pessoais em Priva](priva-data-profile.md#items-with-the-most-data-subject-content).

Para usar o recurso de correspondência de dados, você precisará ser membro do grupo de função Gerenciamento de Privacidade. De dentro de Priva no [portal de conformidade do Microsoft Purview](https://compliance.microsoft.com/), selecione **Configurações** na navegação superior e, em seguida, correspondência **de dados**. A partir daqui, você precisará definir o esquema de dados pessoais e fornecer um upload de dados pessoais, conforme mostrado abaixo. Observe que você pode adicionar itens e excluir itens adicionados, mas não pode modificar um item.

## <a name="prepare-for-data-import"></a>Preparar-se para a importação de dados

Antes de definir o esquema ou carregar dados, você precisará identificar a origem das informações do titular dos dados. O formato de arquivo necessário é .csv, que pode ser lido por um aplicativo como Microsoft Excel. Estruturar essa exportação para que os cabeçalhos de coluna apareçam na primeira linha. Esses cabeçalhos devem incluir os nomes dos atributos para o esquema de dados pessoais. Verifique o formato dos dados em cada campo. Se algum dos dados contiver vírgulas, coloque esses valores entre aspas duplas para garantir que eles não sejam analisados em campos separados.

## <a name="define-the-personal-data-schema"></a>Definir o esquema de dados pessoais

A primeira etapa na configuração da correspondência de dados é definir o esquema de dados pessoais, que descreverá os atributos para seus titulares de dados. Você carregará esse esquema na primeira guia na área de configurações de correspondência de dados. Os arquivos necessários incluem **um arquivo** XML de esquema de dados pessoais e um arquivo XML **do pacote de** regras.

### <a name="personal-data-schema-xml"></a>XML do esquema de dados pessoais

O arquivo de esquema de dados pessoais é um arquivo XML que definirá quais nomes de coluna são esperados.

- Nomeie esse arquivo de *esquemapdm.xml*.
- Defina cada nome de coluna usando a marca Nome do Campo, conforme visto no exemplo abaixo.
- Use searchable = "true" para campos que você deseja pesquisar, até um máximo de cinco campos. Pelo menos um de seus nomes de campo deve ser pesquisável. Sintaxe de exemplo: `\<Field name="" searchable=""/>`.
- O esquema de dados pessoais tem uma seção de marca DataStore. Quatro campos obrigatórios devem ser mapeados para seus nomes de campo: primaryKeyField, upnField, firstNameField, lastNameField.

Por exemplo, o seguinte arquivo XML define um esquema de exemplo, com cinco campos especificados como pesquisáveis: PatientID, MRN, SSN, Telefone e DOB. O primaryKeyField é mapeado para PatientID, upnField é mapeado para MRN, firstNameField é mapeado para FirstName e lastNameField é mapeado para LastName.

Você pode copiar, modificar e usar nosso exemplo.

 ```xml
<PdmSchema xmlns="http://schemas.microsoft.com/office/2020/pdm">
      <DataStore name="Patientrecords" description="Schema for patient records" version="1" primaryKeyField="PatientID" upnField="MRN" firstNameField="FirstName" lastNameField="LastName">
            <Field name="PatientID" searchable="true"/>
            <Field name="MRN" searchable="true" />
            <Field name="FirstName" />
            <Field name="LastName" />
            <Field name="SSN" searchable="true" />
            <Field name="Phone" searchable="true" />
            <Field name="DOB" searchable="true" />
            <Field name="Gender" />
            <Field name="Address" />
      </DataStore>
</PdmSchema>
 ```

### <a name="rule-package-xml"></a>XML do pacote de regras

Ao configurar o pacote de regras, certifique-se de fazer referência corretamente ao arquivo de esquema de dados pessoais criado acima: pdm.xml. No xml do pacote de regras de exemplo a seguir, os campos a seguir precisam ser personalizados para criar o tipo confidencial de correspondência de dados:

- **ID** &  de RulePack **ID PrivacyMatch**: use New-GUID para gerar um GUID.
- **Armazenamento de** dados: esse campo especifica o armazenamento de dados de pesquisa de correspondência de dados pessoais a ser usado. Forneça o nome do DataStore definido de um esquema de dados pessoais configurado.
- **idMatch**: esse campo aponta para o elemento primário para a correspondência de dados pessoais.
  - **Correspondências**: especifica o campo a ser usado na pesquisa exata. Forneça um nome de campo pesquisável do esquema de dados pessoais.
  - **Classificação**: esse campo especifica a correspondência de tipo confidencial que dispara a pesquisa de correspondência de dados pessoais. Você pode fornecer o nome ou o GUID de um tipo de informação confidencial interno ou personalizado existente. Para evitar causar problemas de desempenho, se você usar um tipo de informação confidencial personalizado como o elemento Classificação na correspondência de dados pessoais, não use um tipo de informação confidencial personalizado que corresponda a uma grande porcentagem de conteúdo (como "qualquer número" ou "qualquer palavra de cinco letras"). É recomendável adicionar palavras-chave de suporte ou incluir formatação na definição do tipo de informação confidencial de classificação personalizada.
- **Correspondência**: esse campo aponta para evidências adicionais encontradas na proximidade de idMatch.
  - **Corresponde**: forneça qualquer nome de campo no esquema de dados pessoais para o DataStore.
- **Recurso**: esta seção especifica o nome e a descrição do tipo confidencial em várias localidades.
  - **idRef**: forneça o GUID para a ID ExactMatch.
  - **Nome & descrições**: personalize conforme necessário.

Em nosso exemplo xml do pacote de regras abaixo, estamos referenciando o arquivo de exemplo pdm.xml da etapa anterior que cria o XML do esquema de dados pessoais:

- **Armazenamento de** dados: o nome do dataStore faz referência ao arquivo de esquema que criamos anteriormente: dataStore = "PatientRecords".
- **idMatch**: o valor idMatch faz referência a um campo pesquisável listado no arquivo pdm.xml que criamos anteriormente: idMatch matches = "SSN".
  - **Classificação**: o valor de classificação faz referência a um tipo de informação confidencial existente ou personalizada: classificação = "Número do SEGURO SOCIAL (SSN)". (Nesse caso, usamos o tipo de informação confidencial existente do Número de Seguridade Social dos EUA.)

Crie um pacote de regras no formato XML (com codificação Unicode), como no código de exemplo a seguir. Você pode copiar, modificar e usar este exemplo.

 ```xml
<RulePackage xmlns="http://schemas.microsoft.com/office/2020/pdm">
  <RulePack id="fd098e03-1796-41a5-8ab6-198c93c62b21">
    <Version build="0" major="2" minor="0" revision="0" />
    <Publisher id="eb553734-8306-44b4-9ad5-c388ad970528" />
    <Details defaultLangCode="en-us">
      <LocalizedDetails langcode="en-us">
        <PublisherName>IP DLP</PublisherName>
        <Name>Health Care PDM Rulepack</Name>
        <Description>This rule package contains the Personal Data Match sensitive type for health care sensitive types.</Description>
      </LocalizedDetails>
    </Details>
  </RulePack>
  <Rules>
    <PrivacyMatch id = "E1CC861E-3FE9-4A58-82DF-4BD259EAB381" patternsProximity = "300" dataStore ="PatientRecords" recommendedConfidence = "65" >
      <Pattern confidenceLevel="65">
        <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
        <Any minMatches ="3" maxMatches ="6">
          <match matches="PatientID" />
          <match matches="MRN"/>
          <match matches="FirstName"/>
          <match matches="LastName"/>
          <match matches="Phone"/>
          <match matches="DOB"/>
        </Any>
      </Pattern>
    </PrivacyMatch>
    <LocalizedStrings>
      <Resource idRef="E1CC861E-3FE9-4A58-82DF-4BD259EAB381">
        <Name default="true" langcode="en-us">Patient SSN Exact Match.</Name>
        <Description default="true" langcode="en-us">PDM Sensitive type for detecting Patient SSN.</Description>
      </Resource>
    </LocalizedStrings>
  </Rules>
</RulePackage>
 ```

## <a name="sensitive-info-types"></a>Tipos de informações confidenciais

A segunda etapa na configuração da correspondência de dados é criar tipos de informações confidenciais exclusivos para a correspondência de dados pessoais (PDM). [SiTs (tipos de](/microsoft-365/compliance/sensitive-information-type-learn-about) informações confidenciais) são classificadores baseados em padrões que detectam informações confidenciais, como números de cartão de crédito ou seguro social. Configurar um tipo de informações confidenciais de PDM permite que você use valores de dados exatos em vez de valores genéricos para detectar correspondências. Para iniciar esta etapa, selecione **Criar tipo de informações confidenciais do PDM** para iniciar o assistente de criação.

## <a name="upload-personal-data"></a>Upload dados pessoais

Depois de definir o esquema de dados pessoais e os tipos de informações confidenciais, a terceira etapa é carregar dados pessoais. Vá para **a guia** Upload de dados pessoais, selecione Adicionar e escolha o esquema pessoal que você definiu na primeira etapa e carregue o arquivo que contém os dados pessoais.

Você pode carregar esses dados pessoais escolhendo um arquivo local ou fornecendo uma URL SAS para um local Armazenamento do Microsoft Azure existente que contém seu arquivo de dados pessoais.
Se você preparou um arquivo como a primeira etapa nesse processo que está em conformidade com o esquema criado, poderá usar esse arquivo para o upload.

## <a name="legal-disclaimer"></a>Aviso de isenção de responsabilidade legal

[Aviso de isenção de responsabilidade legal da Microsoft Priva](priva-disclaimer.md)
