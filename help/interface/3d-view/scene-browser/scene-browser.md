---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/3d-view/scene-browser.html"
breadcrumb-title: ''
description: Use o Navegador de cena para navegar e gerenciar elementos, materiais e objetos da cena 3D na viewport.
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D view > Scene browser
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Navegador de cena
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 1%

---


# Navegador de cena

O navegador de cenas da visualização 3D lista todos os elementos na cena e sua hierarquia.

Ela oferece controles para selecionar objetos, alternar sua visibilidade e selecionar qual material deve [substituir um material de cena](../../../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md).

Como o Designer usa o [USD](https://openusd.org/release/index.html) para descrever e gerenciar suas cenas, sua terminologia e conceitos são encontrados nessa árvore de cenas.

É exibido clicando em seu botão de alternância dedicado ![](../../../assets/sceneBrowser-toggleButton.png) na [barra de ferramentas Exibir cena 3D](../../../interface/3d-view/3d-view.md).

![Navegador de cena - Cena 3D carregada](../../../assets/loaded3DScene.png "Navegador de cena - Cena 3D carregada"){zoomable="yes"}

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Árvore de cenas

</td>
<td style="border: 0;" valign="top">

### Alternar objetos na cena

</td>
<td style="border: 0;" valign="top">

### Materiais conectados

</td>
</tr>
</table>

## Árvore de cenas

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

O navegador de cenas exibe uma lista de objetos organizados em uma árvore hierárquica.

Os objetos têm parentesco com outros objetos, até a raiz da cena. Um objeto pai tem um botão de seta que é usado para expandir ou recolher a lista de seus filhos.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Navegador de cena - Árvore de cena](../../../assets/sceneBrowser-sceneTree.png "Navegador de cena - Árvore de cena"){zoomable="yes"}

</td>
</tr>
</table>

Deixe o cursor sobre qualquer item na árvore por alguns segundos para exibir uma dica de ferramenta com as seguintes informações:

* <b>Caminho:</b> o caminho completo do objeto na cena.
* <b>TypeName:</b> o tipo USD do objeto.
* <b>Documentação:</b> informações detalhadas sobre o objeto como um elemento de cena USD.

As malhas têm informações adicionais: contagem de vértices, contagem de face e contagem de UV.

### Objetos adicionados pelo Designer

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

O Designer adiciona alguns objetos a qualquer cena carregada. Os objetos adicionados pelo Designer são rotulados em <b>negrito</b>.

Ao usar a ação “Editar...” nos menus Luzes, Câmera e Ambiente, esses são os objetos que estão sendo editados, independentemente de haver outras luzes, câmeras ou ambientes na cena.

Esses objetos são incluídos na cena quando [exportados](../../../working-with-3d-scenes/exporting-scenes/exporting-scenes.md).

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Navegador de cena - Objetos adicionados pelo Designer listados em negrito](../../../assets/sceneBrowser-addedByDesigner.png "Navegador de cena - Objetos adicionados pelo Designer listados em negrito"){zoomable="yes"}

</td>
</tr>
</table>

* <b>Câmera:</b> a câmera padrão da cena. Esta é a única câmera que você pode interagir no Designer. Todas as câmeras incluídas em uma cena carregada são adicionadas como predefinições para a câmera padrão.
* <b>Ambiente:</b> o ambiente padrão da cena. Qualquer textura aplicada ao ambiente da cena será aplicada somente a esse ambiente. Da mesma forma, girar o ambiente afeta apenas esse ambiente.\
  Quando uma cena carregada inclui uma ou mais iluminações do ambiente ([DomeLight](https://openusd.org/release/user_guides/schemas/usdLux/DomeLight.html) em USD), o ambiente padrão é automaticamente desabilitado para não interferir na iluminação do ambiente da cena.
* <b>Luz de ponto #:</b> se qualquer uma das luzes de ponto do Designer estiver ativada em Luzes > Editar propriedades, cada luz de ponto será adicionada à cena.

## Alternar objetos na cena

### Todos os tipos

Qualquer objeto pode ser ativado e desativado na cena. Quando desativado, um objeto não contribui mais para a cena: ele não projeta sombras, emite ou reflete luz.

O estado de um objeto pai é transferido para seus filhos, portanto, desativar um objeto pai também desativa seus filhos.

A visibilidade de um objeto pode ser alternada clicando em seu botão de olho ![](../../../assets/sceneBrowser-eyeButton.png) ou em seu menu contextual. O menu oferece mais algumas ações para gerenciar a visibilidade dos objetos da cena:

* <b>Ocultar:</b> desabilite o objeto selecionado.
* <b>Mostrar:</b> habilite o objeto selecionado.

Algumas ações afetam a visibilidade das malhas especificamente:

* <b>Mostrar apenas:</b> desabilite todas as malhas, exceto a selecionada e suas filhas.
* <b>Mostrar tudo:</b> habilitar todas as malhas.

Os objetos pai têm as seguintes ações adicionais:

* <b>Ocultar filhos:</b> desabilite todos os filhos do objeto selecionado, recursivamente.
* <b>Mostrar filhos:</b> habilite recursivamente todos os filhos do objeto selecionado.
* <b>Expandir todos os filhos:</b> expande recursivamente todas as listas de filhos sob o objeto selecionado.
* <b>Recolher todos os filhos:</b> Recolher todas as listas de filhos no objeto selecionado, recursivamente.

![Navegador de cena - Alternando a visibilidade do objeto](../../../assets/sceneBrowser-toggleVisibility.gif "Navegador de cena - Alternando a visibilidade do objeto"){zoomable="yes"}

### Ambientes

A visibilidade de qualquer luz ambiente (DomeLight) pode ser ativada e desativada da mesma forma que outros objetos.

Quando uma luz ambiente é desativada, sua contribuição de iluminação para a cena também é desativada.

Se mais de uma iluminação ambiente estiver habilitada, suas contribuições de iluminação serão *adicionadas cumulativamente*.

![Navegador de cena - Alternando a visibilidade do ambiente](../../../assets/sceneBrowser-toggleEnvLights.gif "Navegador de cena - Alternando a visibilidade do ambiente"){zoomable="yes"}

### Luzes

O mesmo vale para todas as luzes na cena: cada uma pode ser alternada individualmente.

![Navegador de cena - Alternando visibilidade da luz](../../../assets/sceneBrowser-toggleLights.gif "Navegador de cena - Alternando visibilidade da luz"){zoomable="yes"}

## Materiais conectados

O navegador de cena também permite conectar qualquer material substituído a outro material listado pelo Designer no [menu Materiais](../../../interface/3d-view/3d-view.md) da exibição 3D.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Os materiais listados pelo Designer são os objetos de material na árvore de cena usada em pelo menos uma malha.

Ao [substituir](../../../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md) qualquer um desses materiais, uma cópia é criada pelo Designer, com um sufixo numérico.

Um material substituído oferece um item adicional em seu menu contextual: o submenu &#39;[Material conectado](../../../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md)&#39; lista todos os outros materiais disponíveis que podem ser usados para substituir esse material.

</td>
<td style="border: 0;" valign="top">

![Navegador de cena - Material conectado](../../../assets/sceneBrowser-connectedMaterial.png "Navegador de cena - Material conectado"){zoomable="yes"}

</td>
</tr>
</table>
