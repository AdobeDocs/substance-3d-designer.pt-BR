---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/pipeline-and-project-configuration/project-configuration-files-sbsprj.html"
breadcrumb-title: ''
description: Saiba como usar arquivos de configuração de projeto SBSPRJ no Substance 3D Designer para gerenciar configurações de projeto.
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > Project Configuration Files - SBSPRJ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Arquivos de configuração de projeto - SBSPRJ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '1001'
ht-degree: 0%

---


# Visão geral

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

<b>Os arquivos de configuração do projeto</b> são os arquivos mais complexos e expansivos usados para configurar o Substance 3D Designer.

Eles são especiais porque você pode usar vários arquivos de configuração de projeto, onde cada próximo projeto “filho” expande ou substitui o anterior “pai”. A menos que seja explicitamente necessário, as configurações não devem ser modificadas nem adicionadas aos arquivos de projeto, para que o Designer possa recorrer à sua configuração pai ou até mesmo aos padrões.

</td>
<td width="25.00%" style="border: 0;" valign="top">

![Ícone de arquivo SBSPRJ](../../assets/sbsprj.png "ícone de arquivo SBSPRJ")

</td>
</tr>
</table>

Por padrão, o Designer tem duas configurações de projeto ativas:

<b>Projeto Padrão: </b>Contém todas as configurações padrão e a biblioteca com a qual o Designer vem em uma nova instalação.*Somente leitura, não pode ser modificado nem removido.*

<b>Projeto de Usuário: </b>como os Padrões são somente leitura, *todas as alterações feitas pelo usuário* entram neste projeto por padrão. *Não pode ser removido.*

Esta configuração básica garante que a biblioteca padrão e outras configurações não possam ser corrompidas ou modificadas, mas ainda permite que usuários amadores únicos adicionem suas próprias modificações sem ter que se preocupar com configurações complexas.

## Expandir ou substituir

A maioria das configurações em um Projeto consecutivo <b>substituirá</b> as do Projeto anterior. Por exemplo, um plug-in diferente do Tangent Space em um arquivo de projeto personalizado substituirá qualquer plug-in TS definido no projeto padrão ou do usuário. Isso significa que, a menos que explicitamente necessário, é recomendado não substituir ou alterar as configurações em projetos filho.

No entanto, há algumas configurações que <b>se expandem</b> nas configurações pai, em vez de substituí-las. Essas configurações destacam-se pelos caminhos e filtros da biblioteca, então adicione mais conteúdo à biblioteca em vez de substituí-lo. Além disso, há os aliases (palavras-chave de caminho para caminhos de arquivo relativos) que se expandem, bem como substituem se uma duplicata for definida. Isso permite um grande controle sobre caminhos de arquivo de conteúdo e referências.

## Conteúdo do arquivo de projeto

Os arquivos de projeto podem conter as seguintes configurações:

<b>Exibição 3D: </b>Sombreador padrão, HDR e definições de estado de cena.

<b>Aliases: </b>Aliases de palavras-chave para caminhos relativos.

<b>Preparação: </b>Configurações para convenções de nomenclatura de cozimento.

<b>Geral: </b>Modelos de gráfico, plug-ins de espaço tangente, padrões de formato normal e de imagem.

<b>Biblioteca: </b>caminhos observados a serem exibidos na biblioteca.

<b>Script: </b>Scripts e interpretadores de retorno de chamada.

<b>Controle de Versão: </b>Configurações para integrar o controle de Versão no Designer.

## Modificação de arquivos de projeto

As configurações de projeto são, como todos os outros tipos, salvas como arquivos XML estruturados (usando uma extensão <b>.sbsprj</b>) que podem ser modificados por meio da interface do usuário do Designer ou de um editor de texto externo.

## Por dentro do Substance 3D Designer

Consulte a página [Configurações do projeto](../../interface/preferences-window/project-settings/project-settings.md) para saber mais sobre como gerenciar arquivos de projeto e alterar as configurações do projeto.

Os arquivos de projeto também incluem <b>categorias</b> e <b>filtros</b> personalizados para a [Biblioteca](../../interface/the-library/the-library.md), sobre a qual você pode saber mais na página [Gerenciar conteúdo e filtros personalizados](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md).

## Editar XML Externamente

Para o Windows, o [Bloco de Notas++](https://notepad-plus-plus.org) é uma boa opção gratuita. No macOS, o [Texto Sublime](https://www.sublimetext.com/) é uma alternativa. Dito isso, qualquer editor com recuo apropriado, seção recolhendo e alguma forma de realce de sintaxe vai tornar sua vida muito mais fácil.

Depois de abrir o arquivo SBSPRJ em um editor, você verá um layout estruturado bastante direto, com seções correspondentes a guias na interface do usuário. Nem todas as configurações serão documentadas aqui, pois isso é razoavelmente autoexplicativo.

![Edição de XML](../../assets/project-xml.png "Edição de XML")

## Caminhos e aliases relativos

Os caminhos relativos combinados com aliases são uma das partes mais complicadas, mas importantes, de uma configuração de projeto. Esta seção irá esclarecê-los. A adição de aliases personalizados para um arquivo de projeto específico é feita em [Configurações do Projeto](../../interface/preferences-window/project-settings/project-settings.md).

Um dos principais problemas com arquivos que fazem referência a outros arquivos em um sistema no computador de vários usuários é que os caminhos de arquivo absolutos não funcionarão. Os usuários podem definir seus repositórios SVN em locais completamente diferentes (por exemplo, C:/John/Gamedev/SubstanceLibrary ou D:/Dev/SubstanceLibrary). Aliases e caminhos relativos funcionam juntos para resolver esse problema. Caso contrário, você pode abrir o arquivo de outra pessoa e ele tentará procurar o nó personalizado usado no local específico em que o usuário o tinha localmente, o que você provavelmente não terá definido exatamente da mesma maneira.

Um <b>alias</b> é uma palavra-chave que substitui (parte de) um caminho. É semelhante a uma variável de ambiente do Windows, como %TEMP%, onde uma única palavra substitui um caminho frequentemente usado que é então definido centralmente. A vantagem é que há caminhos simplificados em todos os lugares e uma maneira de modificar todas as referências de uma só vez ao decidir realocar esse caminho.

>[!NOTE]
>
> **Exemplo de Alias**
> 
> | Alias | Valor de caminho real |
> | --- | --- |
> | <b>sbs</b> | *C:\Program Files\Adobe\Adobe Substance 3D Designer\resources\packages* |
> | <b>personalizado</b> | *D:\Dev\CustomProject\Substance* |
> 
> A biblioteca padrão está localizada, por padrão, em *C:\Program Files\Adobe\Adobe Substance 3D Designer\resources\packages*. Todos os gráficos que usam o conteúdo padrão fazem referência a esse diretório. Em vez de referenciar o caminho completo, um alias de &#39;<b>SBS</b>&#39; (sem aspas) é definido. No caso de uma biblioteca padrão, o valor exato do caminho do SBS é definido na instalação para o diretório que o usuário escolher para o Designer.
> 
> Internamente, uma referência é modificada da seguinte maneira, quando contém um caminho com um alias:
> 
> **C:\Program Files\Adobe\Adobe Substance 3D Designer\resources\packages\blur\_hq.sbs => <b>sbs://</b>desfoque\_hq.sbs**

<b>Os caminhos relativos</b> são sempre relativos ao arquivo em que estão definidos. Isso significa que o local atual do arquivo de configuração determina a maior parte do caminho, e os caminhos de alias serão baseados nele, principalmente apenas adicionando uma subpasta. <b>Isso significa que é altamente recomendável colocar os arquivos sbsprj próximos às pastas que você deseja observar!</b>

Por exemplo, pegue um repositório em *C:/Versioncontrol/Substance/* contendo *CustomProject.sbsprj* e, em seguida, duas pastas, */Base* e */Tools,* contendo nós.

Para definir dois Aliases relativos para Base e Ferramentas, seria feito o seguinte no arquivo SBSPRJ:

### C:/Versioncontrol/Substance/CustomProject.sbsprj

```
   <urlaliases> 

    <size>2</size> 

    <_2 prefix="_"> 

     <path>file:Base</path> 

     <name>BaseAlias</name> 

    </_2> 

    <_1 prefix="_"> 

     <path>file:Tools</path> 

     <name>ToolsAlias</name> 

    </_1> 

   </urlaliases>
```


O resultado desse arquivo de configuração é o seguinte:

**BaseAlias://** será *C:/Versioncontrol/Substance/Base/* e **ToolsAlias://** será *C:/Versioncontrol/Substance/Tools/.*

Se você desejar definir apenas *C:/Versioncontrol/Substance/*, o caminho será listado como **”file:.”**, o ponto que significa o local do próprio arquivo.
