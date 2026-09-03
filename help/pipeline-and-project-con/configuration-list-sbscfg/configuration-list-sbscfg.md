---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/pipeline-and-project-configuration/configuration-list-sbscfg.html"
breadcrumb-title: ''
description: Saiba como usar as listas de configuração SBSCFG no Substance 3D Designer para gerenciar configurações e predefinições de projetos.
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > Configuration List - SBSCFG
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lista de configuração - SBSCFG
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---


# Lista de configuração - SBSCFG

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

O arquivo de Configuração é muito mais simples do que os [arquivos de Configuração de Projeto](../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md), pois contém apenas uma lista de projetos, além do modo de Compatibilidade de mecanismo. Eles servem como uma lista de configuração de projeto/ambiente de nível superior à dos arquivos de projeto individuais.

Você pode ter várias configurações para diferentes ambientes; esses arquivos podem ser mantidos sob controle de versão junto com os arquivos SBSPRJ.

</td>
<td width="25.00%" style="border: 0;" valign="top">

![Ícone de arquivo SBSCFG](configuration-list-sbscfg.resources/configuration-list-sbscfg-01.png "ícone de arquivo SBSCFG")

</td>
</tr>
</table>

## Modificando Arquivos de Configuração

Esses arquivos são simples, mas ainda podem ser modificados de duas maneiras diferentes, assim como os arquivos SBSPRJ.

### Nas Configurações do projeto

A seção realçada é a parte relacionada aos Arquivos de Configuração, basta adicionar mais Projetos à lista que estão armazenados no arquivo SBSCFG definido acima.

![Configurações do projeto](configuration-list-sbscfg.resources/configuration-list-sbscfg-02.png "Configurações do projeto")

### Edição externa como XML

Para o Windows, o <b>Bloco de Notas++</b> é uma boa opção gratuita, e o <b>Texto Sublime</b> do macOS é uma alternativa. No entanto, qualquer editor com recuo apropriado, seção recolhendo e alguma forma de realce de sintaxe vai tornar sua vida muito mais fácil.

Depois de abrir o arquivo SBSCFG em um editor, você verá um layout estruturado bastante direto, com seções correspondentes à interface do usuário.

```
<?xml version="1.0" encoding="UTF-8"?> 

<root> 

 <projects> 

  <projectfiles> 

   <size>1</size> 

   <_1 prefix="_"> 

    <path>custom_project.sbsprj</path> 

   </_1> 

  </projectfiles> 

 </projects> 

 <preferences> 

  <configuration> 

   <compatibilitymode>sbs_engine_v6</compatibilitymode> 

  </configuration> 

 </preferences> 

</root>
```


Observe que os projetos padrão e do usuário não são listados explicitamente, e que quaisquer projetos adicionais são definidos após esses.

O exemplo acima também usa [caminhos relativos](../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md). Observe que a lógica para caminhos relativos é ligeiramente diferente entre arquivos CFG e PRJ: para arquivos CFG, como acima, **você não deve digitar “file:/” antes do caminho**. Em vez disso, o caminho é simplesmente anexado ao local do arquivo CFG no qual é definido.

## Removendo a biblioteca padrão

Por enquanto, a biblioteca padrão não pode ser removida. Não é provavelmente uma boa ideia fazer isso, pois você perderia muitas funcionalidades do Designer.
