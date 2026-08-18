---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/scripting/logging.html"
breadcrumb-title: ''
description: Saiba como implementar o registro em plug-ins Python da Substance 3D Designer para depuração e monitoramento.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Logging
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Registros
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 4%

---


# Registros

Recomendamos usar o módulo de log padrão do Python para o registro.

O módulo <b>sd</b> contém classes auxiliares para redirecionar o log para o console do Designer.

## Registro no painel do console do Designer

```
import logging 

import sd 

 

 

## Create a logger.

logger = logging.getLogger("MyLogger") 

 

 

## Add a handler to redirect logging to Designer's console panel.

ctx = sd.getContext() 

logger.addHandler(ctx.createRuntimeLogHandler()) 

 

 

## Do not propagate log messages to Python's root logger.

logger.propagate = False 

 

 

## Set the default log level if needed.

logger.setLevel(logging.DEBUG) 

 

 

## Use the logger

logger.info("Info message") 

logger.warning("Warning message") 

logger.error("Error message")
```
