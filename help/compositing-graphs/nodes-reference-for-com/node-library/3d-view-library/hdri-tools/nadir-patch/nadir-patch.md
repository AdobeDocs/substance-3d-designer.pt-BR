---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/nadir-patch.html"
breadcrumb-title: ''
description: Use o nó Nadir patch para corrigir a região inferior dos panoramas HDRI para corrigir artefatos inferiores em mapas de ambiente.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Nadir Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Nadir patch
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 1%

---


# Nadir patch

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-nadir-patch.png){width="200px"}

## Nadir patch

**Entrada:** *Exibição 3D/Ferramentas HDRI*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

Este nó fornece funcionalidade para corrigir o ponto central do solo (nadir) de uma imagem mapeada esfericamente. Ele pode ser usado para ocultar ou “clonar” um nadir feio, ou câmera visível ou tripé. Funciona como um [Patch de clone](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md), mas com ajustes para imagens mapeadas esfericamente. O usuário seleciona um ponto em outro lugar da imagem, ou seja, o clonado e mesclado na base. Nenhuma outra entrada externa é necessária além de um único HDRI para processar, mas uma máscara externa pode ser usada como alfa para o efeito de correção.

o efeito pode ser verificado e validado rapidamente com o [Nadir extract](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/nadir-extract/nadir-extract.md).

## Entradas

* **Entrada**: *Entrada de Cores*
* **Entrada de máscara**: *entrada em tons de cinza*\
  Slot de máscara opcional usado para mascarar o patch. Funciona como um alfa.

## Parâmetros

* **Habilitar**: *Falso/Verdadeiro*\
  Ativar ou desativar o efeito de patch.
* **Mostrar auxiliar de quadros**: *Falso/Verdadeiro*\
  Mostrar ou ocultar as linhas auxiliares, para fins de depuração.
* **Thickness de quadros**: *0.0 - 1.0*\
  Thickness de linhas auxiliares.
* **Escala de Correção**: *0.0 - 1.0*\
  Escala de correção global e uniforme. Afeta a origem e o destino.
* **Tamanho do Patch**: *0.0 - 1.0*\
  Tamanho não uniforme do patch.
* **Rotação de Correção**: *0.0 - 1.0*\
  Rotação da correção. Afeta a origem e o destino.
* **Alpha de Correção**: *Quadrado Suave, Gaussiano, Entrada de Máscara*\
  Defina qual alfa será usado para mesclar a correção com o fundo.
* **Dureza do Patch**: *0.0 - 1.0*\
  Definir dureza/contraste de alfa.
* **Deslocamento da Rotação da Origem**: *0.0 - 1.0*\
  Rotação somente para a origem do patch.
* **Coordenadas de Posição**
  * **Posição de Origem**:\
    Posição da origem. Possui alça na exibição 2D.
  * **Posição da correção**:\
    Posição de destino. Possui alça na exibição 2D.

## Imagens de exemplo

![](../../../../../../assets/nadir-patch-ex.gif)

</td>
</tr>
</table>
