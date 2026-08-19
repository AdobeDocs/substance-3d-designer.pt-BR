---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/mdl-library.html"
breadcrumb-title: ''
description: Acesse a biblioteca Idioma de definição de material no Substance 3D Designer para criar materiais personalizados.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > MDL library
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Biblioteca MDL
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---


# Biblioteca MDL

Esta página apresenta a biblioteca de conteúdo relacionado a [gráficos MDL](../../mdl-graphs/mdl-graphs.md) e materiais incluídos no Substance 3D Designer. Ele também explica como instalar e gerenciar conteúdo personalizado na [Biblioteca](../../interface/the-library/the-library.md).

## Conteúdo MDL na biblioteca

Os nós utilizáveis nos gráficos MDL estão disponíveis na seção <b>mdl</b> da [Biblioteca](../../interface/the-library/the-library.md). Os nós são organizados em filtros de acordo com o módulo MDL em que são definidos.\
Se os módulos estiverem armazenados em subpastas, essa hierarquia será *espelhada* na Biblioteca como *categorias*.

Esta seção inclui conteúdo das seguintes fontes:

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Conteúdo integrado

O Designer inclui módulos MDL que contêm blocos de construção básicos para a criação de gráficos MDL, bem como definições completas de material prontas para serem usadas.

Este conteúdo está armazenado neste local no diretório de instalação: `./resources/view3d/iray/`

### Conteúdo personalizado

Além do conteúdo interno, você pode adicionar *seus próprios* módulos MDL à biblioteca.

Na verdade, qualquer módulo MDL encontrado nos diretórios listados na seção <b>MDL</b> das [Configurações do projeto](../../interface/preferences-window/project-settings/project-settings.md) é adicionado a esta seção *cumulativamente* entre os arquivos de projeto.

### NVIDIA vMaterials

Se a biblioteca [vMaterials](https://developer.nvidia.com/vmaterials) da NVIDIA estiver instalada, ela será *adicionada automaticamente* à biblioteca em sua *própria categoria*.

</td>
<td style="border: 0;" valign="top">

![Recursos MDL na Biblioteca](../../assets/mdl-library.png "Recursos MDL na Biblioteca")

Seção *”mdl” na Biblioteca, a biblioteca vMaterials e o conteúdo personalizado estão enquadrados*

</td>
</tr>
</table>

## Conteúdo MDL na visualização 3D

Todos os módulos MDL disponíveis na Biblioteca podem ser usados na [Exibição 3D](../../interface/3d-view/3d-view.md) quando o renderizador Iray é usado.

Abra o menu <b>Materiais</b> e abra um *submenu de material da cena* para procurar os módulos MDL disponíveis. A lista inclui:

* Conteúdo integrado
* Conteúdo personalizado
* NVIDIA [vMaterials](https://developer.nvidia.com/vmaterials)
* [Gráficos MDL](../../mdl-graphs/mdl-graphs.md) carregados

![Materiais MDL na Visualização 3D](../../assets/mdl-apply-in-3dview-material-list.png "Materiais MDL na Visualização 3D")

*Materiais MDL na Visualização 3D*
