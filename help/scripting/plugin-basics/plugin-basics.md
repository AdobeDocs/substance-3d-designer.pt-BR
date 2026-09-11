---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/plugin-basics.html"
breadcrumb-title: ''
description: Conheça as noções básicas da criação de plug-ins Python para o Substance 3D Designer para ampliar a funcionalidade do aplicativo.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Plugin basics
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Noções básicas de plug-in
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 0%

---


# Noções básicas de plug-in

Um plug-in é um arquivo Python ou um módulo Python que define uma função <b>initializeSDPlugin()</b>.

A função <b>initializeSDPlugin()</b> é chamada quando o plug-in é carregado.\
Nesta função, você pode criar elementos da interface do usuário, registrar retornos de chamada e qualquer outra funcionalidade que você possa precisar.

Opcionalmente, o plug-in pode definir uma função <b>uninitializeSDPlugin()</b> que será chamada quando o plug-in for descarregado.\
Você pode usar essa função para liberar recursos, fechar conexões de rede e coisas semelhantes.

```
## Plugin entry point. Called by Designer when loading a plugin.

def initializeSDPlugin(): 

 print("Hello!") 

 

## If this function is present in your plugin,

## it will be called by Designer when unloading the plugin.

def uninitializeSDPlugin(): 

 print("Bye!")
```
