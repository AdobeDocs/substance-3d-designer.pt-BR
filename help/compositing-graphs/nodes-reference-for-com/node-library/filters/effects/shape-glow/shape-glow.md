---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-glow.html"
breadcrumb-title: ''
description: Use o nó Brilho da forma para adicionar efeitos de brilho a formas e texturas para criar efeitos visuais luminosos e atmosféricos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Glow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Brilho da forma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 67f8f59bf50387b87e9009b042f269208c665c65
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 4%

---


# Brilho da forma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-glow.resources/shape-glow-grayscale.png){width="128px"}

![](shape-glow.resources/shape-glow.png){width="128px"}

<b>Entrada:</b> Filtros > Efeitos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Cria um brilho suave ao redor de uma máscara de entrada (para a versão em tons de cinza) ou de uma forma com um canal alfa (para a versão colorida). Em comparação ao [Brilho](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/glow/glow.md), ele funciona de maneiras mais semelhantes a outros softwares de edição de imagens 2D, pois é um efeito mais completo com mais controles.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Modo</b> <i>Suave, Preciso</i> | Alterna entre dois modos de precisão. |
| <b>Largura</b> <i>-1.0 - 1.0</i> | Controla o quanto o brilho alcança. |
| <b>Propagação</b> <i>0.0 - 1.0</i> | Corte/limite para o efeito de desfoque faz com que o brilho pareça sólido próximo à forma. |
| <b>Opacidade</b> <i>0.0 - 1.0</i> | Opacidade de mesclagem para o efeito de brilho. |
| <b>(Sombra) Cor</b> <i>(Valor da cor)</i> | Tonalidade de cor a ser aplicada ao brilho. |
| <b>Cor da máscara</b> <i>(Valor da cor) (Somente Versão em Tons de Cinza)</i> | Cor sólida a ser usada para a saída mapeada de transparência. |
| <b>A Entrada É Pré-Multiplicada</b> <i>Falso/Verdadeiro (Somente Versão Colorida)</i> | Se a entrada deve ser assumida como pré-multiplicada. |
| <b>Saída Pré-Multiplicada</b> <i>Falso/Verdadeiro</i> | Se a saída deve ser pré-multiplicada. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape-glow.resources/shapeglow-ex.png" />
        </td>
    </tr>
</table>
