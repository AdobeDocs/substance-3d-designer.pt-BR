---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/pipeline-and-project-configuration/environment-variables.html"
breadcrumb-title: ''
description: Saiba como usar variáveis de ambiente no Substance 3D Designer para definir caminhos e configurações do sistema.
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > Environment variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Variáveis de ambiente
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 3%

---


# Variáveis de ambiente

Esta página lista variáveis de ambiente que podem ser usadas para substituir o comportamento padrão do aplicativo.

| Variável | Descrição |
| --- | --- |
| **SBS\_DESIGNER\_PYTHON\_PATH** | O caminho a partir do qual o Designer carregará os [plug-ins Python](../../scripting/plugin-basics/plugin-basics.md). |
| **SUBSTANCE\_DESIGNER\_LICENSE** | O local do arquivo de licença (*license.key*) que deve ser usado pelo Designer.   Substitui o caminho definido no [Assistente de Ativação](../../getting-started/activation-and-licenses/activation-and-licenses.md) do Designer.  **Observação:** versões antigas podem precisar usar um nome de variável alternativo:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>SUBSTANCE_DESIGNER_6_LICENSE</strong></li><li data-preserve-html="true"><strong>SUBSTANCE_DESIGNER_5_LICENSE</strong></li></ul> |
| <b>OCIO</b> | O caminho para o arquivo de configuração OCIO que deve ser usado ao usar o [gerenciamento de cores](../../color-management/color-management.md) do OpenColorIO.   Substitui o caminho definido nas configurações de gerenciamento de cores do Designer em [Configurações do projeto](../../interface/preferences-window/project-settings/project-settings.md). |
| **ALLEGO\_LICENSE\_IDLE\_DELAY** | O atraso em segundos antes de liberar uma licença no caso de uma configuração multiusuário O padrão é 7.200 segundos (2 horas). |
