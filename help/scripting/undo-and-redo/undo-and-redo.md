---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/scripting/undo-and-redo.html"
breadcrumb-title: ''
description: Saiba como implementar a funcionalidade de desfazer e refazer em scripts Substance 3D Designer Python para ações do usuário.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Undo and redo
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Desfazer e refazer
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 0%

---


# Desfazer e refazer

Com a classe <b>SDHistoryUtils.UndoGroup</b>, os usuários podem *agrupar ações* para *desfazer ou refazer* todas elas em um único comando.

Esses grupos são *nomeados* pelos usuários e aparecerão por esse nome na lista de desfazer/refazer na interface do usuário.  Isso torna um grande número de ações mais gerenciáveis.

```
import sd 

from sd.api.sdhistoryutils import * 

 

## Get the application and package manager objects.

cxt = sd.getContext() 

app = cxt.getSDApplication() 

pkgMgr = app.getPackageMgr() 

 

## Group one or more changes into an undo group.

with SDHistoryUtils.UndoGroup("My Undo Group"): 

## Create two new packages.

    pkgMgr.newUserPackage() 

    pkgMgr.newUserPackage()
```
