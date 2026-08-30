---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/plugin-search-paths.html"
breadcrumb-title: ''
description: Configure caminhos de pesquisa de plug-ins no Substance 3D Designer para especificar onde os plug-ins Python estão localizados.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Plugin search paths
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Caminhos de pesquisa de plug-in
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 0%

---


# Caminhos de pesquisa de plug-in

O Designer procurará plug-ins em diretórios específicos (ou seja, caminhos de pesquisa). Esta página explica como configurar esses caminhos.

Os usuários podem *adicionar diretórios personalizados* manualmente nas preferências de software ou especificá-los usando variáveis de ambiente.

## Adição manual de caminhos de pesquisa de plug-ins

1. Ir para <b>Editar > Preferências...</b>
1. Selecionar a categoria <b>Projetos</b>
1. Selecione o <b>Arquivo de Projeto</b> que deseja editar
1. Na guia <b>Python</b>, clique no botão *<b>+</b>*para adicionar o diretório que contém os plug-ins
1. Clique em <b>OK</b> para validar

![Configurações de plug-ins Python caminhos de pesquisa Configurações de projeto](plugin-search-paths.resources/image-70.png "Configurações de plug-ins Python caminhos de pesquisa Configurações de projeto")

## Uso de variáveis de ambiente

O aplicativo procurará plug-ins em todos os caminhos especificados usando a variável de ambiente <b>SBS\_DESIGNER\_PYTHON\_PATH </b>.
