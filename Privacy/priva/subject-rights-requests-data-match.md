---
title: Correspondência de dados para solicitações de direitos de assunto
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
description: Saiba como carregar informações adicionais para o Microsoft Priva sobre seus titulares de dados.
ms.openlocfilehash: 1339962a1c4dba18a1d0b21d8a2cebb17ad0f91a
ms.sourcegitcommit: f145dff5e387a8e26db2f3a2c7de125978fbacc9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/28/2022
ms.locfileid: "62248872"
---
# <a name="data-matching-for-subject-rights-requests"></a>Correspondência de dados para solicitações de direitos de assunto

Com a correspondência de dados, as organizações podem permitir que o Microsoft Priva identifique titulares de dados com base nos valores de dados fornecidos exatos. Isso pode ajudar a aumentar a precisão da localização do conteúdo do assunto de dados que corresponde a esses valores de dados tanto para sua equipe interna quanto para usuários externos com os que você interage. Ele também simplifica a necessidade de fornecer campos manualmente durante a criação de solicitações de direitos de assunto e fornece contexto em solicitações de direitos de assunto e para o item Visão geral que mostra seus itens com o conteúdo de assunto de dados mais. Para saber mais sobre essa exibição, consulte [Find and visualize personal data in Priva](priva-data-profile.md#items-with-the-most-data-subject-content).

Para usar o recurso de correspondência de dados, você precisará ser membro do grupo de função Gerenciamento de Privacidade. Em Priva [no Centro de conformidade do Microsoft 365,](https://compliance.microsoft.com/) selecione **Configurações** na nav superior e, em seguida, **correspondência de dados**. A partir daqui, você precisará definir o esquema de dados pessoais e fornecer um carregamento de dados pessoais, conforme mostrado abaixo. Observe que você pode adicionar itens e excluir itens que você adiciona por meio da interface do usuário. No entanto, você não pode modificar um item no local da interface do usuário no momento.

## <a name="prepare-for-data-import"></a>Preparar para importação de dados

Antes de definir o esquema ou carregar dados, você precisará identificar a origem das informações do seu assunto de dados. O formato de arquivo necessário é .csv, que pode ser lido por um aplicativo como Microsoft Excel. Estrutura essa exportação para que seus headers de coluna apareçam na primeira linha. Esses headers devem incluir os nomes dos atributos para seu esquema de dados pessoais. Verifique o formato dos dados em cada campo. Se algum dos dados contiver vírgulas, cerque esses valores com aspas duplas para garantir que não serão analisados em campos separados.

## <a name="define-the-personal-data-schema"></a>Definir o esquema de dados pessoais

O esquema de dados pessoais descreverá os atributos para seus titulares de dados. Upload esquema na primeira guia da área de configurações de correspondência de dados. Os arquivos necessários incluem **um arquivo** XML de esquema de dados pessoais e um **arquivo XML do pacote de** regras.

### <a name="personal-data-schema-xml"></a>XML do esquema de dados pessoais

O arquivo de esquema de dados pessoais é um arquivo XML que definirá quais nomes de coluna são esperados.

- Nomeia esse arquivo de *esquemapdm.xml*.
- Defina cada nome de coluna usando a marca Nome do Campo, conforme visto no exemplo abaixo.
- Use searchable = "true" para campos que você deseja pesquisar, até um máximo de cinco campos. Pelo menos um de seus nomes de campo deve ser pesquisável. Sintaxe de exemplo: `\<Field name="" searchable=""/>`.
- O esquema de dados pessoais tem uma seção de marca DataStore. Quatro campos obrigatórios devem ser mapeados para seus nomes de campo: primaryKeyField, upnField, firstNameField, lastNameField.

Como exemplo, o arquivo XML a seguir define um esquema de exemplo, com cinco campos especificados como pesquisáveis: PatientID, MRN, SSN, Telefone e DOB. O primaryKeyField é mapeado para PatientID, upnField é mapeado para MRN, firstNameField é mapeado para FirstName e lastNameField é mapeado para LastName.

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

Ao configurar o pacote de regras, faça referência correta ao arquivo de esquema de dados pessoais criado acima: pdm.xml. No seguinte xml do pacote de regras de exemplo, os campos a seguir precisam ser personalizados para criar o tipo de dados que match sensitive:

- **ID** &  rulePack **ID PrivacyMatch**: Use New-GUID para gerar um GUID.
- **Datastore**: este campo especifica o repositório de dados de pesquisa de dados de análise de dados pessoais a ser usado. Forneça o nome dataStore definido de um esquema de dados pessoais configurado.
- **idMatch**: este campo aponta para o elemento principal para a combinação de dados pessoais.
  - **Matches**: Especifica o campo a ser usado na busca exata. Forneça um nome de campo pesquisável do esquema de dados pessoais.
  - **Classificação**: este campo especifica a combinação de tipo sensível que dispara a pesquisa de match de dados pessoais. Você pode fornecer o nome ou o GUID de um tipo de informação confidencial interno ou personalizado existente. Para evitar causar problemas de desempenho, se você usar um tipo de informação confidenciais personalizado como o elemento Classification na correspondência de dados pessoais, não use um tipo de informação confidenciais personalizado que corresponderá a uma grande porcentagem de conteúdo (como "qualquer número" ou "qualquer palavra de cinco letras"). Recomendamos adicionar palavras-chave de suporte ou incluir formatação na definição do tipo de informação confidenciais de classificação personalizada.
- **Match**: este campo aponta para evidências adicionais encontradas na proximidade de idMatch.
  - **Corresponde**: forneça qualquer nome de campo no esquema de dados pessoais para DataStore.
- **Recurso**: esta seção especifica o nome e a descrição do tipo sensível em várias localidades.
  - **idRef**: forneça GUID para a ID ExactMatch.
  - **Nome & descrições**: personalizar conforme necessário.

No exemplo XML do pacote de regras abaixo, estamos referenciando o arquivo pdm.xml exemplo da etapa anterior que cria o XML do esquema de dados pessoais:

- **Datastore**: o nome dataStore faz referência ao arquivo de esquema que criamos anteriormente: dataStore = "PatientRecords".
- **idMatch**: o valor idMatch faz referência a um campo pesquisável listado no arquivo pdm.xml que criamos anteriormente: idMatch matches = "SSN".
  - **Classificação**: o valor de classificação faz referência a um tipo de informação confidenciais existente ou personalizado: classificação = "Número de Segurança Social dos EUA (SSN)". (Nesse caso, usamos o tipo de informação confidencial existente do Número de Seguridade Social dos EUA.)

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

## <a name="upload-personal-data"></a>Upload dados pessoais
Depois de definir o esquema de dados pessoais, você pode executar o **carregamento** de dados pessoais na segunda guia da página de configurações de correspondência de dados. Quando você selecionar **Adicionar**, escolha o esquema pessoal que você definiu na primeira etapa e carregue o arquivo que contém os dados pessoais.

Você pode carregar esses dados pessoais escolhendo um arquivo local ou fornecendo uma URL SAS para um local Armazenamento do Microsoft Azure existente que contenha seu arquivo de dados pessoais.
Se você preparou um arquivo como a primeira etapa deste processo que está em conformidade com o esquema criado, você pode usar esse arquivo para o carregamento.

## <a name="legal-disclaimer"></a>Aviso de isenção de responsabilidade legal

[Aviso de isenção de responsabilidade legal da Microsoft Priva](priva-disclaimer.md)
