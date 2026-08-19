---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/scripting/porting-previous-plugins.html"
breadcrumb-title: ''
description: Saiba como migrar plug-ins de versões anteriores do Substance Designer para a API Python atual.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Porting previous plugins
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Migrar plug-ins anteriores
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---


# Migrar plug-ins anteriores

Devido às alterações feitas para oferecer suporte ao Qt para Python, **os plug-ins anteriores não funcionarão mais**.\
Em particular, observe o seguinte:

## Carregamento e descarregamento de plug-ins

Os plug-ins agora são carregados quando o aplicativo <b>é iniciado</b> e são descarregados quando ele <b>sai</b>.\
Portanto, não é *necessário* para que os plug-ins herdem mais de &#39;*sdplugins.Plugin*&#39;.

Para obter mais informações, consulte a seção [Noções básicas sobre plug-ins](../../scripting/plugin-basics/plugin-basics.md).

## Criando elementos da interface do usuário

Os plug-ins *não precisam mais* definir um &#39;*sdplugins.PluginDesc*&#39;.\
Em vez disso, os plug-ins podem usar o <b> novo objeto [UI manager](https://helpx.adobe.com/br/substance-3d/unlisted/documentation/sddoc/scripting-api-next-172825023.html)</b> e o <b>Qt for Python</b> para criar os elementos de interface de usuário necessários.

Você pode encontrar pequenas amostras de código na seção [Criando elementos da interface do usuário](../../scripting/creating-user-interface/creating-user-interface-elements.md).

## Substituição de usos do contexto de localização

A classe &#39;*SDLocationContext*&#39; foi *removida* da API Python.\
Os plug-ins podem usar o objeto </b> do <b>[UI manager](https://helpx.adobe.com/br/substance-3d/unlisted/documentation/sddoc/scripting-api-next-172825023.html) para acessar o gráfico e a seleção ativos no momento.

Você pode encontrar alguns exemplos na seção [Acessando gráficos e seleções](../../scripting/accessing-graphs-and-sel/accessing-graphs-and-selections.md).
