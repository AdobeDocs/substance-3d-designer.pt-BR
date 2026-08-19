---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/scripting/accessing-graphs-and-selections.html"
breadcrumb-title: ''
description: Saiba como acessar e manipular gráficos e seleções de nós em scripts Substance 3D Designer Python.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Accessing graphs and selections
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Acessar gráficos e seleções
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---


# Acessar gráficos e seleções

A classe <b>SDApplication</b> contém alguns métodos úteis que permitem acessar o gráfico *atualmente ativo* e a *seleção atual* dentro dele.

```
import sd 

 

## Get the application and UI manager object.

ctx = sd.getContext() 

app = ctx.getSDApplication() 

uiMgr = app.getQtForPythonUIMgr() 

 

## Get the current graph.

g = uiMgr.getCurrentGraph() 

print("The current graph is %s" % g) 

 

## Get the currently selected nodes.

selection = uiMgr.getCurrentGraphSelectedNodes() 

for node in selection: 

 print("Node %s" % node)
```


Um gráfico exibido em uma exibição de Gráfico *específica* pode ser acessado usando um <b>graphViewID</b>.

Esse método é útil ao criar barras de ferramentas de visualização de gráfico personalizadas. A amostra <b>Criando barras de ferramentas em exibições de gráfico</b> no capítulo [Criando elementos de interface do usuário](../../scripting/creating-user-interface/creating-user-interface-elements.md) fornece mais detalhes.
