---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/nadir-patch.html"
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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 5%

---


# Nadir patch

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](nadir-patch.resources/nadir-patch-01.png){width="200px"}

<b>Entrada:</b> Visualização 3D > Ferramenta HDRI

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Este nó fornece funcionalidade para corrigir o ponto central do solo (nadir) de uma imagem mapeada esfericamente. Ele pode ser usado para ocultar ou “clonar” um nadir feio, ou câmera visível ou tripé. Funciona como um [Patch de clone](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md), mas com ajustes para imagens mapeadas esfericamente. O usuário seleciona um ponto em outro lugar da imagem, ou seja, o clonado e mesclado na base. Nenhuma outra entrada externa é necessária além de um único HDRI para processar, mas uma máscara externa pode ser usada como alfa para o efeito de correção.

o efeito pode ser verificado e validado rapidamente com o [Nadir extract](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/nadir-extract/nadir-extract.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada</b> <i>Entrada de cores</i> |  |
| <b>Entrada de máscara</b> <i>Entrada em tons de cinza</i> | Slot de máscara opcional usado para mascarar o patch. Funciona como um alfa. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Habilitar</b> <i>Falso/Verdadeiro</i> | Ativar ou desativar o efeito de patch. |
| <b>Mostrar Auxiliar de Quadros</b> <i>Falso/Verdadeiro</i> | Mostrar ou ocultar as linhas auxiliares, para fins de depuração. |
| <b>Thickness DO Quadro</b> <i>0.0 - 1.0</i> | Thickness de linhas auxiliares. |
| <b>Escala de correção</b> <i>0.0 - 1.0</i> | Escala de correção global e uniforme. Afeta a origem e o destino. |
| <b>Tamanho da correção</b> <i>0.0 - 1.0</i> | Tamanho não uniforme do patch. |
| <b>Rotação de correção</b> <i>0.0 - 1.0</i> | Rotação da correção. Afeta a origem e o destino. |
| <b>Alpha de correção</b> <i>Quadrado suave, Gaussiano, Entrada de máscara</i> | Defina qual alfa será usado para mesclar a correção com o fundo. |
| <b>Dureza do patch</b> <i>0.0 - 1.0</i> | Definir dureza/contraste de alfa. |
| <b>Deslocamento da Rotação da Origem</b> <i>0.0 - 1.0</i> | Rotação somente para a origem do patch. |
| <b>Coordenadas de Posição</b> |  |
| <b>Posição de Origem</b> | Posição da origem. Possui alça na exibição 2D. |
| <b>Posição da correção</b> | Posição de destino. Possui alça na exibição 2D. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="nadir-patch.resources/nadir-patch-02.gif" />
        </td>
    </tr>
</table>
